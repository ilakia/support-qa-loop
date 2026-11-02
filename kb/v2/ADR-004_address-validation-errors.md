---
id: ADR-004
title: Address validation errors
last_reviewed: 2026-09-02
owner: Addresses team
---

# Address validation errors

When you save a stop, Kerbloop checks the address. If the check fails, the stop is saved but marked with a red warning and cannot be added to a route until the problem is solved.

## Common messages and what to do

**"Postcode does not match city"**
The postcode and city belong to different places. Check both against the customer's details and correct the wrong one.

**"House number not found"**
The street exists, but the map service does not know this house number. This is common for new buildings. Check the number with the customer, then place the pin by hand (see ADR-002).

**"Address outside service area"**
The address is outside the delivery area set for your depot. An Admin can change the service area under **Settings > Depots**. Dispatchers cannot change it.

**"Duplicate stop"**
A stop with the same address and recipient already exists on the same day. Open both stops and delete one, or merge them with **Merge stops**.

**"Location not confirmed"** (grey pin)
The address was typed by hand and not picked from the suggestions. Pick a suggestion or place the pin yourself.

## Stops from file imports
Stops imported from a file go through the same checks. All stops with errors are listed under **Stops > Needs attention**, so you can fix them in one place.

Related: ADR-001 Entering a delivery address, ADR-002 Fixing a wrong map pin.
