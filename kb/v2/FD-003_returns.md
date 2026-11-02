---
id: FD-003
title: Returning parcels to the depot and sender
last_reviewed: 2026-09-08
owner: Failed deliveries team
---

# Returning parcels to the depot and sender

When a parcel cannot be delivered, it goes back to the depot. From there it is either kept for collection or sent back to the sender.

## Marked "Return to depot"
A parcel is marked **Return to depot** after the last failed attempt, or straight away for reasons like **Refused by customer** (see FD-002). The driver keeps the parcel in the vehicle and brings it back at the end of the route.

## Checking in at the depot
At the depot, staff scan the parcel in the web planner under **Depot > Returns check-in**. The parcel status changes to **At depot**. Parcels that were marked for return but not scanned in by the end of the day appear in the **Missing returns** list.

## Customer collection
If **Collection at depot** is on, the customer can pick up the parcel at the depot for 7 days. The customer gets an SMS with the depot address and opening hours. Depot staff mark the parcel **Collected** when it is handed over.

## Return to sender
After the collection period, or right away if collection is off, the parcel status changes to **Return to sender**. Kerbloop adds it to the sender's return list, which you can export under **Reports > Returns** (see ACC-004).

## Customer questions about refunds
Kerbloop does not handle refunds or payments for the goods in a parcel. Customers must contact the shop they ordered from.

Related: FD-002 Retry rules, ACC-004 Exporting reports.
