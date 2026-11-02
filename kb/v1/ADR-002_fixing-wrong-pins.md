---
id: ADR-002
title: Fixing a wrong map pin
last_reviewed: 2026-09-14
owner: Addresses team
---

# Fixing a wrong map pin

Sometimes the map pin for a stop is in the wrong place, for example at the back entrance of a large building or in the middle of a new housing estate. A wrong pin sends the driver to the wrong spot and makes the route longer.

## How to move a pin
1. In the web planner, open the stop under **Stops**.
2. Click **Edit location**.
3. Drag the pin to the correct entrance, or click on the map where the pin should be.
4. Click **Save location**.

The route is recalculated within about one minute. If the route is already started, the driver sees the new location after the app syncs.

## Remember the fix
Tick **Remember this location for this address** before saving. Next time anyone enters the same address, Kerbloop uses your corrected pin instead of the geocoded one. Remembered locations are shared across your whole company account.

## When drivers report a wrong pin
Drivers cannot move pins themselves. In the driver app they can tap **Report location problem** on the stop. The report appears in the web planner as an orange flag on the stop, so a dispatcher can fix it.

## Grey pins
A grey pin means the address was not confirmed by the map service. Check the address and place the pin by hand before you plan the route.

Related: ADR-001 Entering a delivery address.
