---
id: TW-005
title: How estimated arrival times are calculated
last_reviewed: 2026-09-20
owner: Time windows team
---

# How estimated arrival times are calculated

Kerbloop shows an estimated time of arrival (ETA) for every stop to dispatchers in the web planner and to customers on the tracking page.

## What the ETA is based on
- The planned order of stops in the route.
- Driving times from the map service, including typical traffic for that time of day.
- The **service time** for each stop: how long the driver needs at the door. The default is 3 minutes. Admins can change it under **Settings > Planning defaults**, and dispatchers can change it for single stops.
- The driver's live GPS position once the route has started.

## How often it updates
While a route is running, ETAs are updated every 2 minutes from the driver's position. If the driver app is offline, ETAs are not updated until the app reconnects.

## What customers see
Customers do not see the exact ETA. The tracking page shows a 30-minute arrival range, for example 10:15–10:45, until the driver is two stops away. Then the page shows "Your driver is on the way" and a live map.

## Why ETAs can be wrong
- Service times that are too short for large or heavy deliveries.
- Wrong map pins (see ADR-002).
- The driver delivering stops in a different order than planned.

Related: TW-003 Missed time windows, ADR-002 Fixing a wrong map pin.
