---
id: DRV-001
title: Driver app login problems
last_reviewed: 2026-09-12
owner: Driver app team
---

# Driver app login problems

Drivers log in to the Kerbloop driver app with a **company code**, their **mobile number** and a **6-digit PIN**. The company code is the same for everyone in your company and is shown to Admins under **Settings > Company**.

## "Wrong PIN"
- Check that the mobile number is entered with the country code, for example +49.
- After 5 wrong PINs, the account is locked for 15 minutes.
- If the driver forgot the PIN, a dispatcher or Admin opens **Drivers > (driver) > Reset PIN**. The driver gets an SMS with a new temporary PIN and must choose a new one at the next login.

Drivers cannot reset their own PIN in the app.

## "Unknown company code"
The company code was typed wrong or the driver is using an old code. Codes are not case-sensitive. Ask an Admin for the current code.

## "Driver not active"
The driver's profile is switched off in the web planner. A dispatcher or Admin can switch it on under **Drivers > (driver) > Active**.

## "No route assigned"
The driver is logged in but has no route for today. This is not an error. The dispatcher must assign a route under **Routes**.

## The app does not open
Make sure the phone meets the requirements (see DRV-005) and the app is up to date. Removing and reinstalling the app does not delete any delivery data, because everything is saved on the server once the app has synced.

Related: DRV-005 Supported phones and app updates.
