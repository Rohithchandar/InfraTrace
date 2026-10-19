# Civic Trace

**Every Asset. Every Repair. Complete Accountability.**

> **DEXATHON 2026 | Open Innovation | Round 1 concept / proposal stage**

Civic Trace is a proposed **unified public infrastructure maintenance and accountability platform**. It aims to make maintenance history, upcoming service dates, reported defects, and available contractor information easier to track across public assets.

**Project status:** Planning and documentation. A functional prototype has **not yet been published** in this repository. The workflows and technology stack below describe the intended MVP, not completed capabilities.

## The problem

Roads, stormwater drains, and streetlights need continuous maintenance, but relevant records may be scattered across departments and difficult for residents to access. Complaint-driven processes can overlook scheduled maintenance, repeated faults, and whether recently repaired assets are still covered by a contractor's defect-liability period.

## Our proposed solution

Give each registered public asset a **digital infrastructure passport** with its maintenance timeline. Citizens see public-safe asset information; workers submit maintenance evidence; authorized officials review work and approve updates.

### Initial infrastructure categories

| Asset | Example records |
| --- | --- |
| **Roads** | Construction/resurfacing dates, pothole repairs, contractor and defect-liability information |
| **Stormwater drains** | Cleaning/desilting history, reported blockages, scheduled cleaning |
| **Streetlights** | Installations, inspections, electrical faults, component replacements |

The data model is intended to accommodate other municipal assets in future phases.

## Key proposed features

- **Digital infrastructure passport:** Unique asset ID, asset type, location, available records, and chronological service history.
- **Verified maintenance updates:** Workers submit work details, timestamps, and before/after photos; an authorized official approves them before the public `last maintained` date changes. Previous records remain intact.
- **Preventive schedule alerts:** Highlight upcoming and overdue service dates using clear, rule-based checks.
- **WarrantyGuard:** Flag newly reported defects occurring within a *recorded* defect-liability period for official review; do not automatically assign contractor fault.
- **Citizen reporting:** Report visible defects with notes and images, linked to an asset.
- **Authority dashboard:** Review submissions, overdue assets, recurring reports, and maintenance status.
- **Map view:** Show sample assets and condition/status indicators by location.

**Important:** A photo, timestamp, or GPS coordinate alone does not prove that work was properly completed. Approval and audit history support traceability but cannot eliminate false reports.

## What makes Civic Trace different?

Civic Trace is **not just another complaint app**. Its intended focus is the *asset lifecycle*: service history, scheduled work, evidence-backed updates, warranty review, and public-facing visibility in one place. Existing municipal systems may offer individual components; Civic Trace proposes integrating them into one understandable workflow.

## Proposed MVP (24-hour hackathon)

The planned demonstration uses **10–20 clearly labelled sample assets** across roads, drains, and streetlights.

1. Interactive asset map and searchable asset detail view
2. Citizen defect-report submission form
3. Maintenance submission with photos and dates
4. Authorized approval/rejection workflow
5. Historical maintenance timeline and updated last-maintained date
6. Rule-based overdue maintenance and warranty-review flags

**Data source for demo:** fictional/representative data only, clearly marked as such. Actual municipal deployment would require authorized records, data-sharing arrangements, appropriate security controls, and department participation.

## Proposed technology stack

| Component | Technology |
| --- | --- |
| Frontend | React + Tailwind CSS |
| Backend, database, authentication | Supabase (PostgreSQL + Supabase Auth) |
| Photo attachments | Supabase Storage |
| Maps | Leaflet + OpenStreetMap |
| Alerts | JavaScript rule-based service |
| Hosting | Vercel |

These are planned choices and may be adjusted during implementation.

## User roles

- **Citizens:** Explore asset records and submit observations/defect reports.
- **Maintenance workers:** Submit work completion records and evidence.
- **Authorized officials:** Verify/approve maintenance submissions and manage schedules.

## Documentation

- [Round 1 project proposal](docs/PROJECT_PROPOSAL.md)
- [Technical architecture and record workflow](docs/ARCHITECTURE.md)
- [24-hour MVP roadmap](docs/MVP_ROADMAP.md)

## Project roadmap

**Round 1:** Define the problem, differentiated solution, proposed architecture, realistic scope, and demonstration flow.

**Prototype phase:** Implement the three portals, sample asset database, approval pipeline, map, and status rules. Test user roles, dates, and auditability.

**Longer term:** Validate data partnerships, improve verification, and explore maintenance-risk forecasting **only after** obtaining enough reliable historical records.

## Team

**Hackathon team:** Team Verity  
**Team leader:** Rohith Chandar R. G.

### Team members

1. **Rohith Chandar R. G.**
2. Sanlyn Bright A.
3. Rakshana V.
4. Rifni Roch R.
5. Rithika Sri P.
6. Sanjana K.

## Disclaimer

This is a student hackathon project proposal, **not** an official municipal website or an endorsed government service. Any sample contractor names, costs, locations, or maintenance entries are demonstration data. Do not rely on demo records for real infrastructure decisions.
