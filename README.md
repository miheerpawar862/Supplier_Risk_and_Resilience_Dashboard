# Zipline Component Risk Scoring Dashboard

An interactive **Global Supply Management (GSM) risk-scoring dashboard** designed to evaluate supply disruption exposure across drone manufacturing components using configurable scoring logic.

This tool helps simulate sourcing decisions using:

* Lead-time volatility
* Supplier capacity responsiveness
* Geographic concentration exposure
* Component criticality
* Priority-based sourcing recommendations

The dashboard is fully configurable and supports editable scoring thresholds directly from the UI.

---

# Project Purpose

This dashboard models how supply chain teams evaluate **component-level disruption risk** and translate it into sourcing strategy actions.

It answers questions like:

* Which components are most disruption-sensitive?
* Where should we dual-source?
* Which components require safety stock?
* Which items need executive sourcing attention?

It is designed as a **portfolio-level supplier resilience decision tool**.

---

# Features

### Level 1 Risk Engine

Evaluates component disruption risk using three pillars:

```
Composite Risk =
0.30 × Lead-Time Volatility
+ 0.30 × Capacity Responsiveness
+ 0.40 × Geographic Concentration
```

---

### Priority Score Model

Applies production impact weighting:

```
Priority Score =
Composite Risk × Criticality
```

Outputs sourcing recommendations:

| Priority Score | Recommendation              |
| -------------- | --------------------------- |
| < 8            | Monitor                     |
| 8–14           | Dual-source candidate       |
| 15–19          | Safety stock required       |
| ≥ 20           | Strategic redesign priority |

---

### Editable Scoring Framework Tab

Users can modify:

* Lead-time volatility thresholds
* Supplier count scoring logic
* Geographic exposure scoring bands
* Composite risk weights
* Criticality mapping
* Recommendation thresholds

This enables scenario simulation across sourcing strategies.

---

# Folder Structure

```
zipline_component_risk_dashboard/
│
├── index.html
├── README.md
│
└── data/
    ├── base_rows.js
    └── defaults.js
```

---

# How to Run the Dashboard

1. Download the repository
2. Keep folder structure unchanged
3. Open:

```
index.html
```

inside:

* Chrome
* Edge
* Firefox

No installation required ✅
No internet required ✅

---

# Updating Component Data

Edit:

```
data/base_rows.js
```

Example entry:

```
{
  id: "AF-01",
  component: "Carbon Fiber Composite Fuselage",
  category: "Airframe & Structure",
  criticality_label: "High",
  viable_suppliers: 6
}
```

Refresh browser after saving changes.

---

# Updating Default Scoring Logic

Edit:

```
data/defaults.js
```

Example:

```
wtLead: 0.30
wtCap: 0.30
wtGeo: 0.40
```

These control composite risk weighting.

---

# Scoring Methodology Overview

## Level 0 — Inputs

Raw inputs:

* Normal lead time
* Peak lead time
* Supplier count
* Geography exposure
* Criticality

---

## Level 1 — Pillar Scores

Converted into 1–5 scale:

| Pillar                   | Meaning               |
| ------------------------ | --------------------- |
| Lead-time volatility     | shortage sensitivity  |
| Capacity responsiveness  | supplier flexibility  |
| Geographic concentration | geopolitical exposure |

---

## Level 2 — Composite Risk Score

Measures probability of disruption.

```
Range: 1 → 5
```

---

## Level 3 — Priority Score

Measures production impact severity.

```
Priority = Composite × Criticality
```

---

## Level 4 — Recommendation Engine

Translates risk into sourcing action.

Outputs:

* Monitor
* Dual-source readiness
* Safety stock planning
* Strategic redesign candidates

---

# Example Component Output

Example:

```
Component:
Carbon Fiber Composite Fuselage

Composite Risk:
2.3

Criticality:
4

Priority Score:
9.2

Recommendation:
Dual-source candidate
```

---

# Why This Dashboard Matters

Modern supply chains must evaluate both:

```
Probability of disruption
+
Impact of disruption
```

This tool combines both into a single sourcing prioritization workflow.

---

# Intended Use Cases

Suitable for:

* Supply chain students
* Global Supply Managers
* Procurement strategy teams
* Supplier resilience modeling
* Academic research projects
* Portfolio sourcing simulations

---

# Future Enhancements (Planned)

Upcoming improvements:

* Cost exposure scoring layer
* BOM percentage integration
* Supplier concentration index
* Regional geopolitical risk engine
* Scenario comparison mode
* Export-to-Excel functionality

---

# Author

Miheer Pawar
Purdue University — Master’s in Engineering Management
Supply Chain Analytics | Global Supply Management | Risk Modeling

---

# License

Academic / educational use recommended.
Commercial usage optional with attribution.
