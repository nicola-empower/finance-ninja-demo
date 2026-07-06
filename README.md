# FinanceNinja - Architectural Financial Sandbox & Core UI Spike

[![Stack](https://img.shields.io/badge/Architecture-Vanilla%20%2B%20Tailwind-blue?style=flat-square)](#)
[![Tax Engine](https://img.shields.io/badge/Tax%20Engine-HMRC%20Scotland%202024%2F25-emerald?style=flat-square)](#)
[![Design Philosophy](https://img.shields.io/badge/Design-Calm%20Technology-purple?style=flat-square)](#)

An interactive architectural proof of concept (PoC) built to isolate, test, and validate core computational logic and user experience flow for a client-side personal finance dashboard. 

---

## ⚙️ Architectural Intent & Strategy

In digital engineering, deploying heavy, state-managed frameworks (e.g., Next.js, full React rendering pipelines) too early can introduce premature complexity, unneeded dependency maintenance overhead, and data-schema lock-in. 

This repository serves as a **lightweight static spike**. It was built to achieve three primary engineering goals:
1. **Mathematical Feasibility:** Validating a highly contextual, multi-tier tax-banding engine directly in vanilla runtime client-side scripts.
2. **Design System Validation:** Prototyping a responsive, glassmorphic layout using Tailwind CSS utility patterns to analyze visual weight, structural hierarchy, and cognitive layout ease before committing to a rigid global theme setup.
3. **Database-Less Lifecycle Testing:** Isolating core user interactions (dynamic transactional array pushes, event-driven state triggers, and chart instance lifecycle management) without the configuration friction or infrastructure costs of full authentication or a database layer.

---

## 💎 Core Features & Engineering Highlights

### 📉 Regional Multi-Tier Tax Engine
* Implements a standalone, client-side calculator mirroring **HMRC Scottish Tax Rates (2024/2025 ruleset)**.
* Handles precise progressive calculation steps, computing multi-band thresholds concurrently alongside **National Insurance Class 4 percentages** and threshold caps.
* Dynamically manages conditional student loan deductions (Plan 2 threshold parameters) triggered entirely by client state changes.

### 💰 Business Sinking Fund Allocation
* Moves beyond generic global expense tracking to address granular freelancer operational realities.
* Built-in input tracking logic allows users to configure automated percentage deductions for **Holiday Pay Funds**, **Sickness Reserves**, and **Tax/Maternity Allocations** instantly calculated off annual gross income projections.

### 📊 Fluid Reactive Visualisation
* Harnesses a reactive **Chart.js** integration wrapper managed directly by deep event listeners (`DOMContentLoaded` and form element input hooks).
* Seamless dynamic state sync: saving a transaction inside the modular element array immediately updates statistical totals and triggers direct canvas redraws on both the bar chart (Income vs. Expense) and doughnut graph (Spending Categories) dynamically.

---

## 🎨 Design Philosophy: Calm Technology
The UI is constructed to address choice paralysis and cognitive overload in personal accounting applications:
* **Glassmorphic Accents:** Uses tailored backdrop-filter blurs (`blur(10px)`) and delicate border transparency layers to isolate information groups cleanly without hard blocking grids.
* **Semantic Colour Mapping:** Restricted, deliberate palette usage where green indicates transactional health, red monitors overhead drain, and soft blue frames primary analytical widgets to guide visual navigation naturally.

---

## 🛠️ Stack & Dependencies
To ensure immediate execution with zero local environment setup friction, this sandbox uses edge-delivered CDNs for quick architectural testing:
* **Tailwind CSS Core Wrapper** - Rapid design token scaffolding.
* **Lucide Components** - Lightweight vector iconography.
* **Chart.js Core** - High-performance interactive data visualisations.

---

> 🧠 **Engineering Retrospective:** *This static prototype successfully proved that deep computational multi-tiered tax calculations run effortlessly client-side with minimal memory overhead, validating the structural business requirements before proceeding with a production next-stage migration.*
>
> ### Nicola Berry
