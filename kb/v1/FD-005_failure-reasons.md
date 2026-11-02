---
id: FD-005
title: Failed delivery reasons
last_reviewed: 2026-09-08
owner: Failed deliveries team
---

# Failed delivery reasons

When a driver taps **Not delivered** in the driver app, they must choose a reason. The reason decides what happens to the parcel next and appears in reports.

## The reasons
| Reason | What happens next |
|---|---|
| Customer not home | Retry planned (see FD-001, FD-002) |
| No access to building | Retry planned |
| Wrong address | Stop flagged for the dispatcher to fix the address |
| Address does not exist | Return to depot |
| Refused by customer | Return to depot |
| Parcel damaged | Return to depot, photo required |
| Out of time | Retry planned, counted as a driver-side failure |

## Adding a note
For every reason, the driver can add a short note and a photo, for example a picture of a locked gate. Notes are shown to the dispatcher on the stop.

## Wrong address
If the driver chooses **Wrong address**, the stop appears in the web planner under **Stops > Needs attention**. The dispatcher corrects the address or pin (see ADR-002) and plans the stop again.

## Reports
The **Failed deliveries** report shows how many stops failed per reason, driver and area. A high number of "No access to building" in one area often means gate codes are missing from the driver notes.

Related: FD-002 Retry rules, ADR-002 Fixing a wrong map pin, ACC-004 Exporting reports.
