# Madhav Momos Billing – Updated PWA package

## Included in this revision
- Existing offline-first PWA and IndexedDB local data retained (same database name and object store).
- Product deletion with confirmation; past sales retain their saved line-item snapshots.
- Raw material add/edit/delete; deletion is blocked when an active recipe still uses the ingredient.
- Expenses Ledger with categories, amount, description and payment mode.
- Stock-in purchase amount creates one linked Raw Materials expense entry.
- GST disabled by default because the business is currently not GST registered. No GST is added to bills.
- 58mm receipt preview, browser print/save-to-PDF, and previous bill reprint.
- Experimental Web Bluetooth device chooser for compatible BLE devices only. It does not guarantee thermal printing; many low-cost 58mm printers use Bluetooth Classic and need a vendor Android app or native bridge.
- Existing products, recipes, stock, wastage, sales and backup/restore remain.

## Important limitations
- This package is still local-first. Firebase authentication, Firestore multi-device sync, secure business-scoped rules, offline sync outbox and cloud backup are NOT implemented in this ZIP. Firebase project configuration and security rules must be set up and tested before using two devices.
- GST return filing and compliance are not included. GST remains disabled.
- Sample recipe quantities and opening stock should be checked against actual business records.
- Before replacing the hosted app, download a JSON backup on the device containing the live data. Upload the extracted folder contents to the same HTTPS site and retain the same origin so the existing IndexedDB database remains accessible. Test on a backup first.

## Run locally
Serve this folder on localhost or HTTPS; do not open index.html directly from the file manager.
