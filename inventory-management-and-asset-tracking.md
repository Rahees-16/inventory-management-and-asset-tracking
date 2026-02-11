# Inventory Management & Asset Tracking: A Complete Guide

> From stockroom basics to enterprise-scale systems — with real-world examples throughout.

---

# PART I: FOUNDATIONS

---

## Chapter 1: What Is Inventory?

Inventory is any tangible resource a business holds to sell, use in production, or consume during operations. It is one of the most significant assets on a company's balance sheet and directly impacts cash flow, profitability, and customer satisfaction.

### 1.1 Why Inventory Exists

Every business faces a fundamental tension:

- **Customers want things immediately.** They don't want to wait.
- **Suppliers and production take time.** Raw materials must be sourced, goods must be manufactured, shipments must travel.

Inventory exists to bridge that gap. It acts as a buffer between supply and demand.

**Real-life example:**
A grocery store like Walmart doesn't wait for you to order milk before calling the dairy farm. They predict demand, stock shelves in advance, and replenish continuously. Without inventory, every purchase would take days or weeks.

### 1.2 Types of Inventory

#### Raw Materials
Items purchased to be transformed into finished products.

| Industry | Raw Material Examples |
|----------|---------------------|
| Bakery | Flour, sugar, eggs, butter |
| Auto manufacturer | Steel sheets, rubber, glass, wiring |
| Software company | Server hardware, cables (minimal) |
| Clothing brand | Fabric rolls, thread, buttons, zippers |

**Real-life example:**
Toyota purchases steel coils from suppliers like Nippon Steel. These coils sit in Toyota's raw materials inventory until they're stamped into car body panels.

#### Work-In-Progress (WIP)
Items that have started the production process but aren't finished yet.

**Real-life example:**
At a Boeing aircraft factory, a half-assembled 737 fuselage is WIP. The aluminum has been cut, shaped, and partially riveted, but it's not a plane yet. It can't be sold. It can't be returned to raw material. It sits in an expensive limbo.

