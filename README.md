# New Generation Auctions Catalog — Build 2

This is an iPhone-first installable web-app prototype.

Implemented:
- iPhone camera / photo picker with multiple photos per lot
- Sequential lot numbering
- Review/edit/approve workflow
- Catalog persistence on the device using localStorage
- CSV catalog export
- Installable PWA shell (manifest + service worker)
- Real `/api/analyze-lot` integration point for secure server-side AI photo analysis
- Honest fallback when the AI backend is not yet deployed

Next production pieces:
1. Deploy a secure backend for `/api/analyze-lot` and connect an image-capable AI model. Never expose the AI key in the browser.
2. Add authentication, cloud database, and object storage so multiple employees/iPhones share one auction.
3. Match the final CSV and image naming exactly to the user's HiBid/AuctionFlex import template.
4. Add conflict-safe lot number allocation on the server.

The current build does not pretend the AI backend exists: photo analysis requires deployment credentials and a server endpoint.
