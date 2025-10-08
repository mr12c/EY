# 📦 Understanding SKUs (Stock Keeping Units)

### 🧩 What is an SKU?

**SKU** stands for **Stock Keeping Unit** — a unique alphanumeric code assigned to every distinct product a company sells or manufactures.
It helps businesses **track inventory**, **manage sales**, and **identify product variants** efficiently.

Each SKU represents a **specific combination** of product attributes such as:

* Size
* Color
* Material
* Voltage (for electrical items)
* Packaging type
* Any other technical or physical specification

---

### 🏭 Example: Industrial Cables (Asian Paints FMCG Case)

Let’s say **Asian Paints** produces various **wires and cables** for industrial use.
Each variant is slightly different in material, length, or voltage — so each gets its own SKU.

| Product Name              | Voltage | Length | Material | Coating | SKU Code           |
| ------------------------- | ------- | ------ | -------- | ------- | ------------------ |
| FlameGuard Copper Cable   | 1.1 kV  | 100 m  | Copper   | FR      | **AP-CU-FR-100**   |
| FlameGuard Copper Cable   | 11 kV   | 200 m  | Copper   | FR      | **AP-CU-FR-200**   |
| FlameGuard Aluminum Cable | 11 kV   | 100 m  | Aluminum | FRLS    | **AP-AL-FRLS-100** |

So, if a customer (or government RFP) asks for:

> “11 kV, Flame Retardant Low Smoke (FRLS) aluminum cable, 100 meters”

→ The correct match is **AP-AL-FRLS-100**.

---

### 🧠 Why SKUs Matter

1. **Inventory Management** – Each SKU tracks stock levels and movement in warehouses.
2. **Faster Order Fulfillment** – Employees can quickly identify and ship the exact product variant.
3. **Sales Analysis** – Companies can see which SKUs sell best and forecast demand.
4. **RFP Matching (Hackathon Context)** – The AI must automatically match RFP product requirements to the correct SKU.

---

### 💡 Example of “Spec Match %” in an RFP

Suppose an RFP demands:

```
Copper Wire, 1.1 kV, 100m length, Flame Retardant (FR)
```

And the database has:

| SKU            | Voltage | Material | Length | Coating | Spec Match % |
| -------------- | ------- | -------- | ------ | ------- | ------------ |
| AP-CU-FR-100   | 1.1 kV  | Copper   | 100m   | FR      | **100%**     |
| AP-AL-FRLS-100 | 1.1 kV  | Aluminum | 100m   | FRLS    | 75%          |
| AP-CU-FR-200   | 1.1 kV  | Copper   | 200m   | FR      | 85%          |

✅ The top SKU (AP-CU-FR-100) is a **perfect match**.
The AI’s job is to automatically calculate these scores and recommend the best fit.

---

### 🧾 Summary

* **SKU = Unique product ID** for every variant.
* **Purpose:** Efficient tracking, sales, and specification matching.
* **Hackathon Relevance:** AI must read RFP specs → search SKU database → compute best matches automatically.

In essence:

> *Think of SKUs as product DNA — every variant has its own unique code, and matching it right wins the deal.*

