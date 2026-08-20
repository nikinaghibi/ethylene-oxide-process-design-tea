# Ethylene Oxide Process Design & Techno-Economic Analysis

An end-to-end chemical process engineering project focused on the **simulation, preliminary design, equipment sizing, cost estimation, and techno-economic assessment of an industrial ethylene oxide (EO) production process**.

The process was developed and simulated in **Aspen HYSYS**, starting from feed preparation and reaction modeling and extending through absorption, recycle and purge systems, product purification, equipment sizing, capital and operating cost estimation, and long-term economic evaluation.

## Project Overview

Ethylene oxide is an important petrochemical intermediate used in the production of ethylene glycols, polyethylene glycols, ethanolamines, surfactants, and other industrial chemicals.

This project investigates the production of ethylene oxide through the **direct oxidation of ethylene using air**. Particular attention was given to the competing oxidation reactions, reactor design, product recovery, energy requirements, and economic feasibility of the overall process.

The project was developed in two main stages:

1. **Process Simulation & Preliminary Design**
2. **Equipment Sizing, Cost Estimation & Economic Evaluation**

---

## Process Flow

The simulated process consists of the following major sections:

**Air Compression → Intercooling → Ethylene Mixing → Feed Preheating → PFR Reaction → Cooling → Absorption → Second Reaction Stage → Second Absorption → Recycle & Purge → Distillation → Ethylene Oxide Product**

The process incorporates recycle to reduce ethylene losses while a purge stream prevents the accumulation of inert and undesired components.

---

## Process Simulation

The complete process was modeled using **Aspen HYSYS**.

### Components

The simulation includes:

* Ethylene
* Oxygen
* Nitrogen
* Carbon dioxide
* Water
* Ethylene oxide
* Air

### Thermodynamic Model

The **NRTL property package** was selected to represent the system containing both polar and non-polar components.

### Reaction System

Ethylene oxide production was modeled using **heterogeneous catalytic kinetics** in plug flow reactors.

Three reactions were considered:

1. Partial oxidation of ethylene to ethylene oxide
2. Complete oxidation of ethylene to CO₂ and H₂O
3. Further oxidation of ethylene oxide to CO₂ and H₂O

The reactor system was modeled using **PFRs with a fixed catalytic bed**, including catalyst and reactor-bed specifications.

---

## Reactor Design

Initial catalyst and reactor calculations included:

* Catalyst mass estimation from WHSV
* Solid particle density calculation
* Catalyst volume
* Effective packed-bed volume
* Reactor geometry
* Catalyst-bed characteristics

Selected calculated parameters include:

| Parameter              |        Value |
| ---------------------- | -----------: |
| Catalyst bulk density  |   1513 kg/m³ |
| Bed void fraction      |         0.45 |
| Solid particle density |   2751 kg/m³ |
| Catalyst mass          | 158,812.5 kg |
| Catalyst volume        |      57.7 m³ |
| Effective bed volume   |       105 m³ |

Two PFR stages were incorporated into the overall process to increase ethylene utilization.

---

## Feed Preparation

Air is compressed through a **multi-stage compression system** with intercooling before being mixed with the ethylene feed.

The compression train was designed to raise the air pressure progressively to the required reactor operating pressure while controlling the temperature between compression stages.

Five centrifugal compressors were considered throughout the process.

---

## Product Recovery

### Absorption

Two packed absorption columns were used to recover ethylene oxide from the reactor effluent using **water as the solvent**.

The gaseous outlet from the second absorber contains unreacted ethylene and is partially recycled to the feed section.

A recycle/purge configuration was implemented with:

* **Recycle fraction:** 0.70
* **Purge fraction:** 0.30

The calculated overall ethylene conversion after accounting for the recycle and purge system was approximately **38.15%**.

### Distillation

The liquid streams leaving the absorption section were combined and sent to the purification section.

A preliminary column design was first performed using a **Shortcut Column**, followed by rigorous simulation of the main distillation column.

The final column includes a **partial condenser and reboiler**.

The partial condenser allows non-condensable light gases to leave through the vapor outlet while recovering ethylene oxide as the primary liquid product.

### Product Purity

The final liquid product achieved an ethylene oxide mole fraction of:

**0.9863 (98.63 mol%)**

which satisfies the target purity requirement of at least **98 mol% EO**.

The main EO product flow rate was approximately:

**560 kmol/h**

with negligible EO loss through the small overhead vapor stream.

---

## Equipment Sizing

Major process equipment was sized based on the HYSYS simulation results and preliminary chemical engineering design correlations.

Equipment considered includes:

### Heat Exchangers

Eight shell-and-tube heat exchangers were evaluated.

The design included:

* TEMA configuration
* Heat-transfer area
* Overall heat-transfer coefficient
* Tube number and dimensions
* Shell and tube passes
* Tube-side pressure drop
* Shell-side pressure drop

TEMA configurations including **AEL, AEU, and AKU** were selected depending on the thermal service.

### Compressors

Five **centrifugal compressors** were evaluated based on:

* Inlet and outlet pressures
* Compression ratio
* Required shaft power

### Distillation Column

The distillation column was designed using sieve trays.

Representative design specifications include:

| Parameter              |      Value |
| ---------------------- | ---------: |
| Number of trays        |         20 |
| Column diameter        |      1.5 m |
| Tray type              |      Sieve |
| Tray spacing           |     0.55 m |
| Column height          |    16.45 m |
| Pressure drop per tray | 0.3684 kPa |

### Absorption Columns

Two packed absorption towers were designed, including evaluation of:

* Column diameter
* Column height
* Packing type and size
* Packing arrangement
* Pressure drop
* Liquid distributors

