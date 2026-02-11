# Inventory Management & Asset Tracking

A comprehensive A-Z textbook on inventory management and asset tracking — from stockroom basics to enterprise-scale systems. Written in simple language with real-world examples, Indian context, and a running case study (Nadia's Spice Shop) that grows from a home kitchen to a multi-channel business.

## What's Inside

### Part I: Foundations
- **Chapter 1** — What is inventory (raw materials, WIP, finished goods, MRO), inventory vs assets, holding costs
- **Chapter 2** — SKUs, barcodes (UPC, QR, Data Matrix), RFID, NFC, BLE, GPS, IoT sensors
- **Chapter 3** — Inventory valuation methods (FIFO, LIFO, Weighted Average, Specific Identification, FEFO)
- **Chapter 4** — ABC analysis with step-by-step worked example

### Part II: Core Techniques
- **Chapter 5** — Demand forecasting (moving average, exponential smoothing, seasonal decomposition, accuracy metrics)
- **Chapter 6** — Reorder points, safety stock formulas, Economic Order Quantity (EOQ), Min/Max systems
- **Chapter 7** — Inventory counting (full physical count vs cycle counting), accuracy metrics, root cause analysis

### Part III: Warehouse Operations
- **Chapter 8** — Warehouse layout, storage systems, bin addressing, slotting optimization, the golden zone
- **Chapter 9** — Receiving, putaway, picking methods (discrete, batch, zone, wave), packing, shipping

### Part IV: Asset Tracking & Lifecycle
- **Chapter 10** — Full asset lifecycle (planning → procurement → deployment → maintenance → depreciation → disposal), TCO, Indian IT Act depreciation rates, maintenance types

### Part V: The Real World — Industry Examples & Day-in-the-Life
- **Chapter 11** — A day in the life: Flipkart warehouse worker, kirana store manager, IT asset manager in Bengaluru
- **Chapter 12** — Industry-specific inventory in India: retail (DMart, Blinkit), manufacturing (Maruti, Haldiram's), healthcare (Apollo), agriculture, pharma
- **Chapter 13** — A day in the life of a warehouse worker at an Indian 3PL (Delhivery, Bhiwandi)

### Part VI: E-Commerce & Modern Models
- **Chapter 14** — E-commerce inventory in India: self-fulfillment, FBA, 3PL, dropshipping, multi-channel sync, COD/RTO challenges

### Part VII: Modern Technology & the Future
- **Chapter 15** — AI-powered forecasting, warehouse robots, IoT sensors, blockchain traceability, digital twins

### Part VIII: Putting It All Together
- **Chapter 16** — Step-by-step guide to building your inventory system (with Indian tool recommendations: Tally, Vyapar, Zoho, ERPNext)
- **Chapter 17** — 8 common mistakes and how to avoid them
- **Chapter 18** — Nadia's complete journey from home kitchen to multi-channel business

Plus: **interactive tools**, **software walkthrough** (ERPNext, Tally Prime, Google Sheets), full **glossary**, and **further reading**.

## Interactive Calculators

Practice the concepts hands-on with browser-based tools (no installation needed):

| Tool | What it does | File |
|------|-------------|------|
| **EOQ Calculator** | Find the optimal order quantity that minimises total cost | [`tools/eoq-calculator.html`](tools/eoq-calculator.html) |
| **Safety Stock Calculator** | Calculate buffer stock and reorder point from demand variability | [`tools/safety-stock-calculator.html`](tools/safety-stock-calculator.html) |
| **Reorder Point Calculator** | Know exactly when to place your next order | [`tools/reorder-point-calculator.html`](tools/reorder-point-calculator.html) |
| **ABC Analysis Tool** | Classify products into A/B/C tiers with charts | [`tools/abc-analysis.html`](tools/abc-analysis.html) |

Each tool is a single self-contained HTML file — open it in any browser. Uses ₹ (Indian Rupee) formatting and works on mobile.

## Visual Diagrams

The textbook includes **Mermaid diagrams** that render as colourful visual flowcharts on GitHub:
- Inventory types flow (raw materials → WIP → finished goods → customer)
- Warehouse goods flow (receiving → storage → pick → pack → ship)
- Asset lifecycle (plan → buy → tag → deploy → maintain → depreciate → dispose)
- E-commerce fulfillment models
- Demand forecasting decision tree
- FIFO vs LIFO comparison

## Running Case Study: Nadia's Spice Shop

Every chapter ends with Nadia's story — showing how a real business applies each concept as it grows from 15 products in a spare room to 60+ products in a warehouse with 8 employees.

## Real-World Examples

The guide includes Indian and global examples from: Flipkart, Amazon, DMart, Reliance Retail, Maruti Suzuki, Haldiram's, Apollo Hospitals, BigBasket, Blinkit, Delhivery, Meesho, Amul, Indian Railways, Toyota, Zara, IKEA, Ocado, Boeing, and more.

## Who This Is For

- Anyone entering supply chain, logistics, or operations
- Business owners setting up inventory systems for the first time
- Students studying operations management or supply chain
- Engineers building inventory or asset tracking software
- Anyone who wants a single, beginner-friendly reference covering the full domain

## Further Reading

- *The Goal* — Eliyahu Goldratt
- *Toyota Production System* — Taiichi Ohno
- *Inventory Management Explained* — David J. Piasecki

**Free tools to practice with:** ERPNext (Indian, open-source, GST-ready), Odoo, Snipe-IT, Tally Prime (free trial)

## Software Walkthrough

The textbook includes a hands-on appendix covering:
- **ERPNext** — step-by-step: create items, set reorder points, receive stock, process sales orders, check stock reports
- **Tally Prime** — enable inventory, create stock items, record purchases/sales, check stock summaries
- **Google Sheets** — inventory tracker template with formulas for reorder alerts, days-of-stock, and turnover
