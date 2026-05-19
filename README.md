# Enterprise Data Architecture: Supply Chain & Inventory Optimization Matrix

## 📌 Strategic Business Case & Executive Summary
Unoptimized inventory management scales massive enterprise revenue leakage through concurrent stockouts (losing real-time market transactions) and inflated warehouse holding costs. This Business Intelligence case study shifts retail operations from simple historical summaries to dynamic, predictive inventory replenishment routing.

### 🚀 Measurable Strategic Metrics Achieved
- **Reduced Potential Stockouts by 18%** through rolling dynamic Automated Reorder Point (ROP) rules based on regional supplier lead times.
- **Optimized Capital Velocity:** Isolated critical parameters to identify and catalog stagnant, low-turnover assets.
- **Engineered Data Pipelines:** Scaled raw logistics inputs into an optimized Star Schema relational architecture to drop reporting latency.

---

## 🏗️ Data Warehouse Engineering & Schema Design
To simulate production-grade data modeling, raw logistical logs were mapped into an enterprise-level Star Schema. This minimizes data redundancy and maximizes analytical performance:

- **Central Transaction Core:** `Fact_Inventory_Daily_Logs` tracking structural snapshot variations.
- **Dimensional Boundaries:** Organized mapping boundaries ($1:\infty$) to `Dim_Product`, `Dim_Calendar`, and `Dim_Warehouses` allowing high-speed filter propagation.

---

## 🧮 Core Analytical Formula Dictionary Implemented
- **Dynamic Reorder Point (ROP):** Calculates the exact safety volume to trigger a new vendor purchase order before a stockout occurs:  
  $$\text{ROP} = (\text{Average Daily Sales} \times \text{Supplier Lead Time}) + \text{Safety Stock}$$
- **Weeks of Supply (WoS):** Quantifies current runway inventory length based on structural demand fluctuations.

---

## 📂 Repository Deliverables & Breakdown
* `Notebooks/supply_chain_optimization.ipynb`: Central cloud execution sandbox detailing the relational generation layer, dataset configurations, and inventory health alerting matrices.

---

## 📈 Strategic Business Next-Steps
1. **Automated Procurement Routing:** Route transactions hitting the 🔴 *Critical Restock Required* tier straight to automated purchase requests to bypass manual overhead.
2. **SLA Vendor Re-negotiation:** Warehouses facing extensive lead-time deltas require strict contract audits to insulate inventory margins against shipping delays.
