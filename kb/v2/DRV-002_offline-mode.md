---
id: DRV-002
title: Using the driver app offline
last_reviewed: 2026-11-02
owner: Driver app team
---

# Using the driver app offline

Drivers often lose mobile signal in underground car parks, large buildings or rural areas. The Kerbloop driver app keeps working without a connection.

## What works offline
- Viewing the route, the stop list and all stop details.
- Marking stops as delivered or not delivered.
- Collecting proof of delivery: signatures, photos and recipient names.
- Scanning parcels.

## What does not work offline
- Live navigation with traffic. The app falls back to the last downloaded route line.
- Calling the customer through the app.
- Receiving changes from the dispatcher, such as new or moved stops.
- Updating the customer's tracking page and arrival time.

## How long a route is stored
When a route is started, the app downloads it to the phone. The stored route stays available offline for **48 hours** after it was downloaded. After that, the driver must connect to the internet once to keep working.

## Syncing
As soon as the phone is online again, the app sends all saved deliveries, photos and signatures to Kerbloop. This usually takes less than a minute. A cloud icon with a number at the top of the screen shows how many updates are still waiting to be sent.

Drivers should not log out while updates are waiting. Logging out deletes updates that have not been sent yet.

## Tip for dispatchers
If a driver's position stops moving on the live map, they may be offline. Check the **Last sync** time on the driver card before calling the driver.

Related: DRV-003 Scanning parcels, TW-005 How estimated arrival times are calculated.
