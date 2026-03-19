# SOP: Inventory Management — Medical Esthetics Thunder Bay

> Last updated: 2026-03-19

---

## Purpose
To maintain accurate, real-time inventory levels that prevent stockouts of critical items, eliminate dead stock waste, and support smart purchasing decisions.

---

## Core Principles
- Never run out of consumables for high-revenue devices.
- Injectables must be tracked by expiry date — FIFO (first in, first out).
- Retail products should have a clear reorder point, not guesswork.
- Inventory counts inform purchasing; purchasing drives revenue. Treat inventory as a financial system.

---

## Inventory Categories
1. Device consumables (single-use tips, cartridges, applicators, etc.)
2. Injectables (toxins, fillers, PRP supplies)
3. Skincare retail products
4. Supplements and wellness products
5. Treatment consumables (gauze, gloves, numbing cream, etc.)

---

## Step 1 — Add New Items to the Tracker
When a new product or consumable is introduced:
1. Open data/inventory.md.
2. Add the item to the correct table with: name, SKU/code, vendor, par level, reorder point.
3. Set par level = minimum acceptable stock before service quality is impacted.
4. Set reorder point = quantity at which an order must be placed (allows for lead time).

**Formula:**
> Reorder point = (average daily usage × vendor lead time in days) + safety stock

---

## Step 2 — Weekly Spot Checks
Every week, spot-check high-velocity and high-risk items:
- Device consumables for top-revenue treatments
- Injectables (toxins and top-selling fillers)
- Best-selling retail products

Update quantities in inventory.md. Flag anything at or below reorder point.

---

## Step 3 — Monthly Full Cycle Count
On the last Friday of each month:
1. Count every item in inventory against the tracker.
2. Update all quantities in inventory.md.
3. Flag discrepancies (count vs. tracker) and investigate.
4. Move any expired or near-expiry injectables to the Expiry Tracker.
5. Identify dead stock (no sales in 60+ days) and flag for action.
6. Update the Inventory KPIs section.

---

## Step 4 — Reordering
When an item hits its reorder point:
1. Create a reorder entry in the Reorder Tracker table in inventory.md.
2. Contact the vendor using the vendor-email-template.md restock template.
3. Log: item, quantity ordered, vendor, date ordered, expected ETA.
4. Follow up with vendor if no confirmation within 48 hours.
5. Update inventory.md when stock is received (mark "Received" and update quantity).

---

## Step 5 — Expiry Management
For all injectables and products with expiry dates:
- Use FIFO — always use older stock first.
- Flag anything within 60 days of expiry.
- For injectables: communicate with provider to prioritize use before expiry.
- For skincare retail: consider discount or bundle promotion to clear expiring items.
- Log any write-offs (expired, unusable items) in inventory.md with date and reason.

---

## Step 6 — Dead Stock Review
Quarterly, review all items with zero or near-zero sales in 60+ days:
- Is it priced correctly?
- Is it displayed / promoted?
- Can it be bundled with a fast-moving product?
- Should it be returned to vendor or discounted to clear?
- Should it be discontinued?

---

## Inventory KPI Targets

| Metric | Target |
|---|---|
| Inventory cost as % of revenue | < 20% |
| Stockouts per month | 0 for critical items |
| Expired write-offs per month | $0 target |
| Dead stock items | Review and clear quarterly |

---

## Accountability

| Role | Responsibility |
|---|---|
| [Owner / Manager] | Approve all orders over $[threshold] |
| [Admin / Operations] | Weekly spot checks and monthly cycle count |
| [Provider / Clinical] | Flag when treatment supplies are running low mid-day |
