---
id: ADR-003
title: Adding apartment, floor and building details
last_reviewed: 2026-08-30
owner: Addresses team
---

# Adding apartment, floor and building details

Large buildings slow drivers down when they have to search for the right door. Kerbloop has separate fields for these details so they show up clearly in the driver app.

## Fields on a stop
- **Building / entrance**: for example "Building C" or "Entrance via courtyard".
- **Floor**: a number, with 0 for the ground floor.
- **Apartment / unit**: for example "4B".
- **Lift available**: yes or no. Drivers use this to plan heavy deliveries.

You find these fields under **Stops > (stop) > Address details**.

## Why not use the notes field?
The driver app shows the address detail fields in large text at the top of the stop screen. The **Notes for driver** field is shown further down and is easy to miss. Floor and apartment in the notes field also cannot be used for filters or reports.

## Customers can add details too
If tracking links are enabled, the customer can add the floor, apartment and a delivery note on the tracking page until the driver starts the stop. Their changes are marked "added by customer" in the web planner.

## Limits
- Apartment / unit: up to 20 characters.
- Building / entrance: up to 60 characters.

Related: ADR-001 Entering a delivery address.
