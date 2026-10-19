# InfraTrace — 24-Hour MVP Development Roadmap

**Status:** Planned, not yet implemented.

| Time | Work package | Deliverable |
| --- | --- | --- |
| Hours 0–4 | Set up React app, Supabase project, asset schema, UI wireframes | Working skeleton and sample database |
| Hours 4–12 | Asset list/map, public asset detail pages, citizen defect form | Citizen-facing workflow |
| Hours 12–18 | Worker submissions, photo uploads, official approval workflow, maintenance timeline | Verified-update workflow |
| Hours 18–22 | Overdue scheduling rule, contract-period review flag, admin dashboard | Status and alert demonstrations |
| Hours 22–24 | Test user permissions, date logic, responsive UI; prepare demo | End-to-end presentation |

## Demo flow

1. Browse sample infrastructure assets on a map.
2. Open a drain record and show its last verified maintenance date and upcoming due date.
3. Submit a fictional blockage report as a citizen.
4. Log a cleaning job as a maintenance worker with sample evidence.
5. Show that the public last-maintained date **has not yet changed**.
6. Approve the job as an official and show the updated service timeline and next due date.
7. Demonstrate a road defect report within a recorded contract liability period, triggering **review**, not an automatic blame assignment.

## Definition of done

- Works with sample data, not hardcoded screenshots alone.
- Approval updates the last-maintained date correctly and preserves history.
- Citizen reports cannot impersonate verified maintenance.
- Scheduled work and possible warranty reviews are flagged with transparent rules.
- The team can complete the full demonstration without manually changing database rows.
