---
id: TW-002
title: Changing a time window
last_reviewed: 2026-09-20
owner: Time windows team
---

# Changing a time window

Customers sometimes ask for a different delivery time after the stop is created. How you change the window depends on whether the route has started.

## Before the route is started
1. Open the stop in the web planner.
2. Change the start and end time under **Time window**.
3. Click **Save stop**.
4. Click **Re-optimise route** so Kerbloop can find the best new order of stops.

## After the route is started
You can still change the window, but Kerbloop does not reorder the stops automatically, because the driver is already on the road.
1. Change the time window and save the stop.
2. Kerbloop shows the new estimated arrival time. If it falls outside the new window, the stop is marked in red.
3. Use **Move stop** to place the stop earlier or later in the route by hand.
4. The driver gets a notification in the driver app that the order has changed.

## Changes by the customer
If tracking links are enabled, customers can pick a new window on the tracking page from the options you allow (see TW-004). These changes follow the same rules as above.

## What updates automatically
When a window changes, the customer's tracking page and the estimated arrival time are updated within about one minute. If SMS notifications are on, the customer gets a new message with the updated time.

Related: TW-001 Setting a delivery time window, TW-004 Letting customers choose a time window.
