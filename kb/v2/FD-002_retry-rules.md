---
id: FD-002
title: Retry rules for failed deliveries
last_reviewed: 2026-11-02
owner: Failed deliveries team
---

# Retry rules for failed deliveries

When a delivery fails, Kerbloop decides automatically whether and when to try again. Admins can adjust some of these rules.

## Default rules
- A parcel is attempted **up to 3 times in total**: the first attempt and two retries.
- The retry is planned for the **next working day**. Saturdays count as working days only if your depot delivers on Saturdays.
- The retry keeps the original time window, unless the customer picks a new one on the tracking page.
- If the third attempt also fails, the parcel is marked **Return to depot** (see FD-003).

## Reasons that skip the retry
Some failure reasons go straight to **Return to depot** without a retry, because trying again would not help:
- **Refused by customer**
- **Address does not exist**
- **Parcel damaged**

## Changing the rules
Admins can change the retry day under **Settings > Delivery options > Retries**, for example to retry on the same day in the evening. The total number of attempts cannot be changed.

## Manual retries
A dispatcher can always plan an extra attempt by hand. Open the stop, click **Plan again** and choose a date. Manual attempts are marked "manual" in reports.

Related: FD-001 When the customer is not home, FD-005 Failed delivery reasons.
