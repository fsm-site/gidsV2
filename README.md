# GIDS IPHONE REPAIR — Dashboard

Copyright (c) 2026 GIDS IPHONE REPAIR. All rights reserved.

GIDS is a browser-based repair-shop dashboard with a polished glass
interface, local data storage, optional Firebase sync, and installable app
support. Everything below marked **EDIT ME** is a placeholder — open
`index.html` in a text editor and search for "EDIT ME" to find every spot to
customize.

## Purpose

GIDS IPHONE REPAIR is designed to help a phone-repair business manage its
day-to-day work in one place. It replaces scattered notebooks and spreadsheets
with a simple workspace for recording repairs, checking prices and inventory,
tracking revenue, and giving customers a clear repair-status experience.

It is suitable for an owner, manager, or repair-shop team that needs a
lightweight system that can run locally on a computer, tablet, or phone. It is
not a replacement for a full accounting system, payment processor, SMS
provider, or enterprise authentication service.

## How the website works

1. **Open the dashboard** — start the local server and open the localhost URL.
   The app loads immediately and saves changes in the browser.
2. **Staff access** — staff unlock the work dashboard with the staff password.
   They can record repair jobs, appointments, parts used, payments, and
   customer details.
3. **Admin access** — the owner or manager signs in to the Admin panel to
   review sales, manage inventory, update prices, view reports, manage
   suppliers, and change the admin password.
4. **Record a repair** — choose the branch, technician, phone model, service,
   customer, payment method, and status. The dashboard updates totals,
   inventory usage, job history, and receipt information.
5. **Serve the customer** — use the public price list or Customer Status
   Portal to look up a repair using a service/receipt number or phone number.
   Customers can view progress and use digital receipt, print, copy, share, or
   PDF actions.
6. **Review and export** — use analytics for quick business performance
   metrics, then export reports or purchase orders when needed.

## Main areas

- **Dashboard** — daily jobs, sales, branch selection, technician activity,
  appointments, and quick actions.
- **Public inventory** — customer-facing parts and labor pricing without admin
  editing access.
- **Admin panel** — overview KPIs, operations, inventory, suppliers,
  stock-movement history, reports, and account settings.
- **Customer Status** — a customer-friendly repair lookup and receipt view.
- **Calculator** — quick pricing calculations without leaving the dashboard.

## Complete feature guide

### Dashboard and branch controls

The dashboard is the main daily workspace. Select a branch from the top bar to
view branch-specific work and sales. Summary cards show important numbers such
as jobs, sales, inventory value, and low-stock items. Quick actions reduce the
number of clicks needed to log a repair or open the calculator.

The dashboard includes technician sales summaries and recent activity. This
helps an owner compare workload between Downtown, Northside, or any custom
branches configured in the source code.

### Repair jobs and appointments

Staff can create a repair record with the customer name, phone number, device
brand/model, repair type, technician, branch, parts, labor, payment method,
price, notes, and status. Job statuses make progress visible from intake to
completion:

- **Pending** — the repair has been received but work has not started.
- **In progress** — a technician is currently working on the device.
- **Ready** — the repair is complete and ready for customer pickup.
- **Completed** — the customer has received the device and payment is settled.
- **Cancelled** — the job will not be completed.

Appointments can be scheduled for future customers and reviewed by staff from
the operations area. Customer phone numbers connect related work so the team
can review a customer's previous repairs and service history.

### Customers, receipts, and invoices

Every logged job receives a service/receipt number. The receipt records the
customer, device, selected services, parts, labor, total amount, payment mode,
technician, branch, and date. Receipts can be printed or exported as PDF.

The invoice/payment view helps staff see whether a job is paid, pending, or
requires follow-up. The customer history view groups previous jobs by phone
number so repeat customers can be served faster.

### Public price list

The public inventory view is intended for a customer-facing screen or shared
link. It shows available parts, accessories, and labor pricing without exposing
admin editing controls. Staff can switch between parts and labor summaries
before quoting a repair.

### Customer Status Portal

Customers do not need admin access to check a repair. They can search using a
service/receipt number or phone number and see the matching device, repair
status, date, amount, and receipt details. Depending on browser support, the
receipt can be copied, shared through the device share sheet, printed, or
downloaded as a PDF.

The portal is designed for in-store use or for sending a customer the local
dashboard address. For public internet access, configure a proper hosted
backend and authentication before exposing customer information.

### Inventory management

Admin inventory records support:

- Item name, quantity, cost, selling price, and used quantity
- SKU or barcode-friendly identifier
- Supplier name and storage location
- Reorder level and low-stock warning
- Parts versus labor grouping
- Search and quick stock adjustments

Stock movements provide a simple audit trail for stock received, used,
returned, or manually adjusted. Low-stock items appear in the dashboard and
can be turned into a purchase-order CSV for sending to a supplier or opening in
a spreadsheet.

