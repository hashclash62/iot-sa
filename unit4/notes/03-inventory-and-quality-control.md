# Chapter 3: Inventory Management & Quality Control with IIoT

---

## 3.1 Analogy — Library Card System vs RFID Library

In an old library, finding a book means searching card catalogs, walking the shelves, and accepting that you might not know if the book is actually there until you physically check. Managing stock means annual audits where you count every book by hand.

A modern RFID library knows exactly where every book is in real time — including which books are currently checked out, which are misplaced, and which have been on the shelf untouched for 3 years (maybe decommission them). You can query the system at 2am and get an exact answer.

That's the difference IIoT makes for industrial inventory management.

---

## 3.2 Inventory Management Using IIoT (Q3, Q7)

### What is Inventory Management?
Inventory management is the process of tracking raw materials, work-in-progress (WIP), and finished goods — knowing what you have, where it is, how much it costs, and when to reorder.

**The problem IIoT solves:** Traditional inventory management involves periodic manual counts (daily, weekly, monthly) — data is always stale, errors are frequent, and stock-outs or overstock happen because decisions are made on outdated information.

### IIoT Technologies for Inventory:

| Technology | How it works | Best for |
|---|---|---|
| **RFID (Radio Frequency ID)** | Each item has an RFID tag; readers scan tags automatically without line-of-sight | Pallet and case tracking, tooling, work-in-process |
| **Barcode / QR code** | Scan on movement; requires direct scan action | Item-level tracking where RFID cost is high |
| **BLE beacons** | Asset-mounted Bluetooth tags; receivers triangulate location | High-value movable assets (equipment, carts, tools) |
| **Weight/load sensors** | Shelving with load cells detects quantity change | Bins of small parts — count by weight |
| **Computer vision** | Camera + AI counts items on shelves/conveyors | Counting irregular items; no tagging required |

### IIoT Inventory Management System:

```
WAREHOUSE/PRODUCTION FLOOR:
[RFID-tagged pallets/parts]
        | (RFID readers at dock doors, production entry, storage zones)
        ↓
[Warehouse Management System (WMS) + IIoT Platform]
  - Real-time location of every SKU and pallet
  - Auto-decrement stock as materials consumed in production
  - Reorder trigger when stock falls below par level
        ↓
[ERP System (SAP/Oracle)]
  - Procurement orders generated automatically
  - Supplier lead times factored in
  - Cost of inventory calculated in real time
        ↓
[Dashboard: Stock levels, turnover, aging, reorder status]
```

### Benefits of IIoT Inventory Management:
- **Real-time visibility:** Inventory counts are always current — no more "we thought we had it but we don't"
- **Reduced safety stock:** Confidence in real-time data allows safety stock reduction by 20-30% → lower working capital
- **Eliminate stockouts:** Automated reorder triggers before stock runs out → no production stoppages from missing materials
- **Reduce excess inventory:** Analytics identify slow-moving stock → purchasing can reduce order quantities
- **Eliminate manual counting labor:** RFID eliminates annual/quarterly physical count labor (significant for large warehouses)
- **Shrinkage control:** Every item movement is tracked → unauthorized removals detected immediately

---

## 3.3 IIoT Applications in Quality Control (Q8)

Quality control in manufacturing is about catching defects — but the earlier you catch them, the cheaper they are to fix:

```
Cost of defect at different stages:
Design stage:      $1 to fix
Development:       $10 to fix
Manufacturing:     $100 to fix
Customer delivery: $1,000+ to fix (recall, replacement, reputation damage)
```

IIoT moves quality detection from "end of line" to "in-process" — catching defects while the product is still being made, not after.

### IIoT Quality Control Methods:

**1. In-Process Parameter Monitoring**
Monitor the process parameters that determine product quality — not just the product itself.

Example: In plastic injection molding, melt temperature, injection pressure, cooling time, and mold temperature directly determine part dimensions and strength. IIoT monitors these continuously and flags any batch where parameters deviate from the proven "golden settings."

**2. Automated Vision Inspection**
Camera + AI inspects every product on the production line at production speed:
- Surface defects (scratches, cracks, discoloration)
- Dimensional accuracy (part too short/long, hole misplaced)
- Label and packaging correctness
- Assembly verification (is every component present and correctly installed?)

**3. Statistical Process Control (SPC) with Real-Time Data**
Traditional SPC required manual sampling and chart plotting. IIoT SPC:
- Samples every single part (100% inspection vs 1-2% sampling)
- Updates control charts in real time
- Automatically signals when process is drifting toward out-of-control state — operator can correct before defects appear

**4. Traceability**
Every component in every product is tracked — if a batch of purchased components is later found defective, the IIoT system can identify exactly which finished products contain that batch, enabling targeted recall instead of blanket recall.

---

## Quick Summary

- Inventory management IIoT: RFID + sensors + WMS → real-time stock visibility, automated reorder, reduced safety stock
- Key IIoT inventory tech: RFID (pallet/case), BLE beacons (assets), weight sensors (bins), computer vision (no-tag counting)
- Benefits: 20-30% safety stock reduction, zero stockouts, eliminate manual counting labor, shrinkage control
- Quality control IIoT: in-process parameter monitoring, vision inspection, real-time SPC, traceability
- Cost of quality principle: defect caught in manufacturing = $100; at customer = $1,000+ → IIoT shifts detection earlier → massive cost saving
- Traceability enables targeted recall — find exactly which products are affected, not entire production run
