---
id: TW-001
title: Setting a delivery time window
last_reviewed: 2026-09-20
owner: Time windows team
---

# Setting a delivery time window

A time window is the period in which the customer expects the delivery, for example 09:00–12:00. Kerbloop plans the route so that each stop is reached inside its window.

## Add a time window to a stop
1. In the web planner, open the stop under **Stops**.
2. In **Time window**, enter a start time and an end time.
3. Choose **Hard** or **Soft** (see below).
4. Click **Save stop**.

If you leave the time window empty, the stop can be delivered at any time during the driver's shift.

## Hard and soft windows
- **Hard window**: the stop must be reached inside the window. If this is not possible, Kerbloop does not plan the stop and shows it under **Unplanned stops** with the reason "Time window cannot be met".
- **Soft window**: Kerbloop tries to reach the stop in the window but may plan it later if that makes the whole route much shorter. Late stops are shown in orange.

## Rules
- The shortest time window is 30 minutes.
- A stop can have up to two windows on the same day, for example 08:00–10:00 and 16:00–18:00.
- Time windows use the time zone of the depot, not of the dispatcher's computer.

## Default windows
Admins can set a default time window for all new stops under **Settings > Planning defaults**.

Related: TW-002 Changing a time window, TW-003 Missed time windows.
