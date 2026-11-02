---
id: ADR-006
title: Importing stops from a file
last_reviewed: 2026-11-02
owner: Addresses team
---

# Importing stops from a file

If you have many deliveries, you do not need to create every stop by hand. You can import all stops for a day from a CSV or Excel file.

## Steps
1. In the web planner, go to **Stops > Import**.
2. Click **Download template** the first time, so your file has the right columns.
3. Fill in one row per stop and save the file as CSV or Excel (XLSX).
4. Click **Upload file** and choose the delivery date.
5. Check the preview and click **Import stops**.

## Columns in the template
- Required: **Street and house number**, **Postcode**, **City**, **Recipient name**.
- Optional: phone number, parcel ID, time window start and end, floor, apartment / unit, notes for driver.

Use the apartment and floor columns instead of the notes column, so the details show up clearly in the driver app (see ADR-003).

## Limits
- Up to 2,000 stops per file.
- One file per delivery date.

## After the import
Every imported address goes through the same checks as a stop entered by hand. Stops with problems are not lost: they are listed under **Stops > Needs attention**, where you can fix them one by one (see ADR-004).

## Who can do this
Dispatchers and Admins.

Related: ADR-001 Entering a delivery address, ADR-004 Address validation errors.