### Reactors

The two PFR units were sized based on the catalyst requirement, packed-bed volume, operating pressure, and reactor geometry.

---

## Utilities & Energy Analysis

The major process utilities were quantified from the HYSYS simulation.

The analysis included:

* Cooling water
* Boiler feed water
* Steam
* Compressor electricity
* Absorption water
* Condenser duty
* Reboiler duty

Potential opportunities for **heat integration and energy recovery** were also considered to reduce utility consumption and operating costs.

---

## Equipment Cost Estimation

Equipment purchase and installed costs were estimated and updated to a **2026 cost basis**.

Cost escalation was performed using appropriate cost indices, while installation costs were estimated using **Bare Module factors** and equipment-specific correlations.

### Estimated Equipment Costs

| Equipment Category  | Purchase Cost (2026) | Installed Cost (2026) |
| ------------------- | -------------------: | --------------------: |
| Compressors         |             $12.89 M |              $27.71 M |
| Heat Exchangers     |              $0.23 M |               $0.74 M |
| Distillation Column |              $0.22 M |               $0.92 M |
| Absorption Columns  |              $0.55 M |               $1.75 M |
| Reactors            |              $0.58 M |               $1.77 M |
| **Total**           |         **$14.47 M** |          **$32.90 M** |

*Reactor costs exclude catalyst cost.*

---

## Capital Cost Estimation

Different process-plant capital cost estimation approaches were investigated, including:

* Power Law estimation
* Hill method
* Lang Factor method
* Guthrie / Bare Module approach

The analysis considered both direct and indirect investment requirements, including fixed capital and working capital.

This allowed the process simulation to be extended beyond technical design into a complete preliminary **techno-economic assessment (TEA)**.

---

## Operating Economics

The economic model included:

* Raw material costs
* Utility costs
* Solvent consumption
* Catalyst cost
* Operating expenses
* Depreciation
* Taxes
* Technology licensing
* Financing costs
* Product revenue

For the 2026 economic basis, the simulated plant produces approximately:

**385,655 metric tons of ethylene oxide per year**

with an assumed EO selling price of:

**$1,010/ton**

corresponding to approximately:

**$389.5 million/year in gross product sales.**

Ethylene was identified as the dominant raw-material expense.

---

## Profitability & Cash-Flow Analysis

A long-term economic analysis was performed over a **12-year operating period**.

The analysis considered:

* Fixed Capital Investment (FCI)
* Total Capital Investment (TCI)
* Working Capital Investment
* Annual operating cash flow
* Net Present Value (NPV)
* Minimum Attractive Rate of Return (MARR)
* Investment recovery
* Financing structure
* Inflation
* Technology licensing fees
* Temporary plant shutdown scenarios

A **14% minimum rate of return** was used for discounted cash-flow calculations.

Under the assumptions and prices used in the study, the base-case economic evaluation resulted in a negative NPV, indicating that the simulated process configuration was **not economically attractive under the evaluated economic conditions**.

This result highlights the importance of integrating process simulation with economic analysis: a technically feasible process does not necessarily represent an economically viable industrial investment.

---

## Scenario Analysis

Several economic scenarios were investigated to evaluate the robustness of the project.

These included:

* Inflation effects
* Bank financing
* Bond financing
* Technology licensing costs
* Temporary plant shutdown
* Permanent shutdown versus continued operation

A two-year shutdown scenario was also analyzed to determine whether restarting the facility would be economically preferable to permanent closure.

The scenario analysis demonstrated the strong sensitivity of project economics to operating costs, financing obligations, and plant utilization.

---

## Key Engineering Outcomes

This project integrates several major areas of chemical process engineering:

* Steady-state process simulation
* Thermodynamic model selection
* Heterogeneous catalytic reaction modeling
* PFR design
* Gas compression
* Heat exchanger design
* Absorption
* Recycle and purge design
* Distillation
* Equipment sizing
* Utility estimation
* Equipment costing
* CAPEX estimation
* OPEX analysis
* Discounted cash-flow analysis
* Techno-economic feasibility assessment

Rather than focusing exclusively on process simulation, the project follows the process from **reaction and flowsheet development to preliminary industrial design and economic decision-making**.

---

## Software & Engineering Tools

* **Aspen HYSYS** — Process simulation and equipment modeling
* **Microsoft Excel** — Engineering calculations, costing, and economic analysis
* Chemical engineering design correlations and cost-estimation methods
* CEPCI-based cost escalation
* Bare Module / Guthrie cost estimation

---

## Repository Structure

```text
ethylene-oxide-process-design-tea/
│
├── README.md
│
├── Simulation/
│   └── Ethylene-Oxide-HYSYS-Model
│
├── Reports/
│   ├── Ethylene-Oxide-Process-Simulation.pdf
│   └── Ethylene-Oxide-Equipment-Costing-and-Economics.pdf
│
└── README-assets/
    └── process-flowsheet.png
```

> The exact folder and file names may be adjusted to match the repository structure.

---

## Academic Context

This project was developed as part of the **Preliminary Plant Design / Process Design coursework** at the:

**Department of Chemical and Petroleum Engineering**
**Sharif University of Technology**

The work combines process simulation, preliminary equipment design, cost estimation, and economic feasibility analysis to provide an integrated assessment of an industrial ethylene oxide production process.

---

## Author

**Niki Naghibi**
Chemical Engineering
Sharif University of Technology

---

## Disclaimer

This repository represents an **academic preliminary process-design and techno-economic study**. Equipment dimensions, cost estimates, operating assumptions, and economic results are intended for educational and preliminary evaluation purposes and should not be interpreted as detailed engineering specifications for construction or commercial operation.
