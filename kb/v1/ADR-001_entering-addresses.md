---
id: ADR-001
title: Entering a delivery address
last_reviewed: 2026-09-14
owner: Addresses team
---

# Entering a delivery address

Dispatchers add delivery addresses in the Kerbloop web planner, under **Stops > New stop**.

## Steps
1. Click **New stop**.
2. Start typing the street and house number in the **Address** field. Kerbloop suggests matching addresses after three characters.
3. Pick the correct suggestion from the list. The postcode, city and map pin are filled in automatically.
4. Add the recipient name and a phone number. The phone number is used for the tracking link SMS and lets the driver call the customer.
5. Click **Save stop**.

## Tips
- Always pick a suggestion instead of typing the full address by hand. Hand-typed addresses are not geocoded and get a grey pin with the warning "Location not confirmed".
- Use the **Notes for driver** field for gate codes or where to leave the parcel. Do not put the apartment number there; use the apartment fields instead (see ADR-003).
- If an address is not in the suggestion list, for example a new building, type it fully and then place the pin on the map yourself (see ADR-002).

## Who can do this
Users with the **Dispatcher** or **Admin** role. Drivers cannot create stops in the driver app.

Related: ADR-002 Fixing a wrong map pin, ADR-004 Address validation errors.
