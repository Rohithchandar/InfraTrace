# Civic Trace — Round 1 Project Proposal

**Event:** DEXATHON 2026  
**Theme:** Open Innovation  
**Stage:** Project idea / proposal (not yet a deployed product)

## 1. Problem statement

Residents can often report damaged civic assets, yet a complaint alone does not tell them when the asset was last maintained, when service is next due, which work was completed, or whether a newly reported issue falls within a recorded contractor defect-liability period. Asset and work-order data can also be dispersed across administrative systems.

## 2. Proposed approach

Civic Trace proposes an integrated digital infrastructure passport for each registered asset. It links inspection and maintenance entries, planned service dates, defect reports, verification evidence, and appropriate public-facing contractor data.

**Goal:** Move from isolated complaints toward traceable maintenance lifecycles and preventive follow-up.

## 3. Initial asset coverage

- **Roads:** resurfacing, pothole repair, inspections, recorded defect-liability dates
- **Stormwater drainage:** desilting/cleaning, blockage reports, next due date
- **Streetlights:** installation and component replacements, fault reports, inspections

## 4. Platform roles

**Citizen portal:** View public asset records, search via a map, submit defects with photos.

**Worker portal:** Log maintenance work, attach supporting evidence, submit for review.

**Authority portal:** Check evidence, approve/reject updates, view overdue work, review reports and warranty flags.

## 5. Key innovation

**Digital Infrastructure Passport** — one enduring service history for an asset.  

**Verification-based updates** — approval changes the publicly displayed last-maintained date while preserving earlier entries in an audit trail.  

**Preventive alerts** — automated date-based warnings on scheduled work.  

**WarrantyGuard** — identifies a reported defect that may warrant checking the contractor's recorded obligations, without asserting liability.

The novelty claim is the proposed integration and user experience, not the assertion that no government software currently tracks maintenance.

## 6. Example demonstration (fictional)

Asset: **Navalur Stormwater Drain — DR-104**  
Last maintenance: **15 June 2026**  
Scheduled cleaning due: **15 September 2026**  
Citizen blockage reports: **8**

The system highlights the overdue date and reports. An official assigns work, a maintenance worker submits evidence, and an authorized reviewer approves it. The verified maintenance record is then appended and the last-maintained field updates. The next service date follows the chosen schedule.

All demonstration values must be labelled sample data.

## 7. Feasible 24-hour MVP

Build a web application with **10–20 simulated asset records**, map pins, asset detail pages, citizen reports, maintenance entry forms, approval status, historical records, and overdue/warranty flags. A trained AI prediction model is **outside** the core MVP; scheduling and alerts will be rule-based.

## 8. Expected value

**Citizens:** Access to clearer maintenance records and reporting channels.  
**Authorities:** Better visibility into overdue work, repeated problems, and verified maintenance history.  
**Public funds:** Better information when reviewing repeat repairs and recorded warranty periods.

These are expected benefits to be evaluated after testing, not measured outcomes of the current proposal.

## 9. Practical constraints

- Real records require municipal collaboration, imports, and permission.
- Photo/location evidence is imperfect and can be manipulated.
- Role-based data access and moderation are needed to protect privacy.
- Not every asset has a fixed maintenance interval or a warranty.
- Dates, costs, and contractor responsibility must not be fabricated as real municipal facts.

## 10. Closing vision

**A smarter city is not only one that builds more, but one that maintains better.**

*Every Asset. Every Repair. Complete Accountability.*