WIP inventory is dangerous because:
- It ties up capital (you've already spent money on materials + labor)
- It can't generate revenue yet
- It takes up floor space
- It can become obsolete if designs change mid-production

#### Finished Goods
Completed products ready for sale or shipment.

**Real-life example:**
An iPhone sitting in Apple's warehouse in Zhengzhou, China, boxed with charger and documentation, ready to ship to retail stores worldwide — that's finished goods inventory.

#### MRO (Maintenance, Repair, and Operations)
Items consumed during operations but not part of the final product.

**Real-life example:**
A car factory uses thousands of welding tips per day. These tips wear out and must be replaced constantly. They're not part of the car — the customer never sees them — but without them, production stops. Other MRO items: lubricants, safety gloves, cleaning supplies, light bulbs, printer paper.

#### Packaging Materials
Boxes, labels, shrink wrap, pallets — anything used to package and ship finished goods.

**Real-life example:**
Amazon's fulfillment centers stock dozens of box sizes, air pillows, tape guns, and shipping labels. These are inventoried and tracked just like products, because running out of boxes is just as bad as running out of product.

### 1.3 Inventory vs. Assets

This distinction is critical and often confused:

| Characteristic | Inventory | Fixed Asset |
|---------------|-----------|-------------|
| Purpose | To be sold or consumed | To be used over time |
| Lifespan | Short (days to months) | Long (years) |
| Accounting | Current asset (balance sheet) | Non-current asset (depreciated) |
| Example | A laptop in Best Buy's stockroom | A laptop on an employee's desk |
| Tracking focus | Quantity, cost, turnover | Location, condition, depreciation |

**The same physical item can be either, depending on intent:**

- A Dell laptop in Dell's warehouse = **inventory** (they plan to sell it)
- A Dell laptop on your office desk = **fixed asset** (you plan to use it for years)
- A Dell laptop at a refurbishment shop = **inventory** (they'll resell it)

### 1.4 The Cost of Holding Inventory

Inventory is NOT free to hold. The total cost of holding inventory typically ranges from **20% to 35% of the inventory's value per year**.

#### Breakdown of Holding Costs:

```
Capital cost:         8-15%   (money tied up that could be invested elsewhere)
Storage cost:         2-5%    (warehouse rent, utilities, shelving)
Service cost:         1-3%    (insurance, taxes on inventory)
Risk cost:            5-15%   (obsolescence, damage, shrinkage, spoilage)
                     --------
Total holding cost:  16-38%   of inventory value per year
```

**Real-life example:**
If a retailer holds $10 million in inventory and the holding cost is 25%, they're spending $2.5 million per year just to HAVE that inventory. This is why companies obsess over inventory reduction — every dollar of inventory eliminated saves roughly 25 cents per year in perpetuity.

**Real-life example — the cost of excess:**
In 2001, Cisco wrote off $2.2 BILLION in excess inventory when the dot-com bubble burst. They had ordered components based on inflated demand forecasts. When demand evaporated, they were stuck with warehouses full of networking equipment nobody wanted.

### 1.5 The Cost of NOT Having Inventory (Stockouts)

The flip side is equally painful:

- **Lost sales:** Customer buys from a competitor
- **Lost customers:** They don't come back
- **Production downtime:** A missing component stops the entire line
- **Expediting costs:** Emergency air freight instead of ocean shipping
- **Reputation damage:** "Always out of stock" becomes your brand

**Real-life example:**
During the 2020-2021 semiconductor shortage, automakers like Ford and GM lost billions in revenue. A single missing $1 chip could prevent the completion of a $50,000 truck. Ford estimated the shortage cost them $2.5 billion in 2021 alone.

**The fundamental challenge of inventory management is balancing these two costs: holding too much vs. holding too little.**

---

## Chapter 2: Inventory Identification — SKUs, Barcodes, and Naming

Before you can manage inventory, you need to identify it unambiguously. This chapter covers how items are named, numbered, and tagged.

### 2.1 Stock Keeping Units (SKUs)

An SKU is a unique alphanumeric code assigned to each distinct product variant. It's the fundamental unit of inventory tracking.

**Key principle:** If two items differ in ANY way that matters to your business, they should have different SKUs.

**Example — T-shirt SKUs:**

```
TS-BLK-S     T-shirt, Black, Small
TS-BLK-M     T-shirt, Black, Medium
TS-BLK-L     T-shirt, Black, Large
TS-RED-S     T-shirt, Red, Small
TS-RED-M     T-shirt, Red, Medium
TS-RED-L     T-shirt, Red, Large
```

One "product" (a t-shirt) generates 6 SKUs because each color-size combination must be tracked independently. A store might be overstocked on TS-BLK-L but completely out of TS-RED-S.

**SKU explosion is real:**
If you sell t-shirts in 10 colors, 5 sizes, and 3 fabric types, that's 10 x 5 x 3 = 150 SKUs from ONE product concept.

**Real-life example:**
Amazon's catalog has over 350 million SKUs. Walmart stores carry about 120,000 SKUs. A small boutique might have 500-2,000 SKUs.

### 2.2 SKU Design Best Practices

A well-designed SKU scheme encodes useful information:

```
[Category]-[Sub-category]-[Attribute1]-[Attribute2]-[Sequence]

Examples:
ELEC-LAP-DEL-15-001    Electronics > Laptop > Dell > 15" > Item 001
FURN-CHR-OFC-BLK-003   Furniture > Chair > Office > Black > Item 003
FOOD-BEV-COF-DRK-012   Food > Beverage > Coffee > Dark Roast > Item 012
```

**Rules:**
- Keep it human-readable (someone should guess what it is from the SKU)
- Use consistent length and format
- Avoid characters that cause confusion: O/0, I/1, L/1
- Never reuse a retired SKU (it creates historical data confusion)
- Don't embed information that changes (like price or supplier)

### 2.3 Universal Product Codes (UPC) and Barcodes

While SKUs are internal to your business, UPCs are universal. The barcode on every product in a store is a UPC.

**UPC-A structure (12 digits):**
```
0  74182  76510  8
|  |      |      |
|  |      |      └── Check digit (calculated)
|  |      └── Item number (assigned by manufacturer)
|  └── Company prefix (assigned by GS1)
└── Number system digit (0 = standard product)
```

**How it works in practice:**
1. A company joins GS1 (the global standards organization) and receives a company prefix
2. The company assigns item numbers to each product
3. The check digit is calculated mathematically to catch scanning errors
4. This barcode is printed on every unit of that product worldwide

**Real-life example:**
When a cashier scans a can of Coca-Cola, the scanner reads the UPC barcode, looks it up in the store's database, finds the product name and current price, and records the sale. Simultaneously, the inventory system reduces the count of that SKU by one.

### 2.4 Barcode Types

| Type | Format | Capacity | Common Use |
|------|--------|----------|------------|
| UPC-A | 1D, 12 digits | Numbers only | Retail products (USA/Canada) |
| EAN-13 | 1D, 13 digits | Numbers only | Retail products (international) |
| Code 128 | 1D, variable | Alphanumeric | Shipping labels, internal use |
| Code 39 | 1D, variable | Alphanumeric | Military, healthcare, automotive |
| QR Code | 2D, square | Up to 4,296 chars | URLs, complex data, mobile scanning |
| Data Matrix | 2D, square | Up to 2,335 chars | Small parts, electronics, pharma |

**Real-life example:**
FedEx uses Code 128 barcodes on shipping labels. The barcode encodes the tracking number, which links to their system containing sender, receiver, weight, route, and delivery status.

### 2.5 RFID (Radio-Frequency Identification)

RFID uses radio waves to identify items without line-of-sight scanning. Unlike barcodes, you don't need to point a scanner at each item individually.

**Components:**
- **RFID tag:** A tiny chip + antenna attached to the item (cost: $0.05-$15 per tag)
- **RFID reader:** Emits radio waves and reads responses (cost: $500-$5,000)
- **Software:** Processes the data from readers

**Types of RFID tags:**

| Type | Power Source | Range | Cost | Use Case |
|------|-------------|-------|------|----------|
| Passive | Powered by reader's signal | 1-12 meters | $0.05-$0.50 | Retail, apparel, warehouse |
| Active | Internal battery | Up to 100 meters | $5-$15 | Vehicle tracking, large assets |
| Semi-passive | Battery + reader signal | 10-30 meters | $1-$5 | Temperature monitoring |

**Real-life example — Zara:**
Zara, the fashion retailer, tags every garment with an RFID chip sewn into the label. Benefits they achieved:
- **Inventory accuracy went from 70% to 98%**
- Full store inventory count takes hours instead of days
- They can instantly locate any item in the store
- Automatic alerts when stock is low on the sales floor

Staff walk through the store with a handheld reader, and within seconds, the system knows exactly what's on every shelf, rack, and in the back room.

**Real-life example — Walmart:**
In 2022, Walmart mandated that suppliers apply RFID tags to items in specific categories (apparel, home goods, electronics). This allows them to:
- Take inventory of an entire department in minutes
- Reduce out-of-stock items by 30%
- Improve online order fulfillment from stores

### 2.6 Other Tracking Technologies

**NFC (Near-Field Communication):**
Very short range (< 4 cm). Used in contactless payments and high-security asset tracking. Example: Tapping your phone to a museum exhibit for information.

**BLE Beacons (Bluetooth Low Energy):**
Range of 10-30 meters. Battery lasts 2-5 years. Used for indoor location tracking.
Example: Hospitals track wheelchairs and IV pumps with BLE tags to prevent loss and improve utilization.

**GPS:**
Global range but high power consumption. Used for vehicles, shipping containers, and high-value mobile assets.
Example: Maersk tracks every shipping container globally using GPS. They can tell you the exact latitude/longitude of any of their 4+ million containers.

**IoT Sensors:**
Go beyond location — they track condition: temperature, humidity, vibration, light exposure.
Example: Pharmaceutical companies use IoT sensors in vaccine shipments to ensure cold-chain integrity. If a pallet of vaccines rises above 8°C, the system alerts immediately, and those vaccines may need to be discarded.

---

## Chapter 3: Inventory Valuation — How Much Is Your Inventory Worth?

Inventory valuation determines the monetary value of inventory on your balance sheet and directly impacts your reported profit. Different methods produce different profit numbers from the exact same transactions.

### 3.1 Why Valuation Matters

When you sell an item, you need to record two things:
1. **Revenue:** What the customer paid (straightforward)
2. **Cost of Goods Sold (COGS):** What that item cost you (less straightforward)

The problem: You may have purchased the "same" item multiple times at different prices. Which cost do you use?

### 3.2 FIFO (First-In, First-Out)

**Principle:** The oldest inventory is sold first.

**Example:**
A bookstore buys copies of a novel:
```
Purchase 1 (Jan):  100 copies at $8 each  = $800
Purchase 2 (Mar):  100 copies at $9 each  = $900
Purchase 3 (Jun):  100 copies at $10 each = $1,000

Total: 300 copies, total cost $2,700
```

They sell 150 copies in July at $15 each.

**Under FIFO:**
```
COGS = First 100 copies at $8 = $800
     + Next 50 copies at $9   = $450
     = $1,250

Revenue = 150 x $15 = $2,250
Gross Profit = $2,250 - $1,250 = $1,000

Remaining inventory value:
  50 copies at $9  = $450
  100 copies at $10 = $1,000
  Total: $1,450
```

**When prices are rising, FIFO:**
- Reports HIGHER profit (you're expensing the cheaper old costs)
- Shows HIGHER inventory value on the balance sheet
- Results in HIGHER tax liability

**Real-life example:**
Most grocery stores naturally operate on FIFO — older milk gets pushed to the front, newer milk goes in the back. This matches physical flow and prevents spoilage.

### 3.3 LIFO (Last-In, First-Out)

**Principle:** The newest inventory is sold first (for accounting purposes — physical flow can differ).

**Using the same bookstore example, selling 150 copies:**

**Under LIFO:**
```
COGS = Last 100 copies at $10 = $1,000
     + Next 50 copies at $9   = $450
     = $1,450

Revenue = 150 x $15 = $2,250
Gross Profit = $2,250 - $1,450 = $800

Remaining inventory value:
  100 copies at $8 = $800
  50 copies at $9  = $450
  Total: $1,250
```

**When prices are rising, LIFO:**
- Reports LOWER profit ($800 vs $1,000 under FIFO)
- Shows LOWER inventory value
- Results in LOWER tax liability (this is why US companies use it)

**Important:** LIFO is allowed under US GAAP but **prohibited under IFRS** (international standards). Most of the world uses FIFO.

**Real-life example:**
ExxonMobil uses LIFO for its petroleum inventory. Oil prices fluctuate dramatically, and LIFO allows them to match current high oil costs against current revenue, reducing taxable income. In their annual report, they disclose what inventory would be worth under FIFO (usually billions more).

### 3.4 Weighted Average Cost

**Principle:** Every unit is valued at the average cost of all units available.

**Same bookstore example:**
```
Average cost per copy = $2,700 / 300 = $9.00

Sell 150 copies:
COGS = 150 x $9.00 = $1,350
Gross Profit = $2,250 - $1,350 = $900

Remaining inventory: 150 copies x $9.00 = $1,350
```

**Advantage:** Simple, smooths out price fluctuations.
**Disadvantage:** Doesn't reflect actual physical flow.

**Real-life example:**
Gas stations effectively use weighted average. When a tanker delivers 8,000 gallons at $3.20/gal into a tank that already has 2,000 gallons bought at $3.00/gal, the new average cost is:

```
(2,000 x $3.00 + 8,000 x $3.20) / 10,000 = $3.16/gallon
```

### 3.5 Specific Identification

**Principle:** Track the actual cost of each individual unit.

Used for high-value, unique, or serialized items.

**Real-life example:**
A car dealership tracks each vehicle individually. VIN #1FTFW1E50MFA12345 was purchased for $42,000 from the manufacturer. When it sells for $55,000, COGS is exactly $42,000. There's no ambiguity because each car is unique.

Other uses: jewelry, art, real estate, custom machinery.

### 3.6 FEFO (First-Expired, First-Out)

Not an accounting valuation method, but a critical **physical movement** method for perishable goods.

**Principle:** Items closest to expiration are shipped/sold first, regardless of when they were received.

**Real-life example:**
A pharmaceutical distributor receives two batches of medication:
```
Batch A: Received Jan 15, Expires Dec 2025
Batch B: Received Feb 1, Expires Sep 2025
```

Under FIFO, you'd ship Batch A first (received first).
Under FEFO, you'd ship Batch B first (expires sooner).

FEFO prevents waste and is often legally required in food and pharma industries.

---

## Chapter 4: Inventory Classification — The ABC Analysis

Not all inventory items are equally important. ABC analysis helps you focus attention and resources where they matter most.

### 4.1 The Pareto Principle in Inventory

Vilfredo Pareto observed in 1896 that 80% of Italy's land was owned by 20% of the population. This 80/20 rule appears everywhere, including inventory:

- ~20% of SKUs typically generate ~80% of revenue
- ~20% of SKUs account for ~80% of inventory value

### 4.2 ABC Classification

| Class | % of SKUs | % of Value | Management Approach |
|-------|-----------|------------|-------------------|
| A | 10-20% | 70-80% | Tight control, frequent counting, precise forecasting |
| B | 20-30% | 15-25% | Moderate control, periodic review |
| C | 50-70% | 5-10% | Simple controls, bulk ordering, minimal attention |

### 4.3 How to Perform ABC Analysis

**Step-by-step example — an auto parts store with 10 items:**

```
SKU          Description           Annual Sales ($)
-------------------------------------------------
PART-001     Engine Block           120,000
PART-002     Transmission           95,000
PART-003     Brake Pads             40,000
PART-004     Oil Filter             35,000
PART-005     Spark Plugs            25,000
PART-006     Wiper Blades           12,000
PART-007     Air Freshener          5,000
PART-008     License Plate Frame    3,000
PART-009     Valve Stem Cap         1,500
PART-010     Keychain               800
                                   ---------
Total:                             $337,300
```

**Step 1: Sort by annual sales value (already sorted)**

**Step 2: Calculate cumulative percentage**

```
SKU          Annual Sales   % of Total   Cumulative %   Class
-------------------------------------------------------------
PART-001     $120,000       35.6%        35.6%          A
PART-002     $95,000        28.2%        63.7%          A
PART-003     $40,000        11.9%        75.6%          B
PART-004     $35,000        10.4%        86.0%          B
PART-005     $25,000        7.4%         93.4%          B
PART-006     $12,000        3.6%         96.9%          C
PART-007     $5,000         1.5%         98.4%          C
PART-008     $3,000         0.9%         99.3%          C
PART-009     $1,500         0.4%         99.8%          C
PART-010     $800           0.2%         100.0%         C
```

**Result:**
- **A items (2 SKUs, 20%):** Engine blocks and transmissions = 63.7% of sales value
- **B items (3 SKUs, 30%):** Brake pads, oil filters, spark plugs = 29.7% of sales value
- **C items (5 SKUs, 50%):** Everything else = 6.6% of sales value

### 4.4 Different Policies by Class

**Class A — Engine Blocks ($120K/year):**
- Count weekly
- Maintain safety stock calculated to 99% service level
- Negotiate best supplier pricing with volume contracts
- Track each unit's location precisely
- Review demand forecast monthly

**Class B — Brake Pads ($40K/year):**
- Count monthly
- Maintain safety stock at 95% service level
- Standard supplier terms
- Track by bin location
- Review demand forecast quarterly

**Class C — Keychains ($800/year):**
- Count annually
- Order in bulk when low (two-bin system)
- Whatever supplier is cheapest
- Track at category level, not individual location
- No formal forecasting — just keep "some" in stock

### 4.5 Beyond Simple ABC — Multi-Criteria Analysis

Pure revenue-based ABC misses critical items. Consider:

**A $2 O-ring that's Class C by revenue but shuts down a $50M production line if stockout occurs.**

Advanced ABC analysis adds criteria:
- **Revenue impact** (traditional)
- **Criticality** (what happens if we run out?)
- **Lead time** (how long to replenish?)
- **Demand variability** (how predictable?)
- **Supplier risk** (single source? foreign? reliable?)

**Real-life example:**
In aerospace, a small titanium fastener might cost $15 (Class C by value) but has a 16-week lead time from a single specialized supplier and is required for every aircraft. It gets managed like a Class A item because of criticality and supply risk.

---

# PART II: CORE INVENTORY MANAGEMENT TECHNIQUES

---

## Chapter 5: Demand Forecasting — Predicting What You'll Need

Everything in inventory management starts with forecasting. If you could perfectly predict demand, you'd never have excess stock or stockouts.

### 5.1 Why Forecasting Is Hard

**All forecasts are wrong. The goal is to be less wrong.**

Demand is influenced by:
- Seasonality (winter coats sell in fall, not spring)
- Trends (growing or declining category)
- Promotions (a 30% off sale spikes demand)
- Economic conditions (recession reduces luxury purchases)
- Competitor actions (a rival launches a better product)
- Random variation (noise that can't be predicted)
- Black swan events (pandemic, natural disaster, viral TikTok)

**Real-life example:**
In 2020, nobody's forecast predicted that toilet paper demand would spike 845% in a single week. No forecasting model accounts for panic buying during a pandemic. This is why safety stock exists.

### 5.2 Qualitative Forecasting Methods

Used when historical data is limited or unreliable.

**Sales force composite:** Ask your sales team what they expect to sell.
- Pro: Salespeople know their customers
- Con: They tend to be optimistic (or pessimistic to lower quotas)

**Market research:** Surveys, focus groups, test markets.
- Pro: Direct customer input
- Con: What people say and what they do often differ

**Delphi method:** Gather expert opinions anonymously through multiple rounds until consensus emerges.
- Pro: Reduces bias from dominant personalities
- Con: Slow, expensive

**Real-life example:**
When Apple launches a brand-new product category (like Vision Pro), there's no historical sales data. They rely on market research, executive judgment, and analogies to previous launches to forecast first-year demand. They famously got it wrong with the original iPhone — they underestimated demand massively.

### 5.3 Quantitative Forecasting Methods

Used when you have reliable historical data.

#### Moving Average

Take the average of the last N periods.

**Example — monthly umbrella sales:**
```
Month:   Jan  Feb  Mar  Apr  May  Jun  Jul
Sales:   100  120  90   110  130  95   ?

3-month moving average for July:
= (Apr + May + Jun) / 3
= (110 + 130 + 95) / 3
= 111.7 → Forecast: 112 umbrellas
```

**Limitation:** Treats all recent months equally. A spike in May has the same weight as a normal June.

#### Weighted Moving Average

More recent periods get higher weights.

```
Weights: Current month = 0.5, One month ago = 0.3, Two months ago = 0.2

July forecast:
= (0.5 x 95) + (0.3 x 130) + (0.2 x 110)
= 47.5 + 39 + 22
= 108.5 → Forecast: 109 umbrellas
```

#### Exponential Smoothing

A sophisticated weighted average where the weight decreases exponentially for older data.

```
New Forecast = α × (Actual Demand) + (1 - α) × (Previous Forecast)

Where α (alpha) = smoothing factor, between 0 and 1
- High α (0.5-0.9): Reacts quickly to changes (volatile demand)
- Low α (0.1-0.3): Smooths out noise (stable demand)
```

**Example:**
```
Previous forecast = 100
Actual demand = 120
α = 0.3

New forecast = 0.3 × 120 + 0.7 × 100 = 36 + 70 = 106
```

The forecast adjusts upward (from 100 to 106) because actual demand was higher, but not all the way to 120 because we're smoothing.

#### Seasonal Decomposition

**Real-life example — ice cream shop:**
```
            Q1(Winter)  Q2(Spring)  Q3(Summer)  Q4(Fall)   Annual
Year 1:     2,000       5,000       12,000      4,000      23,000
Year 2:     2,400       6,000       14,000      4,800      27,200
Year 3:     2,800       7,000       16,500      5,600      31,900

Seasonal indices:
Q1: ~9% of annual
Q2: ~22% of annual
Q3: ~52% of annual
Q4: ~17% of annual

Year 4 trend projection: ~36,500 annual sales
Q1 forecast: 36,500 × 0.09 = 3,285
Q2 forecast: 36,500 × 0.22 = 8,030
Q3 forecast: 36,500 × 0.52 = 18,980
Q4 forecast: 36,500 × 0.17 = 6,205
```

### 5.4 Forecast Accuracy Metrics

**Mean Absolute Deviation (MAD):**
```
MAD = Σ|Actual - Forecast| / n

Example over 4 months:
Actual:   100  120  90  110
Forecast: 105  110  95  108

Deviations: |100-105| + |120-110| + |90-95| + |110-108|
          =  5 + 10 + 5 + 2 = 22

MAD = 22 / 4 = 5.5 units
```

**Mean Absolute Percentage Error (MAPE):**
```
MAPE = Σ(|Actual - Forecast| / Actual) / n × 100

= (5/100 + 10/120 + 5/90 + 2/110) / 4 × 100
= (0.050 + 0.083 + 0.056 + 0.018) / 4 × 100
= 5.2%
```

A MAPE under 10% is generally considered good. Under 5% is excellent.

**Real-life benchmark:**
- Stable consumer staples (toothpaste, soap): MAPE 5-15%
- Fashion/seasonal items: MAPE 30-60%
- New products with no history: MAPE 50-100%+

---

## Chapter 6: Reorder Points, Safety Stock, and EOQ

This chapter answers three critical questions:
1. **When** should I reorder? (Reorder Point)
2. **How much extra** should I keep as a buffer? (Safety Stock)
3. **How much** should I order each time? (EOQ)

### 6.1 Reorder Point (ROP)

The inventory level at which you place a new order.

```
ROP = (Average Daily Demand × Lead Time in Days) + Safety Stock
```

**Example — a coffee shop ordering coffee beans:**
```
Average daily usage: 5 kg
Supplier lead time: 4 days
Safety stock: 6 kg (we'll calculate this below)

ROP = (5 × 4) + 6 = 26 kg
```

**Meaning:** When your coffee bean inventory drops to 26 kg, place a new order. The 20 kg covers normal usage during the 4-day wait. The 6 kg of safety stock protects against demand spikes or delivery delays.

### 6.2 Safety Stock

Safety stock is buffer inventory that protects against uncertainty in both demand and supply.

#### Basic Safety Stock Formula:
```
Safety Stock = Z × σ_d × √L

Where:
Z = Service level factor (from normal distribution)
σ_d = Standard deviation of daily demand
L = Lead time in days
```

**Service Level Z-values:**

| Service Level | Z-value | Meaning |
|--------------|---------|---------|
| 90% | 1.28 | Stockout 10% of the time |
| 95% | 1.65 | Stockout 5% of the time |
| 97.5% | 1.96 | Stockout 2.5% of the time |
| 99% | 2.33 | Stockout 1% of the time |
| 99.9% | 3.09 | Stockout 0.1% of the time |

**Full example — a hospital tracking surgical gloves:**
```
Average daily usage: 200 boxes
Standard deviation of daily usage: 30 boxes
Lead time: 3 days
Desired service level: 99% (critical medical supply)

Safety Stock = 2.33 × 30 × √3
            = 2.33 × 30 × 1.73
            = 121 boxes

ROP = (200 × 3) + 121 = 721 boxes
```

**Interpretation:** Keep 121 boxes of safety stock. Reorder when you hit 721 boxes. You'll avoid stockouts 99% of the time.

#### When Lead Time Also Varies:

```
Safety Stock = Z × √(L × σ_d² + d² × σ_L²)

Where:
σ_L = Standard deviation of lead time
d = Average daily demand
```

**Real-life example — an electronics retailer ordering from China:**
```
Average daily demand: 50 units
Std dev of daily demand: 10 units
Average lead time: 30 days (ocean freight)
Std dev of lead time: 5 days (port delays, customs)
Service level: 95%

Safety Stock = 1.65 × √(30 × 10² + 50² × 5²)
            = 1.65 × √(3,000 + 62,500)
            = 1.65 × √65,500
            = 1.65 × 255.9
            = 422 units
```

Notice how lead time variability (5-day std dev on a 30-day lead time) dominates the safety stock calculation. This is why companies work so hard to reduce lead time variability — it has an outsized impact on required safety stock.

### 6.3 Economic Order Quantity (EOQ)

EOQ finds the order quantity that minimizes total inventory cost (ordering cost + holding cost).

```
EOQ = √(2DS / H)

Where:
D = Annual demand (units)
S = Fixed cost per order (ordering/setup cost)
H = Holding cost per unit per year
```

**Example — office supply company ordering printer paper:**
```
Annual demand (D): 10,000 reams
Cost per order (S): $50 (purchase order processing, receiving, inspection)
Holding cost per unit/year (H): $2 per ream (storage, insurance, capital)

EOQ = √(2 × 10,000 × 50 / 2)
    = √500,000
    = 707 reams per order

Number of orders per year: 10,000 / 707 ≈ 14 orders
Days between orders: 365 / 14 ≈ 26 days
```

**Why it works — the cost tradeoff:**

```
If you order 100 reams at a time (small, frequent orders):
  Ordering cost: (10,000/100) × $50 = $5,000/year
  Holding cost: (100/2) × $2 = $100/year
  Total: $5,100/year

If you order 5,000 reams at a time (large, infrequent orders):
  Ordering cost: (10,000/5,000) × $50 = $100/year
  Holding cost: (5,000/2) × $2 = $5,000/year
  Total: $5,100/year

If you order 707 reams (EOQ):
  Ordering cost: (10,000/707) × $50 = $707/year
  Holding cost: (707/2) × $2 = $707/year
  Total: $1,414/year
```

**At EOQ, ordering cost equals holding cost.** That's always the case — it's a mathematical property of the formula.

### 6.4 Limitations of EOQ

EOQ assumes:
- Constant, known demand (rarely true)
- Fixed lead time (varies in practice)
- No quantity discounts (suppliers often offer them)
- Instant replenishment (orders arrive all at once)
- Single product (ignores interactions between products)

**Real-life adjustment:**
Most companies use EOQ as a starting point, then adjust for:
- **Quantity discounts:** Order more if price break savings exceed extra holding cost
- **Truck-load optimization:** Round up to fill a truck or container
- **Supplier minimums:** Adjust to meet minimum order quantities
- **Shelf life:** Don't order more than you can sell before expiration

### 6.5 Min/Max Replenishment System

A simpler alternative to ROP + EOQ:

```
Minimum level (Min) = Reorder Point
Maximum level (Max) = Min + EOQ (or a chosen order quantity)

Rule: When stock drops to Min, order enough to reach Max.
Order quantity = Max - Current Stock
```

**Example — a small restaurant managing olive oil:**
```
Min = 5 bottles (don't go below this)
Max = 20 bottles

Current stock: 4 bottles (below Min!)
Order quantity: 20 - 4 = 16 bottles
```

This system is intuitive and works well for Class B and C items where precise optimization isn't worth the effort.

---

## Chapter 7: Inventory Counting and Accuracy

You can have the best systems in the world, but if your recorded quantities don't match physical reality, nothing works. This chapter covers how to keep records accurate.

### 7.1 Why Records Become Inaccurate

- **Theft/shrinkage:** Employee theft, shoplifting, pilferage
- **Damage:** Broken items not recorded as write-offs
- **Receiving errors:** Counted wrong when goods arrived
- **Picking errors:** Pulled wrong item or wrong quantity
- **System errors:** Software bugs, duplicate transactions
- **Unrecorded movements:** Items moved between locations without updating system
- **Returns processed incorrectly:** Returned items not restocked properly

**Industry shrinkage rates:**
- Retail: 1.4% of sales (~$100 billion/year in the US alone)
- Warehouse: 0.1-0.5% of inventory value
- Manufacturing: 0.5-2% depending on material value

### 7.2 Full Physical Inventory Count

Counting every single item in your facility.

**Process:**
1. **Preparation (1-2 weeks before):**
   - Clean and organize warehouse
   - Ensure all items are in correct locations
   - Process all pending receipts and shipments
   - Print count sheets or configure handheld scanners

2. **Freeze operations:**
   - Stop all receiving, shipping, and movement
   - This typically means shutting down for 1-3 days

3. **Count:**
   - Assign teams to sections
   - Two-person teams: one counts, one records
   - First count, then blind recount of discrepancies

4. **Reconcile:**
   - Compare physical counts to system records
   - Investigate significant discrepancies
   - Adjust system records

5. **Resume operations**

**Real-life example:**
IKEA conducts a full physical inventory at every store once per year. Their stores stock 9,500+ products. The count typically happens overnight and into the next morning, with the store closed to customers. Hundreds of employees participate. Cost: approximately $200,000-$500,000 per store per count event (lost sales + labor).

**Problem:** It's expensive, disruptive, and gives you accuracy only once per year. The day after the count, accuracy starts degrading again.

### 7.3 Cycle Counting

Counting a small portion of inventory every day, so the entire inventory is counted over a period (typically quarterly or annually).

**ABC-based cycle counting schedule:**

| Class | % of SKUs | Count Frequency | Result |
|-------|-----------|----------------|--------|
| A | 20% | Monthly | Counted 12 times/year |
| B | 30% | Quarterly | Counted 4 times/year |
| C | 50% | Annually | Counted 1 time/year |

**Daily cycle count calculation:**
```
Working days per year: 250

A items: 200 SKUs × 12 counts/year = 2,400 counts
B items: 300 SKUs × 4 counts/year  = 1,200 counts
C items: 500 SKUs × 1 count/year   = 500 counts
Total counts per year:                4,100 counts

Counts per day: 4,100 / 250 = 16.4 → about 17 counts per day
```

One person can typically count 15-30 SKUs per hour, so this requires about 1 hour of dedicated counting per day.

**Real-life example:**
Amazon's fulfillment centers use continuous cycle counting powered by their systems. When a picker is sent to a bin to retrieve an item and notices a discrepancy ("system says 5, but I see 3"), they flag it. The system also generates proactive count tasks for bins that haven't been verified recently or that show suspicious patterns.

### 7.4 Inventory Accuracy Metrics

**Inventory Record Accuracy (IRA):**
```
IRA = (Number of accurate records / Total records counted) × 100

Example: Counted 500 SKUs, 475 matched system records
IRA = 475/500 × 100 = 95%
```

**World-class target: 95-99% accuracy**

**Dollar accuracy:**
```
Dollar Accuracy = 1 - (Σ|System Value - Actual Value| / Total Inventory Value)

Example:
Total inventory value: $1,000,000
Sum of absolute discrepancies: $15,000
Dollar accuracy = 1 - (15,000/1,000,000) = 98.5%
```

**Real-life benchmarks:**
- Top performers (Amazon, Toyota): 99%+
- Average companies: 80-95%
- Struggling companies: Below 80% (operations are chaotic)

### 7.5 Root Cause Analysis for Discrepancies

When you find a discrepancy, don't just adjust the number — find out WHY.

**Common patterns and their causes:**

| Pattern | Likely Cause |
|---------|-------------|
| System shows MORE than actual | Theft, unrecorded damage, receiving shortages |
| System shows LESS than actual | Unrecorded returns, double-shipment received |
| Always off by same amount | Systematic counting error, unit-of-measure mismatch |
| Specific location always wrong | Training issue with staff in that area |
| High-value items most affected | Targeted theft |
| Discrepancies spike after certain shifts | Specific employee issue |

**Real-life example:**
A distribution center found that their count of a specific part was always off by multiples of 12. Investigation revealed that the supplier shipped in cases of 12, but the receiving team was recording "1" (meaning 1 case) while the system expected individual units. A simple unit-of-measure correction fixed months of discrepancies.

---

# PART III: WAREHOUSE OPERATIONS

---

## Chapter 8: Warehouse Layout and Storage

### 8.1 Warehouse Zones

A well-organized warehouse has distinct zones:

```
┌──────────────────────────────────────────────────────────┐
│                    SHIPPING DOCK                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│  │ Staging  │  │ Staging  │  │ Staging  │              │
│  │ Lane 1   │  │ Lane 2   │  │ Lane 3   │              │
│  └──────────┘  └──────────┘  └──────────┘              │
│                                                          │
│  ┌──────────────────────────────────────────────────┐   │
│  │              PACKING AREA                         │   │
│  │  Stations 1-6, QC Check, Labeling                │   │
│  └──────────────────────────────────────────────────┘   │
│                                                          │
│  ┌──────────────────────────────────────────────────┐   │
│  │            PICK ZONE (Fast movers)                │   │
│  │  Shelving, Flow Racks, Carton Pick               │   │
│  └──────────────────────────────────────────────────┘   │
│                                                          │
│  ┌──────────────────────────────────────────────────┐   │
│  │          BULK STORAGE (Pallet Racking)            │   │
│  │  Selective, Drive-in, Push-back                   │   │
│  └──────────────────────────────────────────────────┘   │
│                                                          │
│  ┌──────────────────────────────────────────────────┐   │
│  │          RESERVE / OVERFLOW STORAGE               │   │
│  │  Seasonal, Slow movers, Bulk overstock            │   │
│  └──────────────────────────────────────────────────┘   │
│                                                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────────────────┐  │
│  │Receiving │  │Receiving │  │  QC / Inspection     │  │
│  │ Dock 1   │  │ Dock 2   │  │  Area                │  │
│  └──────────┘  └──────────┘  └──────────────────────┘  │
│                    RECEIVING DOCK                         │
└──────────────────────────────────────────────────────────┘
```

### 8.2 Storage Systems

**Selective Pallet Racking:**
Most common. Each pallet is directly accessible. Lower density but maximum flexibility.
Used for: Items with many SKUs and moderate quantities per SKU.

**Drive-In Racking:**
Forklifts drive into the rack structure. High density, but LIFO access only.
Used for: Few SKUs with high quantity (e.g., a beverage distributor storing pallets of Coca-Cola).

**Push-Back Racking:**
Pallets sit on nested carts on inclined rails. Load from front, gravity pushes forward.
Used for: 2-6 pallets deep per SKU, LIFO access.

**Pallet Flow (Gravity Flow):**
Inclined rollers, load from back, pick from front. FIFO access.
Used for: Perishables, date-sensitive items.

**Automated Storage and Retrieval System (AS/RS):**
Computer-controlled cranes store and retrieve pallets/totes in high-density racking (often 100+ feet tall).
Used for: High-volume, space-constrained operations.

**Real-life example:**
Ocado (UK online grocery) operates fully automated warehouses where thousands of robots travel on a grid on top of the warehouse, diving down to retrieve specific totes of groceries. Their system can process a 50-item grocery order in about 5 minutes — a task that would take a human 30+ minutes walking through aisles.

### 8.3 Bin Locations and Addressing

Every position in a warehouse has an address, just like a street address.

**Typical format:**
```
Zone - Aisle - Rack - Level - Position

A-05-03-B-02

A    = Zone A (fast-moving items)
05   = Aisle 5
03   = Rack section 3 (counting from the end of the aisle)
B    = Level B (second shelf from floor: A=floor, B=second, C=third)
02   = Position 2 (left to right within the shelf)
```

**Why this matters:**
When a picker gets an order to fill, their pick list says:
```
Pick List #4521
Destination: Packing Station 3

1. SKU: ELEC-MOUSE-LOG-001   Qty: 2   Location: A-05-03-B-02
2. SKU: ELEC-KEYB-LOG-004    Qty: 1   Location: A-05-04-B-01
3. SKU: FURN-STAND-MON-002   Qty: 1   Location: C-12-01-A-01
```

Good location addressing means the picker can navigate directly to each item without wandering or asking for help.

### 8.4 Slotting Optimization

Slotting is deciding WHERE each SKU lives in the warehouse. It's one of the highest-impact decisions in warehouse operations.

**Principles:**
- **Fast movers near shipping:** A-class items go in the pick zone, closest to packing/shipping
- **Heavy items at floor level:** No lifting required, safer
- **Related items together:** If items frequently ship together, store them near each other
- **Ergonomic considerations:** Items picked most often at waist height (golden zone)
- **Size matching:** Small items in small bins, large items on pallets

**The golden zone:**
```
Height from floor:
  Above 6 ft:   Slow movers, lightweight items
  3-5 ft:        GOLDEN ZONE — fastest movers here (waist to shoulder)
  1-3 ft:        Medium movers, heavier items
  Floor level:   Heaviest items, pallet picks, bulk cases
```

**Real-life example:**
A wine distributor analyzed their pick data and found that 5 wines (out of 2,000 SKUs) accounted for 35% of all picks. These 5 wines were scattered throughout the warehouse. By moving them to floor-level positions near the shipping dock, picker travel distance decreased by 22%, and daily throughput increased by 15%.

---

## Chapter 9: Receiving, Putaway, Picking, Packing, and Shipping

### 9.1 Receiving

The process of accepting incoming goods from suppliers.

**Steps:**
1. **Appointment scheduling:** Truck arrives at scheduled time (dock appointment)
2. **Unloading:** Forklift removes pallets from truck
3. **Verification:** Check PO (purchase order) against packing slip and actual goods
4. **Inspection:** Quality check (sample or full inspection depending on supplier reliability)
5. **System receipt:** Enter received quantities into inventory system
6. **Labeling:** Apply internal barcodes/labels if supplier labels are insufficient
7. **Putaway:** Move goods to storage locations

**What can go wrong:**
- Received quantity doesn't match PO (short shipment or over-shipment)
- Wrong items received
- Damaged goods
- Missing documentation
- Items fail quality inspection

**Real-life example:**
At Costco distribution centers, inbound trucks are "cross-docked" — products flow from the receiving dock directly to outbound shipping lanes without ever entering storage. This works because Costco carries only ~3,700 SKUs (vs. Walmart's 120,000+), and demand is high enough that incoming shipments can be immediately allocated to outbound store deliveries.

### 9.2 Putaway

Moving received goods from the receiving dock to their storage location.

**Putaway strategies:**

| Strategy | How It Works | Best For |
|----------|-------------|----------|
| Fixed location | Each SKU has a permanent home | Small warehouses, few SKUs |
| Random (floating) | System assigns any available location | Maximizing space utilization |
| Zone-based | Items go to a designated zone, any spot within | Balance of control and flexibility |
| Closest open location | Put it in the nearest empty spot | Speed (but harder to find later) |
| Class-based | A items near dock, C items in back | Supporting ABC movement strategy |

**Real-life example:**
Amazon uses "random stow" — when an item is received, the associate places it in any available bin and scans both the item and the bin barcode. The system remembers where everything is. This seems chaotic, but it's brilliant because:
- It maximizes space utilization (no reserved empty spaces for specific SKUs)
- It distributes popular items across the warehouse (reducing aisle congestion)
- It places dissimilar items near each other (reducing picking errors — you won't confuse a book with a blender)

### 9.3 Picking

Retrieving items from storage to fulfill orders. This is typically the MOST expensive warehouse activity, accounting for 50-65% of warehouse labor costs.

**Picking methods:**

#### Discrete (Single Order) Picking
One picker, one order at a time. Walk through the warehouse, pick all items for that order, return.

- Pro: Simple, low error rate
- Con: Maximum walking distance
- Best for: Small warehouses, complex/large orders

#### Batch Picking
One picker picks items for multiple orders simultaneously.

```
Instead of:
  Trip 1: Order A needs items from aisles 1, 5, 12
  Trip 2: Order B needs items from aisles 2, 5, 11
  Trip 3: Order C needs items from aisles 1, 3, 12

Batched:
  Single trip: Pick all items from aisles 1, 2, 3, 5, 11, 12
  Then sort into orders A, B, C at packing station
```

- Pro: Drastically reduces walking
- Con: Requires sorting step, slightly higher error risk
- Best for: Many small orders with overlapping items

#### Zone Picking
Each picker is assigned to a zone. An order passes through each zone, and pickers add items from their zone.

```
Order #1001 needs:
  Zone A (Electronics):  USB cable, mouse
  Zone B (Books):        2 novels
  Zone C (Clothing):     T-shirt

Zone A picker adds USB cable + mouse → tote moves to Zone B
Zone B picker adds 2 novels → tote moves to Zone C
Zone C picker adds T-shirt → tote moves to packing
```

- Pro: Pickers know their zone well, less walking
- Con: Requires coordination, orders wait for slowest zone
- Best for: Large warehouses with diverse inventory

#### Wave Picking
Orders are grouped into "waves" (e.g., all orders shipping via FedEx Ground by 2 PM). Each wave is released, picked, packed, and shipped together.

- Pro: Aligns picking with shipping schedules
- Best for: Operations with defined shipping cutoff times

**Real-life example:**
Zappos (online shoe retailer, owned by Amazon) processes up to 20,000 orders per day from their warehouse in Shepherdsville, Kentucky. They use a combination of zone and batch picking. Shoes are stored in a multi-level mezzanine, and conveyor systems transport totes between zones. Their warehouse staff walk an average of 10 miles per shift.

### 9.4 Packing

Preparing picked items for shipment.

**Considerations:**
- Right-size the box (minimize dimensional weight charges)
- Adequate protection (bubble wrap, air pillows, paper)
- Include packing slip and any inserts
- Weight/dimensions for carrier rate calculation
- Fragile items need special handling

**Real-life example:**
Amazon's "frustration-free packaging" initiative redesigned product packaging so many items can ship in their own packaging without an additional Amazon box. This saved:
- Millions of cardboard boxes per year
- Reduced package volume (fitting more on trucks)
- Faster packing (no box selection, no void fill)
- Better customer experience (easier to open)

### 9.5 Shipping

Getting the packed order to the customer.

**Carrier selection factors:**
- Delivery speed (overnight vs. ground)
- Package size/weight
- Destination zone
- Cost
- Service reliability
- Special requirements (hazmat, refrigerated, signature required)

**Real-life example — shipping rate optimization:**
A medium-sized e-commerce company ships 1,000 packages/day. Using a rate shopping system, each package is compared across UPS, FedEx, USPS, and regional carriers. The system selects the cheapest option that meets the promised delivery date. Typical savings: 15-25% vs. using a single carrier.

---

# PART IV: ASSET TRACKING AND LIFECYCLE MANAGEMENT

---

## Chapter 10: Asset Lifecycle Management

While inventory flows through a business (bought → stored → sold), assets are kept and used. Asset tracking manages items through their entire life with the organization.

### 10.1 The Asset Lifecycle

```
1. Planning & Budgeting
       │
       ▼
2. Procurement / Acquisition
       │
       ▼
3. Receiving & Tagging
       │
       ▼
4. Deployment / Assignment
       │
       ▼
5. Operation & Utilization
       │
       ▼
6. Maintenance & Repair ──────┐
       │                       │
       ▼                       │
7. Redeployment / Transfer ───┘
       │
       ▼
8. Depreciation (ongoing from step 4)
       │
       ▼
9. Retirement / Disposal
```

### 10.2 Stage 1: Planning and Budgeting

Before acquiring assets, organizations plan:

- **Capital budget:** How much money is available for assets this year?
- **Needs assessment:** What do we actually need? Can we lease instead of buy?
- **Total Cost of Ownership (TCO):** Purchase price is just the beginning.

**TCO Example — company laptop:**
```
Purchase price:                    $1,200
Setup and configuration labor:     $150
Software licenses (3 years):       $600
IT support (3 years):              $450
Accessories (dock, monitor, bag):  $400
Disposal/data wipe:                $50
                                   ------
3-year TCO:                        $2,850
Annual TCO:                        $950

The $1,200 laptop actually costs $2,850 over its life.
```

**Real-life example:**
A hospital evaluating an MRI machine:
```
Purchase price:               $1,500,000
Installation & site prep:     $500,000
Annual maintenance contract:  $150,000 × 10 years = $1,500,000
Training staff:               $50,000
Helium refills:               $30,000/year × 10 = $300,000
Electricity:                  $25,000/year × 10 = $250,000
Disposal/decommission:        $100,000
                              ----------
10-year TCO:                  $4,200,000

That $1.5M machine actually costs $4.2M over its life.
```

### 10.3 Stage 2-3: Procurement, Receiving, and Tagging

When an asset arrives:

1. **Verify against purchase order** (correct model, specs, quantity)
2. **Assign an asset tag** (unique ID that follows this asset for its entire life)
3. **Record in the asset register:**
   - Asset ID / tag number
   - Description
   - Serial number (manufacturer's)
   - Purchase date
   - Purchase price
   - Vendor
   - Warranty expiration
   - Assigned location
   - Assigned user (if applicable)
   - Asset category (IT, furniture, vehicle, machinery)
   - Expected useful life
   - Depreciation method

**Asset tag formats:**
```
Sequential:     AST-00001, AST-00002, AST-00003
Category-based: IT-LAP-0001, IT-MON-0001, FRN-DSK-0001
Location-based: NYC-FL3-0001, LON-FL1-0001
```

### 10.4 Stage 4-5: Deployment and Utilization

**Assignment tracking:**
Who has what, and where is it?

```
Asset: IT-LAP-0247
Type: Dell Latitude 5540
Serial: FGHJ456789
Status: Deployed
Assigned to: Sarah Chen (Engineering)
Location: Building A, Floor 3, Desk 312
Deployed date: 2024-03-15
Last seen: 2024-11-20 (badge scan at Building A)
```

**Utilization tracking:**
Is the asset actually being used effectively?

**Real-life example — fleet management:**
A delivery company has 200 trucks. GPS tracking shows:
```
Truck #47:  Running 11 hours/day, 95% capacity → well-utilized
Truck #123: Running 3 hours/day, 40% capacity → underutilized
Truck #89:  In maintenance 15 days this month → reliability issue
```

With this data, they might:
- Remove truck #123 from the fleet (sell or reassign)
- Investigate why truck #89 keeps breaking down
- Buy more trucks like #47 (same model/config clearly works well)

**Real-life example — software license management:**
A company pays for 500 Photoshop licenses at $300/year each ($150,000/year). Usage tracking shows only 280 are actively used. That's $66,000/year wasted on unused licenses.

### 10.5 Stage 6-7: Maintenance

#### Types of Maintenance:

**Reactive (Run-to-failure):**
Fix it when it breaks.
- Pro: No upfront maintenance cost
- Con: Unplanned downtime, often more expensive repairs, safety risk
- Appropriate for: Low-cost, non-critical, easily replaceable items

**Preventive (Time-based):**
Schedule maintenance at regular intervals regardless of condition.
- Example: Change oil every 5,000 miles. Replace air filters every 6 months.
- Pro: Reduces unexpected failures
- Con: May replace parts that still have life left (wasteful)

**Predictive (Condition-based):**
Use sensors and data to predict when maintenance is needed.
- Example: Vibration sensor on a motor detects increasing amplitude → schedule bearing replacement before failure.
- Pro: Maintenance only when actually needed, maximum component life
- Con: Requires sensors, data infrastructure, and analytics capability

**Prescriptive:**
AI not only predicts when failure will occur but recommends the specific action to take.
- Example: "Motor bearing on Press #7 will fail in 12-18 days. Schedule replacement in next planned downtime window (Thursday). Parts needed: SKF 6205 bearing (in stock, Bin C-04-02)."

**Real-life example — predictive maintenance at Rolls-Royce:**
Rolls-Royce monitors every jet engine they manufacture using thousands of sensors that stream data in real-time during flight. They analyze:
- Temperature profiles
- Vibration patterns
- Oil particle content
- Fuel consumption efficiency
- Pressure differentials

Their systems can predict engine component failures weeks before they happen, allowing airlines to schedule maintenance at convenient times rather than having an aircraft grounded unexpectedly. This "power by the hour" service model means airlines pay per flight hour and Rolls-Royce handles all maintenance.

### 10.6 Work Orders

A work order is a formal request to perform maintenance on an asset.

```
WORK ORDER #WO-2024-1847

Asset:        CNC Machine #4 (AST-MCH-0004)
Location:     Building B, Production Floor, Bay 7
Priority:     High
Type:         Corrective Maintenance
Requested by: John Miller (Production Manager)
Assigned to:  Maria Garcia (Maintenance Tech III)

Problem Description:
  CNC Machine #4 producing parts outside tolerance.
  X-axis positioning error of +0.05mm detected during
  QC check on Part #P-7721 (batch of 50, all scrapped).

Tasks:
  [ ] Inspect X-axis linear guide rails
  [ ] Check ball screw backlash
  [ ] Verify servo motor encoder alignment
  [ ] Recalibrate X-axis
  [ ] Run test program and verify tolerance

Parts Needed:
  - Ball screw nut (if worn) — SKU: MCH-BSN-20-001
  - Linear guide block (if damaged) — SKU: MCH-LGB-20-002

Estimated downtime: 4-8 hours
Actual downtime: ___
Actual parts used: ___
Resolution notes: ___
```

### 10.7 Stage 8: Depreciation

Assets lose value over time. Depreciation is the accounting method for recognizing this decline.

**Why it matters:**
- A $50,000 machine doesn't cost $50,000 in the year you buy it (for accounting/tax purposes)
- The cost is spread over the asset's useful life
- Depreciation reduces taxable income each year

#### Straight-Line Depreciation
Most common. Equal expense each year.

```
Annual Depreciation = (Cost - Salvage Value) / Useful Life

Example — delivery van:
  Purchase price: $40,000
  Estimated salvage value: $5,000 (what you'll sell it for at end of life)
  Useful life: 7 years

  Annual depreciation = ($40,000 - $5,000) / 7 = $5,000/year

Year 1: Book value = $40,000 - $5,000 = $35,000
Year 2: Book value = $35,000 - $5,000 = $30,000
Year 3: Book value = $30,000 - $5,000 = $25,000
...
Year 7: Book value = $10,000 - $5,000 = $5,000 (salvage value)
```

#### Declining Balance Depreciation
Higher depreciation in early years (accelerated).

```
Annual Depreciation = Book Value × Depreciation Rate

Double-declining balance rate = 2 / Useful Life

Example — same van:
  Rate = 2/7 = 28.57%

Year 1: $40,000 × 28.57% = $11,428 → Book value: $28,572
Year 2: $28,572 × 28.57% = $8,163  → Book value: $20,409
Year 3: $20,409 × 28.57% = $5,831  → Book value: $14,578
Year 4: $14,578 × 28.57% = $4,165  → Book value: $10,413
Year 5: $10,413 × 28.57% = $2,975  → Book value: $7,438
Year 6: $7,438  × 28.57% = $2,125  → Book value: $5,313
Year 7: $5,313  - $5,000  = $313    → Book value: $5,000
```

**Note:** In year 7, we only depreciate down to salvage value, not the full 28.57%.

**Why use accelerated depreciation?**
- Tax benefits: Higher deductions in early years when the asset generates the most revenue
- Matches reality: Many assets (especially technology) lose value fastest in early years

#### Units of Production

Depreciation based on actual usage, not time.

```
Depreciation per unit = (Cost - Salvage) / Total Expected Units

Example — printing press:
  Cost: $200,000
  Salvage: $20,000
  Expected lifetime production: 1,000,000 pages

  Depreciation per page = ($200,000 - $20,000) / 1,000,000 = $0.18/page

Year 1: Printed 300,000 pages → Depreciation: $54,000
Year 2: Printed 250,000 pages → Depreciation: $45,000
Year 3: Printed 150,000 pages → Depreciation: $27,000
```

**Real-life application:**
Airlines depreciate aircraft based on flight hours, not years. A plane that flies 4,000 hours/year depreciates faster than one flying 2,000 hours/year, which reflects actual wear and tear.

### 10.8 Stage 9: Disposal

When an asset reaches end of life:

**Options:**
1. **Sell:** Auction, broker, direct sale
2. **Trade-in:** Toward a replacement
3. **Donate:** Tax benefits for charitable donation
4. **Recycle:** Recover materials
5. **Destroy:** For data security (hard drives) or hazmat compliance

**Real-life example — IT asset disposal:**
When a company retires 500 laptops, they must:
1. Back up any needed data
2. Wipe all drives (DOD 5220.22-M standard: 3 passes minimum, or physical destruction)
3. Remove asset tags and update the register
4. Determine disposition: refurbish and resell, donate, or recycle
5. Obtain certificate of destruction/recycling for compliance
6. Record the disposal and any gain/loss

**Gain/Loss on disposal:**
```
Laptop original cost: $1,200
Accumulated depreciation: $1,000
Book value: $200

If sold for $300: Gain of $100 (taxable)
If sold for $100: Loss of $100 (tax deductible)
If destroyed:     Loss of $200 (write-off)
```

---

# PART V: SYSTEMS AND TECHNOLOGY

---

## Chapter 11: Inventory and Asset Management Systems

### 11.1 Spreadsheets (Where Everyone Starts)

**When spreadsheets work:**
- Under ~500 SKUs
- Single location
- 1-3 people managing inventory
- Low transaction volume

**Simple inventory spreadsheet structure:**
```
| SKU | Description | Location | Qty On Hand | Reorder Point | Last Count Date | Unit Cost |
|-----|-------------|----------|-------------|---------------|-----------------|-----------|
| A001 | Widget Blue | Shelf A1 | 45 | 20 | 2024-01-15 | $3.50 |
| A002 | Widget Red  | Shelf A2 | 12 | 20 | 2024-01-15 | $3.50 |
| B001 | Gadget Pro  | Shelf B1 | 8  | 5  | 2024-01-14 | $24.99 |
```

**When spreadsheets break down:**
- Multiple people editing simultaneously (version conflicts)
- No audit trail (who changed what, when?)
- No real-time updates
- No automated alerts (reorder points must be manually checked)
- Formula errors compound silently
- No integration with barcode scanners, POS systems, or accounting

**Real-life example:**
A small Etsy seller managing 50 handmade jewelry designs in a Google Sheet works fine. A growing e-commerce business with 5,000 SKUs, 3 warehouses, and 200 orders/day will drown in spreadsheet chaos.

### 11.2 Warehouse Management Systems (WMS)

Software that manages daily warehouse operations: receiving, putaway, picking, packing, shipping.

**Core features:**
- Real-time inventory visibility by location
- Directed putaway (system tells workers where to store items)
- Pick optimization (efficient pick paths)
- Wave/batch planning
- Integration with barcode/RFID scanners
- Labor management and productivity tracking
- Shipping integration (carrier selection, label printing)

**Popular WMS solutions:**

| System | Target Market | Cost Range |
|--------|--------------|------------|
| Manhattan Associates | Enterprise | $500K-$5M+ |
| Blue Yonder (JDA) | Enterprise | $500K-$3M+ |
| HighJump (Korber) | Mid-market to enterprise | $100K-$1M |
| Fishbowl | Small business | $5K-$50K |
| Logiwa | E-commerce | $200-$2,000/month |
| ShipBob WMS | Small e-commerce | Usage-based |

### 11.3 Enterprise Resource Planning (ERP)

ERP systems integrate ALL business functions into a single system: inventory, accounting, purchasing, sales, manufacturing, HR, and more.

**How inventory fits into ERP:**

```
┌─────────────────────────────────────────────────────┐
│                    ERP SYSTEM                        │
│                                                     │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐     │
│  │  Sales   │───▶│ Inventory│◀───│Purchasing│     │
│  │  Orders  │    │Management│    │  Orders  │     │
│  └──────────┘    └────┬─────┘    └──────────┘     │
│                       │                             │
│            ┌──────────┼──────────┐                 │
│            ▼          ▼          ▼                 │
│     ┌──────────┐ ┌──────────┐ ┌──────────┐       │
│     │Accounting│ │Production│ │ Warehouse│       │
│     │ (COGS,  │ │ Planning │ │ Mgmt     │       │
│     │  GL)    │ │ (MRP)    │ │ (WMS)    │       │
│     └──────────┘ └──────────┘ └──────────┘       │
│                                                     │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐     │
│  │   HR     │    │ Finance  │    │ CRM      │     │
│  │          │    │          │    │          │     │
│  └──────────┘    └──────────┘    └──────────┘     │
└─────────────────────────────────────────────────────┘
```

**The magic of integration:**
When a customer places an order:
1. **Sales module** creates the order
2. **Inventory module** checks availability and reserves stock
3. **Warehouse module** generates a pick list
4. **Accounting module** creates an invoice
5. **Inventory module** reduces on-hand quantity
6. **Purchasing module** (if stock is low) generates a purchase order to the supplier
7. **Finance module** records the revenue and COGS

All of this happens in ONE system, with ONE database, with no manual data transfer.

**Popular ERP systems:**

| System | Target | Annual Cost |
|--------|--------|-------------|
| SAP S/4HANA | Large enterprise | $500K-$10M+ |
| Oracle NetSuite | Mid-market | $50K-$500K |
| Microsoft Dynamics 365 | Mid to large | $100K-$2M |
| Odoo | SMB (open source) | Free - $50K |
| ERPNext | SMB (open source) | Free - $20K |
| Sage Intacct | SMB | $15K-$100K |

**Real-life example — failed ERP implementation:**
In 1999, Hershey's went live with a new SAP ERP system just before Halloween — their busiest season. The implementation was rushed (30 months compressed into 18). The result:
- $150 million in unshipped orders
- Inventory was in warehouses but the system couldn't process orders correctly
- Stock price dropped 8% in one day
- It took 2 years to fully recover

**Lesson:** ERP implementations are massive projects. Never go live during peak season.

### 11.4 Computerized Maintenance Management Systems (CMMS)

Software specifically for managing assets and maintenance.

**Core features:**
- Asset register (all assets with specs, location, history)
- Work order management (create, assign, track, close)
- Preventive maintenance scheduling
- Parts inventory management (maintenance supplies)
- Labor tracking
- Reporting (MTBF, MTTR, maintenance costs by asset)

**Key metrics tracked by CMMS:**

```
MTBF (Mean Time Between Failures):
  How long an asset runs before breaking down.
  Example: If a pump fails every 90 days on average, MTBF = 90 days.

MTTR (Mean Time To Repair):
  How long it takes to fix something once it breaks.
  Example: Average pump repair takes 4 hours, MTTR = 4 hours.

OEE (Overall Equipment Effectiveness):
  OEE = Availability × Performance × Quality

  Availability = Actual run time / Planned run time
  Performance = Actual output / Theoretical max output
  Quality = Good units / Total units produced

  Example:
    Planned: 8-hour shift
    Downtime: 1 hour (changeover + breakdown)
    Availability = 7/8 = 87.5%

    Theoretical rate: 100 units/hour
    Actual: 80 units/hour
    Performance = 80/100 = 80%

    Total produced: 560 units
    Good units: 540
    Quality = 540/560 = 96.4%

    OEE = 87.5% × 80% × 96.4% = 67.5%

World-class OEE: 85%+
Average manufacturing OEE: 60%
```

**Popular CMMS systems:**
- IBM Maximo (enterprise)
- SAP PM (enterprise, integrated with SAP ERP)
- Fiix (mid-market, cloud)
- UpKeep (SMB, mobile-first)
- Limble (SMB)

---

## Chapter 12: Multi-Location and Supply Chain Considerations

### 12.1 Multi-Warehouse Inventory

When you have more than one location, new challenges emerge:

**Transfer orders:**
Moving inventory between your own locations.
```
Transfer Order #TO-1547
From: Warehouse East (Philadelphia)
To: Warehouse West (Phoenix)
Reason: Rebalancing — West is low on summer items

SKU          Description      Qty    Status
APPRL-SS-001 Sun Hat          200    In Transit
APPRL-SS-015 Swim Trunks      150    In Transit
OUTDR-BB-003 Beach Ball       500    In Transit

Ship date: 2024-03-01
ETA: 2024-03-05
Carrier: FedEx Freight
Tracking: 7729-4481-3390
```

**Inventory allocation decisions:**
When multiple warehouses can fulfill an order, which should?

Factors:
- **Proximity to customer** (shortest delivery time)
- **Inventory levels** (ship from location with excess, not the one running low)
- **Shipping cost** (zone-based rates)
- **Warehouse capacity** (relieve the busy warehouse)

**Real-life example:**
When you order something on Amazon, their system considers 175+ fulfillment centers across the US. The algorithm factors in:
- Which warehouses have the item in stock
- Distance to your delivery address
- Current workload at each warehouse
- Delivery promise made to you (same-day, next-day, two-day)
- Whether multiple items in your order can ship from the same location (saves shipping)

Sometimes it's cheaper to split your order across two warehouses than to transfer inventory first.

### 12.2 Distributed Order Management (DOM)

DOM systems sit on top of inventory across all locations and channels, making intelligent fulfillment decisions.

```
Customer orders 3 items online:
  Item A: In stock at Warehouse, Store #12, Store #45
  Item B: In stock at Warehouse only
  Item C: In stock at Store #12 only

DOM decision options:
  Option 1: Ship all from Warehouse → Item C not available, backorder it
  Option 2: Ship A+C from Store #12, B from Warehouse → 2 shipments
  Option 3: Transfer C to Warehouse, ship all from Warehouse → delay

DOM weighs: Cost, speed, inventory balance, customer promise
Selects: Option 2 (meets delivery promise, avoids backorder)
```

**Real-life example:**
Target's "ship from store" program turned 1,900 stores into mini-fulfillment centers. During peak season, stores near the customer ship online orders faster and cheaper than distant warehouses. This strategy helped Target achieve same-day delivery on 95% of online orders in targeted zip codes.

### 12.3 Inventory Visibility Across the Supply Chain

**The bullwhip effect:**
Small demand changes at the retail level get amplified up the supply chain.

```
Customer demand increases 10%
  → Retailer orders 20% more (overreacting + safety stock padding)
    → Distributor orders 40% more
      → Manufacturer orders 60% more
        → Raw material supplier orders 80% more

Result: Massive overproduction and excess inventory throughout the chain
```

**Real-life example:**
Procter & Gamble first identified the bullwhip effect when studying Pampers diaper demand. While baby diaper usage is remarkably stable (babies don't suddenly use more diapers), their supply chain saw wild demand swings because each level was independently overreacting to perceived demand changes.

**Solution: Supply chain visibility**
Share real-time inventory and demand data across the chain.

- **VMI (Vendor-Managed Inventory):** The supplier monitors your inventory and decides when to replenish.
  - Example: Coca-Cola delivery drivers check store shelves and restock directly, rather than waiting for the store to place orders.

- **CPFR (Collaborative Planning, Forecasting, and Replenishment):** Trading partners share forecasts and coordinate plans.
  - Example: Walmart shares point-of-sale data with suppliers in real-time through Retail Link, so suppliers can see exactly what's selling and adjust production accordingly.

---

# PART VI: ADVANCED TOPICS

---

## Chapter 13: Lean Inventory and Just-In-Time (JIT)

### 13.1 The Toyota Production System

The most influential inventory management philosophy originated at Toyota in the 1950s under Taiichi Ohno. The core idea: **inventory is waste**.

**The seven wastes (Muda):**
1. **Overproduction:** Making more than needed
2. **Waiting:** Idle time between process steps
3. **Transportation:** Unnecessary movement of materials
4. **Over-processing:** Doing more work than necessary
5. **Inventory:** Excess stock beyond immediate need
6. **Motion:** Unnecessary movement of people
7. **Defects:** Scrap, rework, returns

### 13.2 Just-In-Time (JIT)

**Principle:** Produce and deliver exactly what is needed, when it is needed, in the quantity needed.

**How it works at Toyota:**
1. A car is ordered by a customer (or dealer)
2. The assembly line produces that specific car
3. Parts arrive at the assembly line exactly when needed — not hours or days early
4. Suppliers deliver multiple times per day in small quantities
5. If a defect is found, the line stops immediately (andon cord)

**The Kanban system:**
Kanban (Japanese for "signboard") is a visual scheduling system:

```
Workstation B uses Part X from a bin.
When the bin is empty:
  1. The empty bin (with a Kanban card) is sent to Workstation A
  2. Workstation A sees the empty bin → produces more Part X
  3. When the bin is full, it's sent back to Workstation B

No central scheduling needed. Production is pulled by actual consumption.
```

**Physical Kanban example — two-bin system:**
```
Bin 1 (Active):  [■■■■■■□□□□]  ← Currently using from this bin
Bin 2 (Reserve): [■■■■■■■■■■]  ← Full, waiting

When Bin 1 is empty:
  → Start using Bin 2
  → Send Bin 1 to supplier/production for refill
  → Bin 1 returns full before Bin 2 is empty (if sized correctly)
```

**Real-life example:**
Dell revolutionized PC manufacturing in the 1990s with a JIT build-to-order model. When you ordered a Dell computer online:
1. Your order triggered component pulls from supplier bins at Dell's factory
2. Most components were within 15 minutes of the assembly line
3. Your specific computer was assembled, tested, and shipped within 48 hours
4. Dell held approximately 4 days of inventory vs. competitors' 30-60 days

This gave Dell a massive cash flow advantage — they collected payment from customers before paying suppliers.

### 13.3 Risks of JIT

JIT works brilliantly — until it doesn't.

**Real-life example — the 2011 Thailand floods:**
In October 2011, massive floods in Thailand destroyed hundreds of factories, including major hard drive manufacturers. Companies running JIT had zero buffer stock. Western Digital and Seagate lost months of production. Hard drive prices doubled overnight and took over a year to normalize. Companies like HP and Dell couldn't build computers because they had no hard drive inventory buffer.

**Real-life example — COVID-19 supply chain disruption:**
The pandemic exposed JIT vulnerability across industries:
- Auto manufacturers couldn't get chips (they had cancelled orders during lockdown, then couldn't get back in the queue)
- Hospitals ran out of PPE (gloves, masks, gowns) because they held minimal inventory
- Grocery stores couldn't stock shelves because their JIT replenishment systems assumed steady demand

**Post-COVID trend:** Many companies are shifting from "just-in-time" to "just-in-case" — carrying more safety stock of critical components.

### 13.4 Finding the Balance

The goal isn't maximum inventory or minimum inventory. It's **optimal** inventory.

```
                   Cost
                    ▲
                    │
   Total Cost ───  │    ╲        ╱
                    │     ╲      ╱
                    │      ╲    ╱
                    │       ╲  ╱
                    │        ╲╱  ← Optimal
   Holding Cost ── │        ╱╲
                    │       ╱  ╲
                    │      ╱    ╲
   Shortage Cost ─  │     ╱      ╲
                    │    ╱        ╲
                    └──────────────────▶
                    Low     ◄──►     High
                         Inventory Level
```

---

## Chapter 14: Inventory for Different Industries

### 14.1 Retail

**Unique challenges:**
- Thousands to millions of SKUs
- Seasonal demand swings (holiday, back-to-school, weather)
- Omnichannel fulfillment (online, in-store pickup, ship from store)
- Perishability (fashion items have a "season," not just food)
- Markdown optimization (when and how much to discount slow sellers)

**Real-life example — Zara's fast fashion model:**
While traditional retailers plan collections 6-12 months ahead, Zara:
- Designs to shelf in 2-3 weeks
- Produces in small batches (intentional scarcity)
- Ships new items to stores twice per week
- If an item sells well, they produce more. If not, they move on.
- 85% of inventory sells at full price (industry average: 60%)

Their entire model is built on minimal inventory risk and fast response to actual demand.

### 14.2 Manufacturing

**Unique challenges:**
- Bill of Materials (BOM) management — a product may need 500+ components
- Production scheduling tied to material availability
- Quality holds (quarantine inventory until QC passes)
- Lot traceability (which batch of raw material went into which finished product?)

**Material Requirements Planning (MRP):**
MRP calculates what materials are needed, in what quantities, and when.

```
Product: Wooden Table
BOM:
  1x Table top (oak, 120cm × 80cm)
  4x Table legs (oak, 72cm)
  16x Wood screws (#8 × 1.5")
  4x Rubber feet
  1x Finish (250ml polyurethane)

Customer orders 50 tables, delivery in 4 weeks.

MRP explosion:
  50 table tops needed
  - In stock: 20
  - Need to produce: 30
  - Raw oak required: 30 × 0.96 sq meters = 28.8 sq meters
  - Oak lead time: 1 week
  → Order oak by end of week 1

  200 table legs needed (50 × 4)
  - In stock: 80
  - Need to produce: 120
  - Raw oak required: 120 × 0.15 sq meters = 18 sq meters
  → Order with table top oak

  800 wood screws (50 × 16)
  - In stock: 2,000
  - No order needed ✓

  200 rubber feet (50 × 4)
  - In stock: 50
  - Need: 150
  - Supplier lead time: 3 days
  → Order by end of week 3

  50 × 250ml finish (12.5 liters)
  - In stock: 8 liters
  - Need: 4.5 liters
  - Supplier lead time: 2 days
  → Order by end of week 3
```

### 14.3 Healthcare

**Unique challenges:**
- Patient safety is paramount (wrong item = potential death)
- Expiration management (FEFO is legally required)
- Recall traceability (must trace every item to every patient)
- Par level management (each nursing unit has standard stock levels)
- Controlled substances (strict chain-of-custody, DEA regulations)
- Implant tracking (serial number tied to patient record permanently)

**Real-life example — operating room inventory:**
A hospital might stock $500,000+ of inventory in each operating room suite:
- Surgical instruments (tracked, sterilized, reused)
- Implants (joint replacements, screws, plates — expensive, serialized)
- Consumables (sutures, gauze, gloves — restocked daily)
- Medications (anesthetics, antibiotics — temperature controlled)

When a surgeon uses a hip implant:
1. The implant barcode is scanned
2. Patient record updated with implant serial number, lot number, manufacturer
3. Inventory decremented
4. If inventory drops below par → automatic reorder
5. If manufacturer issues a recall → system identifies every patient with that lot number

### 14.4 Food and Beverage

**Unique challenges:**
- Perishability (strict sell-by, use-by, best-before dates)
- Cold chain management (temperature monitoring from farm to shelf)
- Regulatory compliance (FDA, USDA, HACCP)
- Lot traceability (foodborne illness outbreak → trace to source farm)
- High SKU count with variants (size, flavor, packaging)

**Real-life example — Chipotle's food safety tracking:**
After E. coli outbreaks in 2015, Chipotle implemented comprehensive lot tracking:
- Every ingredient is tracked from supplier through to restaurant
- DNA-based testing of ingredients before they enter supply chain
- If a customer gets sick, they can trace which restaurant, which batch of ingredients, which supplier, and which farm
- This level of traceability is expensive but essential

### 14.5 Construction

**Unique challenges:**
- Project-based inventory (materials tied to specific job sites)
- Weather and site condition impacts
- Theft (construction sites are high-theft environments)
- Waste management (ordering 10% extra for cutting waste is standard)
- Tool tracking (expensive power tools move between sites)

**Real-life example:**
A large construction company tracked tool usage with RFID tags and discovered:
- They owned 1,200 circular saws but could only locate 800
- They were renting 50 additional saws per month because they "didn't have enough"
- After implementing RFID tracking, they found lost tools worth $2 million
- Rental costs dropped 80%

---

## Chapter 15: KPIs and Analytics

### 15.1 Key Performance Indicators

#### Inventory Turnover
```
Inventory Turnover = Cost of Goods Sold / Average Inventory Value

Example:
  COGS: $5,000,000
  Average inventory: $1,000,000
  Turnover = 5.0 (inventory "turns" 5 times per year)
```

**Industry benchmarks:**
| Industry | Typical Turnover |
|----------|-----------------|
| Grocery | 14-20 |
| Fast fashion | 8-12 |
| General retail | 4-6 |
| Industrial distributor | 3-5 |
| Aerospace/defense | 1-3 |
| Fine jewelry | 1-2 |

**Real-life example:**
Walmart's inventory turnover is approximately 8.5. This means their entire inventory sells and is replaced every ~43 days. In contrast, a luxury watch dealer might turn inventory once per year — each watch sits in the case for an average of 12 months before selling.

#### Days of Supply (DOS)
```
Days of Supply = Average Inventory / Average Daily Usage

Example:
  Inventory: $1,000,000
  Daily COGS: $13,700 ($5M / 365)
  DOS = 73 days

Meaning: At current sales rates, you have 73 days of inventory on hand.
```

#### Fill Rate
```
Fill Rate = (Orders Shipped Complete / Total Orders) × 100

Example:
  Total orders this month: 10,000
  Orders shipped complete (all items, on time): 9,500
  Fill rate = 95%
```

Target fill rates:
- A items: 97-99%
- B items: 93-97%
- C items: 85-93%

#### Carrying Cost Percentage
```
Carrying Cost % = Annual Carrying Costs / Average Inventory Value × 100

Example:
  Warehouse rent: $200,000
  Insurance: $30,000
  Labor (inventory management): $150,000
  Depreciation/obsolescence: $100,000
  Capital cost (opportunity): $150,000
  Total carrying cost: $630,000

  Average inventory value: $2,000,000
  Carrying cost %: $630,000 / $2,000,000 = 31.5%
```

#### Inventory Accuracy Rate
```
Accuracy = (Correct Counts / Total Counts) × 100
Target: 97%+ for well-managed operations
```

#### Dead Stock Percentage
```
Dead Stock % = (Value of items with no sales in 12 months / Total inventory value) × 100

Under 5% is healthy. Over 10% needs immediate attention.
```

### 15.2 Dashboard Example

A well-designed inventory dashboard shows:

```
┌─────────────────────────────────────────────────────────────┐
│                  INVENTORY DASHBOARD                         │
│                  Date: 2024-11-20                            │
├──────────────┬──────────────┬──────────────┬───────────────┤
│ Total Value  │ Turnover     │ Fill Rate    │ Accuracy      │
│ $4.2M       │ 6.3x        │ 96.8%        │ 98.2%         │
│ ▲ 3% MoM    │ ▲ 0.4 MoM   │ ▼ 0.5% MoM  │ ▲ 0.3% MoM   │
├──────────────┴──────────────┴──────────────┴───────────────┤
│                                                             │
│ ALERTS                                                      │
│ ⚠ 23 SKUs below reorder point                              │
│ ⚠ 8 SKUs with zero stock (stockout)                        │
│ ⚠ 145 SKUs with no movement in 90+ days                    │
│ ⚠ 12 purchase orders overdue                                │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│ INVENTORY BY CATEGORY              │ TOP 5 BY VALUE         │
│                                    │                        │
│ Electronics:  $1.8M (43%)          │ 1. Server Rack  $320K  │
│ Furniture:    $0.9M (21%)          │ 2. Laptop Pro   $180K  │
│ Office:       $0.7M (17%)          │ 3. Monitor 4K   $140K  │
│ Consumables:  $0.5M (12%)          │ 4. Office Desk  $95K   │
│ Other:        $0.3M (7%)           │ 5. Network SW   $88K   │
│                                    │                        │
├────────────────────────────────────┴────────────────────────┤
│ AGING ANALYSIS                                              │
│                                                             │
│ 0-30 days:   $2.1M  ██████████████████████  (50%)          │
│ 31-60 days:  $1.0M  ██████████  (24%)                      │
│ 61-90 days:  $0.5M  █████  (12%)                           │
│ 91-180 days: $0.3M  ███  (7%)                              │
│ 180+ days:   $0.3M  ███  (7%) ← Review for write-off      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Chapter 16: Compliance, Auditing, and Regulations

### 16.1 Sarbanes-Oxley (SOX) — US Public Companies

Section 404 requires internal controls over financial reporting, including inventory.

**What this means for inventory:**
- Inventory counts must be auditable
- System access controls (who can adjust inventory? who approves write-offs?)
- Segregation of duties (the person who orders can't also receive)
- Documentation of inventory procedures
- Evidence that controls are tested regularly

### 16.2 GAAP and IFRS Inventory Standards

**ASC 330 (US GAAP) / IAS 2 (IFRS):**
- Inventory must be valued at the **lower of cost or net realizable value**
- If an item's market value drops below what you paid, you must write it down
- Write-downs must be disclosed in financial statements

**Example:**
```
You purchased 1,000 widgets at $10 each = $10,000
Market value drops to $7 each = $7,000

You must write down inventory by $3,000 even though you haven't sold anything.
This $3,000 hits your income statement as a loss.
```

### 16.3 ISO 55000 — Asset Management Standard

The international standard for asset management. Not legally required, but demonstrates best practices.

**Key principles:**
- Asset management must align with organizational objectives
- Leadership commitment required
- Risk-based thinking
- Lifecycle approach (cradle to grave)
- Continuous improvement

### 16.4 Industry-Specific Regulations

| Industry | Regulation | Inventory Impact |
|----------|-----------|-----------------|
| Food | FDA FSMA | Full lot traceability from farm to fork |
| Pharma | FDA 21 CFR Part 211 | Serialization, temperature tracking, recall capability |
| Medical devices | FDA 21 CFR Part 820 | Device tracking, UDI (Unique Device Identification) |
| Defense | DFARS/ITAR | Controlled items tracking, export compliance |
| Chemicals | OSHA/EPA | Hazmat inventory, SDS management, quantity limits |
| Auto | TREAD Act | Defect tracking, recall traceability by VIN |

**Real-life example — pharmaceutical serialization:**
The Drug Supply Chain Security Act (DSCSA) requires that by 2024, every individual prescription drug package must have a unique serial number tracked throughout the supply chain. This means:
- Manufacturers serialize every bottle/box at the packaging line
- Wholesalers scan and verify each unit when received and shipped
- Pharmacies verify each unit against a national database before dispensing
- Goal: Prevent counterfeit drugs (estimated 10-30% of drugs in developing countries are counterfeit)

---

# PART VII: IMPLEMENTATION GUIDE

---

## Chapter 17: Building Your Inventory Management System

### 17.1 Phase 1: Foundation (Weeks 1-4)

**Step 1: Audit your current state**
- How many SKUs do you have?
- Where is inventory stored?
- What's your current accuracy?
- What are your biggest pain points?

**Step 2: Define your requirements**
```
Must-have:
  □ Real-time stock levels
  □ Barcode scanning
  □ Reorder alerts
  □ Multiple location support
  □ Integration with accounting

Nice-to-have:
  □ Mobile app
  □ Demand forecasting
  □ Lot/serial tracking
  □ Customer portal

Not needed:
  □ Manufacturing/BOM
  □ Warehouse robotics
  □ AI-powered optimization
```

**Step 3: Select your system**

| Business Size | Recommended Starting Point |
|--------------|---------------------------|
| 1-10 employees, <500 SKUs | Spreadsheet + barcode scanner |
| 10-50 employees, 500-5,000 SKUs | Cloud inventory software (inFlow, Sortly, Cin7) |
| 50-200 employees, 5,000-50,000 SKUs | ERP system (Odoo, ERPNext, NetSuite) |
| 200+ employees, 50,000+ SKUs | Enterprise ERP + WMS (SAP, Oracle, Manhattan) |

### 17.2 Phase 2: Data Setup (Weeks 5-8)

**The hardest part.** Garbage in = garbage out.

**Master data cleanup:**
- Standardize item descriptions (no more "widget" vs "Widget" vs "WIDGET blue")
- Assign consistent SKUs
- Verify unit of measure (is it sold by the each, pack, case, pallet?)
- Set up categories and classifications
- Enter accurate costs
- Define storage locations

**Real-life tip:**
Budget 2-3x more time for data cleanup than you think. It always takes longer. Every company that has implemented an inventory system says the same thing: "We underestimated the data migration effort."

### 17.3 Phase 3: Process Design (Weeks 9-12)

Document every process:
- How will items be received?
- Who scans what, when?
- How are pick lists generated?
- When are cycle counts performed?
- Who can adjust inventory? What approvals are needed?
- How are returns processed?
- When are reports reviewed?

### 17.4 Phase 4: Go Live and Stabilize (Weeks 13-16)

- Full physical count before go-live (establish accurate baseline)
- Train all users
- Run parallel systems for 1-2 weeks if possible
- Daily reconciliation in first week
- Expect productivity to DROP initially (learning curve)
- Weekly check-ins to address issues

### 17.5 Phase 5: Optimize (Ongoing)

- Refine reorder points based on actual data
- Implement ABC analysis and adjust policies
- Introduce cycle counting
- Analyze dead stock and take action
- Review and improve picking efficiency
- Add integrations (accounting, e-commerce, shipping)

---

## Chapter 18: Common Mistakes and How to Avoid Them

### Mistake 1: Treating Inventory Management as an IT Project
It's a **business process** change that happens to use technology. The system is only as good as the processes and people using it.

### Mistake 2: Not Counting Frequently Enough
"We'll do a physical count at year-end" means 364 days of accumulating errors. Implement cycle counting.

### Mistake 3: Ignoring Carrying Costs
"We got a great deal on 10,000 units!" Did you factor in the $25,000/year it costs to store them?

### Mistake 4: Over-Relying on Safety Stock
Safety stock is a band-aid. The real fix is reducing lead time variability and improving forecast accuracy.

### Mistake 5: Not Training Staff
A $500,000 system operated by untrained staff produces $0 in value.

### Mistake 6: Perfect Data Paralysis
Don't wait for perfect data to start. Start with what you have, count frequently, and improve over time. 80% accurate data is infinitely better than no data.

### Mistake 7: Not Measuring
If you don't track accuracy, turnover, and fill rate, you can't improve. Establish baselines and track trends.

### Mistake 8: One-Size-Fits-All Policies
Your $50,000 server does not need the same tracking as your $2 pen. Use ABC classification and apply proportional effort.

---

# GLOSSARY

| Term | Definition |
|------|-----------|
| **ABC Analysis** | Classification of items by value (A=high, B=medium, C=low) |
| **AS/RS** | Automated Storage and Retrieval System |
| **BOM** | Bill of Materials — list of components to make a product |
| **Carrying Cost** | Total cost of holding inventory (storage, capital, risk, insurance) |
| **CMMS** | Computerized Maintenance Management System |
| **COGS** | Cost of Goods Sold |
| **Cycle Count** | Counting a portion of inventory regularly instead of all at once |
| **Dead Stock** | Inventory with no sales or movement for an extended period |
| **DOM** | Distributed Order Management |
| **EOQ** | Economic Order Quantity — optimal order size |
| **ERP** | Enterprise Resource Planning — integrated business software |
| **FEFO** | First-Expired, First-Out |
| **FIFO** | First-In, First-Out |
| **Fill Rate** | Percentage of orders shipped complete and on time |
| **JIT** | Just-In-Time — minimizing inventory by ordering close to demand |
| **Kanban** | Visual scheduling system that pulls production based on consumption |
| **Lead Time** | Time between placing an order and receiving it |
| **LIFO** | Last-In, First-Out |
| **MAPE** | Mean Absolute Percentage Error (forecast accuracy) |
| **MRO** | Maintenance, Repair, and Operations supplies |
| **MRP** | Material Requirements Planning |
| **MTBF** | Mean Time Between Failures |
| **MTTR** | Mean Time To Repair |
| **NRV** | Net Realizable Value — estimated selling price minus costs to sell |
| **OEE** | Overall Equipment Effectiveness |
| **Par Level** | The standard quantity to maintain at a location |
| **ROP** | Reorder Point — inventory level that triggers a new order |
| **Safety Stock** | Buffer inventory to protect against demand/supply uncertainty |
| **Shrinkage** | Loss of inventory due to theft, damage, or error |
| **SKU** | Stock Keeping Unit — unique identifier for each product variant |
| **Slotting** | Determining optimal storage locations for items |
| **TCO** | Total Cost of Ownership |
| **UPC** | Universal Product Code (barcode standard) |
| **VMI** | Vendor-Managed Inventory |
| **WIP** | Work-In-Progress |
| **WMS** | Warehouse Management System |

---

# FURTHER READING

**Books:**
- *Inventory Management Explained* — David J. Piasecki
- *World-Class Warehousing and Material Handling* — Edward Frazelle
- *The Goal* — Eliyahu Goldratt (a novel about manufacturing and constraints)
- *Toyota Production System* — Taiichi Ohno
- *Factory Physics* — Hopp and Spearman (academic, comprehensive)

**Standards and Organizations:**
- APICS/ASCM (Association for Supply Chain Management) — certifications: CPIM, CSCP
- GS1 — Global barcode and RFID standards
- ISA-95 — Manufacturing integration standards
- ISO 55000 — Asset management standards

**Open Source Software to Practice With:**
- Odoo (ERP with full inventory module)
- ERPNext (ERP with inventory, asset tracking, manufacturing)
- PartKeepr (electronic parts inventory)
- Snipe-IT (IT asset management)

---

*This guide covers the essential knowledge for understanding inventory management and asset tracking from fundamentals through advanced implementation. The field is vast and constantly evolving with new technology (AI-driven demand forecasting, autonomous warehouses, blockchain-based supply chain tracking), but the core principles outlined here have remained stable for decades and will continue to be relevant.*
