# Civic Trace — Proposed Architecture

> Architecture specification for an unbuilt hackathon MVP. It documents intended behaviour, not a live system.

## Logical flow

```text
Citizen Portal      Worker Portal      Authority Dashboard
       \                 |                   /
        \                |                  /
              React Web Frontend
                      |
            Supabase Auth + API
                      |
           PostgreSQL / Supabase
            |        |        |
          Assets  Maintenance Reports
            |        |        |
        Schedules  Approvals / Audit
                      |
                  Photo Storage
                      |
             Status / Alert Rules
                      |
              Leaflet Asset Map
```

## Minimal data entities

| Entity | Representative fields |
| --- | --- |
| `assets` | `id`, `type`, `name`, `location`, `condition_status` |
| `maintenance_records` | `id`, `asset_id`, `work_type`, `performed_at`, `submitted_by`, `review_status`, `approved_by`, `approved_at` |
| `maintenance_evidence` | `id`, `record_id`, `photo_path`, `uploaded_at` |
| `schedules` | `asset_id`, `next_due_at`, `interval_days` (optional) |
| `defect_reports` | `id`, `asset_id`, `reported_at`, `description`, `status` |
| `contracts` | `id`, `asset_id`, `contractor_name`, `liability_start`, `liability_end` (when recorded) |
| `audit_events` | `id`, `actor_id`, `action`, `target_id`, `created_at` |

## Important workflow: updating `last maintained`

1. An authenticated maintenance worker submits work details and evidence.
2. The entry is stored with `review_status = pending`; it does **not** alter the verified public date.
3. An authorized reviewer approves or rejects the submission.
4. On approval, the entry becomes part of the public-safe maintenance timeline.
5. The displayed **last maintained** date is derived from the most recent *approved performed_at* date (not simply the submission or approval date).
6. Previous records and decision timestamps remain stored; corrections follow an auditable process.
7. If appropriate, the next service date is calculated from the asset's configured schedule or set explicitly by an official.

This prevents ordinary citizen reports or unreviewed worker submissions from directly changing the verified maintenance date.

## Rules in the initial demo

- **Overdue:** `next_due_at` is before today's date and no approved work has satisfied that due date.
- **Approaching due:** scheduled service is within a configurable warning window.
- **Possible warranty review:** a defect report date falls within a recorded liability period for the relevant asset/work; forward to official review.
- **Repeat defects:** multiple open/recent reports on the same asset produce a review flag (do not label them verified failures automatically).

All rules require sensible handling of missing dates and incomplete records.

## Security and privacy requirements

- Use Supabase Auth and role-based access / row-level security policies.
- Never store API secrets in the frontend repository.
- Keep non-public contact details and sensitive maintenance evidence restricted.
- Distinguish **reported**, **submitted**, and **officially approved** information.
- Record approvals and edits; ensure authorized reviewers cannot silently erase history.
- Label all simulated assets and statistics clearly in the hackathon demo.

## Scope exclusions for Round 1 / MVP

- No live city-government integrations.
- No validated predictive AI model or guarantee of flood/stampede prevention.
- No automatic contractor fault determination.
- No blockchain claim or tamper-proof guarantee.
- No verified financial savings claim.