### Suppliers and purchase orders

The supplier directory keeps supplier names, contact details, and notes near
the inventory tools. When stock reaches its reorder level, the purchase-order
generator prepares a CSV containing the low-stock items, quantities, prices,
and supplier-related information. The CSV can be edited before sending to a
supplier.

### Analytics and reports

The analytics area calculates business metrics from recorded jobs, including:

- Gross sales and job count
- Average ticket value
- Completed versus open jobs
- Completion rate
- Top service or repair type
- Technician activity and sales
- Seven-day sales trend

Reports can be filtered by branch and date context, then exported for
bookkeeping or management review. Excel and PDF exports are generated in the
browser using the included report libraries.

### Calculator

The built-in calculator is useful for quickly adding labor, parts, discounts,
or customer quotes without leaving the dashboard. It does not automatically
charge a payment method or connect to a bank or e-wallet.

### Admin and staff access

Staff access protects the operational dashboard. Admin access protects
inventory editing, reports, account settings, and other management tools.
Admin users can change the admin password from the Admin panel. Login fields
are intentionally empty when the app opens so credentials are not displayed
or prefilled.

This access control is implemented in the browser and is appropriate for a
local/private tool, not for high-security production authentication. Use a
backend identity provider and server-side permissions for a multi-location
business or internet-facing deployment.

## Typical daily workflow

1. Start the local server and open the dashboard.
2. Staff unlock the dashboard and select the correct branch.
3. Check today's appointments and pending repairs.
4. Add a new customer and repair job, or locate the customer's history.
5. Select the technician, device, service, parts, price, and payment method.
6. Update the status as work progresses.
7. Print or share the receipt when the repair is ready.
8. Review sales, technician totals, and low-stock alerts before closing.
9. Adjust inventory and export a purchase order for items that need restocking.
10. Use reports for owner review and bookkeeping.

## Customization for a buyer

The buyer can adapt the included dashboard without rebuilding a framework:

- Change `BIZ_NAME` and `BIZ_LOCATION` for the shop identity.
- Replace `BRANCHES` with the actual branch list.
- Replace `TECHS` with the staff/technician list.
- Update phone models, service types, payment modes, and initial inventory.
- Change the default passwords before entering real data.
- Add a Firebase project when multiple devices need shared records.
- Replace the included SVG icon with the business logo if desired.

Keep the app's data structure consistent when editing the source. Make a
backup of the browser data or Firebase document before making large changes.

## Ownership and credits

This customized app is branded **GIDS IPHONE REPAIR**. Add the technicians to
the `TECHS` list in `index.html` when their names are confirmed. Their names
will then appear in repair-job forms and technician reports.

## Copyright

Copyright (c) 2026 GIDS IPHONE REPAIR. All rights reserved. The GIDS
IPHONE REPAIR name, branding, interface design, source code, documentation,
icons, and included application assets are proprietary to the owner unless a
separate written license says otherwise. Buyers may use the delivered app for
their purchased business use, but may not copy, resell, redistribute, or
rebrand the application for third parties without the owner's permission.

## Where data is stored

By default, data is stored in the browser's local storage on the device being
used. This means the app works without an internet connection after it has
loaded, but data is not automatically shared with other devices. For shared
multi-device data, connect your own Firebase Firestore project and configure
the security rules for your business.

## Before you use it

1. **Set your business info** — search for `BIZ_NAME` / `BIZ_LOCATION`,
   `BRANCHES`, and `TECHS` near the top of the `<script>` block and change
   them to your real shop name, address, branches and technicians.

2. **Connect your own Firebase project (optional but recommended)** —
   the original file shipped with a *real, live* Firebase project and
   plaintext admin/staff passwords baked into the code. That's been
   stripped out for safety — reusing someone else's project would let
   this new copy read and write straight into their live business data.
   To wire up sync across devices:
   - Go to https://console.firebase.google.com and create a project
   - Add a Web App, enable Firestore (test mode is fine to start)
   - Copy your config object into the `firebaseConfig` block
   - If you skip this step, the app still works fully — it just saves
     to that browser's local storage only, instead of syncing to the cloud.

3. **Use the updated access credentials** — staff access uses `SAGids`.
   Admin access accepts either `adminjaja` or `admintristan`, both using
   `162022gids`. Change the admin password from the Admin panel before putting
   this in front of real staff. The login fields are intentionally blank.

## Quick start on Windows

1. Open the Windows **Start** menu, search for **PowerShell**, and open it.
2. Copy and run these commands:

```powershell
cd "C:\Users\iamde\OneDrive\Desktop\GIDS\GIDS"
.\start-localhost.cmd
```

3. Open Chrome or Edge and visit **http://gidsayphonetech:4173**.
   If that name does not open yet, use **http://localhost:4173**.
4. Use the dashboard. The app opens immediately; no separate download or
   installer is required.

## Open it on an Android phone or iPhone

