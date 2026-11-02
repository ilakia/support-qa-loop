---
id: DRV-003
title: Scanning parcels in the driver app
last_reviewed: 2026-08-19
owner: Driver app team
---

# Scanning parcels in the driver app

Scanning makes sure the right parcel is loaded into the right vehicle and handed to the right customer. The driver app uses the phone camera to scan barcodes and QR codes.

## When to scan
- **Loading at the depot**: the driver taps **Load vehicle** and scans every parcel. Parcels that belong to another route trigger a red warning "Wrong route".
- **At the stop**: before marking a stop as delivered, the driver scans the parcel. If the code belongs to a different stop, the app shows "Parcel belongs to stop X".

## Supported codes
Code 128, EAN-13, DataMatrix and QR codes. The parcel code must match the **Parcel ID** saved on the stop.

## The scan does not work
- Clean the camera lens and hold the phone 15 to 30 cm from the label.
- Turn on the flashlight with the torch icon in poor light.
- If the label is damaged, tap **Enter code by hand** and type the parcel ID.

Manually entered codes are marked "manual" in reports, so dispatchers can see how often labels are unreadable.

## Missing parcels
If a parcel on the route was not scanned during loading, the stop shows a warning icon. The driver can still deliver it, but the dispatcher sees it in the **Load check** report.

## Bluetooth scanners
Admins can allow external Bluetooth ring scanners under **Settings > Driver app**. Pair the scanner in the phone's Bluetooth settings, then select it in the app under **Menu > Scanner**.

Related: DRV-002 Using the driver app offline, FD-004 Proof of delivery.
