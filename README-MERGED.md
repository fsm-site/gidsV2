# GIDS V2 — Merged Build

This build uses the expanded GIDS frontend from the newer copy while preserving the original production Firebase project and document.

## Preserved production infrastructure
- Firebase project: `gids-7d44c`
- Firestore document: `app-data/gids-tech-data`
- Original branches: San Antonio, Bataan, Angeles
- Original technicians: Tristan, Jaja, Peypey, Kakai
- Original payment modes: Cash, E-Wallet
- Original admin account structure/password is preserved when existing production data is loaded.

## Added features from the newer build
- Customer repair-status portal
- Customer history
- Job status and appointment tracking
- Invoice tracking
- Job/inventory search
- Supplier management
- SKU, location and reorder levels
- Low-stock alerts
- Stock movements
- Purchase-order export
- Dynamic technician management
- Analytics and sales trends
- Average ticket/completion/open-job/top-service KPIs
- Remembered session
- Improved PWA install flow

## Deployment
This package is intentionally frontend-only for GitHub/Vercel/Firebase hosting. The Flask/SQLite local backend from the source copy is not included because Firebase remains the production data source.

## Important
Before deploying over the live site, keep a backup/export of the current Firestore `app-data/gids-tech-data` document. The merged app includes schema migration for the new fields, but a backup is still recommended.