The phone and the Windows computer must be connected to the same Wi-Fi network.

1. Start the server using the Windows steps above.
2. Look in PowerShell for the line **On another device**, for example:
   `http://192.168.1.25:4173`.
3. On the phone, open that address in Chrome (Android) or Safari (iPhone).
4. If the phone cannot connect, allow Python through Windows Defender Firewall
   on private networks and confirm both devices are on the same Wi-Fi.

On Android, use Chrome's menu and choose **Add to home screen** or **Install
app**. On iPhone, use Safari's **Share** button and choose **Add to Home
Screen**. The Windows server must remain running while the phone uses the app.

## Run locally

Do not open the HTML file directly if you want offline caching or app
installation. In PowerShell, run:

```powershell
.\start-localhost.cmd
```

Then open http://gidsayphonetech:4173. The browser will offer an **Install app**
button when PWA installation is supported. Data remains in local storage unless
you configure Firebase.

Keep the PowerShell window open while using the app. Press **Ctrl+C** to stop
the local server.

If PowerShell blocks the script, run the server directly instead:

```powershell
cd "C:\Users\iamde\OneDrive\Desktop\GIDS\GIDS"
& "C:\Users\iamde\.local\bin\python3.14.exe" -m http.server 4173
```

If port `4173` is already in use, open the existing
http://gidsayphonetech:4173 page. Otherwise, stop the other local server and run
the command again.

## Install as a Windows app

1. Start the local server using the steps above.
2. Open http://gidsayphonetech:4173 in Chrome or Edge.
3. Click **Install app**, or use the install icon in the browser address bar.
4. Launch **GIDS IPHONE REPAIR** from the Windows Start menu.

The installable app is defined by `app.webmanifest`, uses `gd2.png` as its
current dark app icon,
and caches its shell with `sw.js` for a faster repeat launch. Browser support
and install prompts vary by browser.

### Opening the installed app later

After installation, search for **GIDS IPHONE REPAIR** in the Windows Start menu
and open it like any other app. The local server must still be running. If the
app cannot connect, start PowerShell again and run:

```powershell
cd "C:\Users\iamde\OneDrive\Desktop\GIDS\GIDS"
.\start-localhost.cmd
```

### First login

The login fields are blank on purpose. For this demo, the initial admin
the initial staff password is `SAGids`. Admin access accepts the usernames
`adminjaja` and `admintristan`, both with password `162022gids`. Change the
admin password immediately from the Admin panel before using real business or
customer information.

### Remembering a login

Both the Admin Login and Staff Access screens include **Remember me on this
device**, enabled by default. After a successful login, the app remembers the
access level in that browser so the next time the installed app opens it can
return directly to the dashboard. This is device/browser-specific and does not
share credentials with other devices.

Use **Log out** from the Admin panel when the device is shared or when you want
to remove the remembered session. Clearing the browser's site data also removes
the remembered session.

## What's new vs. the original

- **Low-stock alert banner** on the Inventory tab, and a "Low-stock items"
  stat card on the Overview tab (tap it to jump straight to Inventory).
  Flags anything at or below its configured reorder level (3 by default).
- **Search box on the Jobs table** — filter logged jobs by tech, customer,
  service, phone, or payment method without leaving the page.
- **Search box on the Inventory table** — quickly find a part by name.
- **Business operations workspace** — schedule appointments, track job status,
  group customer history, and review invoice/payment state from the Admin
  Operations tab.
- **Dashboard analytics** — average ticket, completion rate, open-job count,
  top service, and a seven-day sales trend are calculated from local jobs.
- **Inventory controls** — a supplier directory, SKU/barcode, reorder level and
  location fields; a recent stock-movement ledger; and a low-stock
  purchase-order CSV generator.
- **Customer status portal** — customers can look up a service/receipt number
  or phone, view repair status, and use digital receipt copy, share, print and
  PDF actions without admin access.
- **Local-storage fallback** — if Firebase isn't configured (or is
  unreachable), the app now keeps working off the browser's local storage
  instead of failing.
- **Glassy dark workspace** — translucent panels, soft blue accents, and a
  dark navy background improve focus and reduce glare.
- **No startup splash animation** — the dashboard opens immediately.
- **Installable PWA** — use the dashboard like a standalone desktop or mobile
  app.
- Sensitive data removed: the original file's live Firebase credentials were
  replaced with placeholders. Login fields are blank and credentials are not
  displayed in the interface.

## Everything else

Same structure as the original: employee view, public price list, admin
login/panel (overview, inventory, reports), transaction logging, receipt
printing, and Excel/PDF report export.

## Important security note

This is a client-side dashboard. Local passwords are stored in browser
storage and should not be treated as production-grade authentication. If the
dashboard will be used by multiple people or exposed beyond your local
network, add a proper backend authentication layer and configure Firebase
Security Rules before storing real customer or business data.
