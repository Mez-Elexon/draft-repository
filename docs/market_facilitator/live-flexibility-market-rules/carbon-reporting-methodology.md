# Carbon Reporting Methodology

<details>

<summary>Summary</summary>

| Identifier                | FMR-CR                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Title                     | Carbon Reporting Methodology                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Published version number  | 0.1                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Status                    | Draft for consultation                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Audience                  | DNOs                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Expertise                 | Carbon Reporting, C31e Reporting                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Description               | <p>What?</p><p>This rule sets out the common methodology for calculating and displaying the carbon impact of DNO procured flexibility services<br>How?</p><p>It sets out a detailed methodology and assumptions to make as part of the annual reporting set out in licence condition 31E.<br>Who?</p><p>This rule impact all DNOs<br>When?</p><p>This rule come into force in January 2026<br>Why?</p><p>To drive a common and consistent view of the carbon impact.</p> |
| Change since last version | Translation of Open Networks methodology. Minimal Changes                                                                                                                                                                                                                                                                                                                                                                                                                |

</details>

{% include "../../../.gitbook/includes/legal-intro.md" %}

## 1. Core rule

### 1.2. Methodology

&#x20;DNO[^DNO]s will perform the calculation by technology category without input from providers, except to confirm the technology category where required.

The calculation includes direct (such as fuel combustion) and consequential carbon impacts (such as battery charging) but excludes indirect impacts (such as embedded emissions in the materials).

The general formula varies by generation, storage (export), and demand / storage (imports).

In the formulae:

· kWh is the energy delivered (as opposed to requested) measured at the site of the resource;

· η is the energy conversion efficiency of the generator _g_ or storage _s;_

· EF is the fuel emission factor;

· GI is the grid intensity factor at import _i_, export _e_, or at turndown _td;_ and

· Payback% is the consequential increase in load or generation following a turn-down or turn-up event respectively.

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top">Solution</td><td valign="top">Export increase / import decrease</td><td valign="top">Export decrease / import increase</td></tr><tr><td valign="top">Generation</td><td valign="top"><p>Combustion of fuel (direct) = +kWh/η<sub>g</sub> x EF</p><p>displace grid generation (consequential) = -kWh x GI</p></td><td valign="top"><p>Reduced combustion of fuel (direct) = -kWh/η<sub>g</sub> x EF</p><p>replaced by more grid generation (consequential) = +kWh x GI</p></td></tr><tr><td valign="top">Storage (export)</td><td valign="top"><p>Input energy (consequential) = +kWh/η<sub>s</sub> x GI<sub>i</sub> (if from grid), or +(kWh/η<sub>s</sub>)/η<sub>g</sub> x EF (if from generator)</p><p>displace grid generation (consequential) = -kWh x GI<sub>e</sub></p></td><td valign="top"><p>Replaced by more grid generation (consequential) = +kWh x GI</p><p>displace grid generation (consequential) =</p><p>-kWh x GI</p></td></tr><tr><td valign="top">Demand or Storage (import)</td><td valign="top"><p>Reduced grid imports (direct) =</p><p>-kWh x GI<sub>td</sub></p><p>increased grid imports (consequential) = +kWh x payback% x GI<sub>i</sub></p></td><td valign="top"><p>Increased grid imports (direct) = +kWh x GI</p><p>reduced grid imports (consequential) = +kWh x payback% x GI</p></td></tr></tbody></table>

#### **Notes**

Generation

· When a generator is instructed to export it burns more fuel and displaces the marginal grid generation.

· When a generator is instructed to reduce exports, it burns less fuel with the reduction replaced by an increase from the marginal grid generation. For a renewable generator assume a zero EF.

· If the generator is displacing imports, the carbon impact is the same as the equivalent amount exported directly to the grid.

· For bioenergy, report on both inclusive and exclusive of biogenic CO<sub>2</sub> released during burning of biomass and biofuels by using the relevant emission factors.\\

Storage (export)

· When storage is instructed to increase exports, it displaces the marginal grid generation. The source of that energy and the efficiency of energy conversion is also counted.

· When storage is instructed to reduce exports, the calculation assumes a temporal shifting of that export.

· If storage input energy is physically supplied from a renewable generator assume zero carbon, this does not apply to non-physical supplies of low carbon electricity, which should assume grid intensity.

· If storage discharge is displacing imports, the carbon impact is the same as the equivalent amount exported directly to the grid.

· Where DNOs are unsure whether storage is providing export increase or import reduction, use the storage calculation. This ensures carbon impacts are not underestimated and incentivises additional information to be provided.

Demand / storage (import)

· When demand or storage is instructed to reduce imports the reduction in energy is replaced by the marginal grid generation. There is a consequential rebound in load known as payback.

· When demand or storage is instructed to increase imports the increase in energy is supplied by the marginal grid generation. There is a consequential reduction in load, an equivalent to “payback”.

· If demand is shifted, such as deferred EV charging, then payback% is 100%. Otherwise, assume an associated payback as a percentage of the turn-down energy of 21%. Where DNOs are unsure, assume load shifting. This ensures carbon impacts are not underestimated and incentivises additional information to be provided. For import increase the payback% assumption is 100%.

· Where DNOs are unsure whether storage is providing export increase or import reduction, use the storage calculation. This ensures carbon impacts are not underestimated and incentivises additional information to be provided.

### 1.2. Conversion factors

DNOs should use the conversion factor sources presented in the following table.

The data source used for grid intensity is a static value, all grid intensity factors is therefore equal (except for short-run and long-run factors). In the case of storage, GI<sub>i</sub> = GI<sub>e</sub> and in the case of demand, GI<sub>td</sub>=GI<sub>i</sub>. The different notations in the formula allows for inclusion of time series grid intensity factors in future. See Supporting Notes for further discussion on use of grid intensity factors.

\\

| Factor type           | Source                                                                                                                                                                                                                                                                                                                                                                                                                                          | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Fuel emission factors | BEIS/Defra\[a]                                                                                                                                                                                                                                                                                                                                                                                                                                  | CO2e, Gross CV. Updated annually.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Efficiency            | BEIS/Defra\[b]                                                                                                                                                                                                                                                                                                                                                                                                                                  | The DUKES report is updated annually, however the others are one-off reports.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Grid intensity        | <p>· BEIS Electricity Generation Costs 2020[c] – [A]</p><p>· <a href="https://www.gov.uk/government/statistics/electricity-chapter-5-digest-of-united-kingdom-energy-statistics-dukes">Coal </a><a href="https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/910261/storage-costs-technical-assumptions-2018.pdf">–</a> DUKES[d] – [B]</p><p>· BEIS Storage Costs and Assumptions 2018[e] – [C]</p> | <p>Short-run: EF of natural gas divided by efficiency of an OCGT e.g. based on 2022 EF, 183gCO2e/kWh / 35% = 523gCO2e/kWh.</p><p>Long-run: Average of consumption long-run marginal factors, use most recently updated value rather than forecasts (2021 at time of writing). Irregularly updated.</p><p>Note, long-run refers to interventions that results in sustained change in demand/generation over years. Short-run refers to interventions that result in temporary change in demand/generation.</p> |
| Payback%              | <p>For demand-turn-down: Low Carbon London report[f]</p><p>For demand-turn-up: Open Network working group view</p>                                                                                                                                                                                                                                                                                                                              | <p>Demand-turn-down: From a one-off innovation trial. Assume 21% for reduction services, based on the average of trial events. Assume 100% for load shifting solutions.</p><p>Demand-turn-up: Assume 100%</p>                                                                                                                                                                                                                                                                                                 |

### 1.3. Technology categorisation

The technology categorisations are given in the following table, which maps licence condition 31E technology categories by the relevant technology categories required for selecting the appropriate conversion factor. This is advisory rather than prescribed to allow for some flexibility where the mapping is incomplete.

The licence condition 31E technology categories may be subject to change pending engagement with Ofgem to add additional granularity.

| Licence Condition 31E Technology Categorisation                              | Emissions Factor (and Grid intensity factor)               | Efficiency                                                                               | Demand payback                 |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------ |
| Advanced Fuel (produced via gasification or pyrolysis of biofuel or waste)   |                                                            | Advanced Conversion Technologies \[A]                                                    |                                |
| Biofuel - Biogas from anaerobic digestion (excluding landfill & sewage)      |                                                            | Anaerobic digestion (AD) \[A]                                                            |                                |
| Biofuel - Landfill gas                                                       | Biogas - Landfill gas                                      |                                                                                          |                                |
| Biofuel - Other                                                              | Biogas – Biogas                                            | Energy from Waste (EfW) \[A]                                                             |                                |
| Biofuel - Sewage gas                                                         | Biogas - Biogas                                            |                                                                                          |                                |
| Biomass                                                                      | Biomass - wood logs, wood chips, wood pellets, grass/straw | Biomass – dedicated \[A]                                                                 |                                |
| Demand                                                                       | Grid intensity                                             |                                                                                          | Payback (21%), shifting (100%) |
| Fossil - Brown coal/lignite                                                  | Figures not available                                      |                                                                                          |                                |
| Fossil - Coal gas                                                            |                                                            |                                                                                          |                                |
| Fossil - Gas                                                                 | Gaseous fuels - natural gas                                | OCGT, CCGT, Recip \[A]                                                                   |                                |
| Fossil - Hard coal                                                           | Solid fuels - Coal (electricity generation)                | Coal \[B]                                                                                |                                |
| Fossil - Oil                                                                 | Liquid fuel - Diesel (average biofuel blend)               | Diesel \[A]                                                                              |                                |
| Fossil - Oil shale                                                           |                                                            |                                                                                          |                                |
| Fossil - Other                                                               | Other factors available                                    |                                                                                          |                                |
| Fossil - Peat                                                                |                                                            |                                                                                          |                                |
| Geothermal                                                                   |                                                            |                                                                                          |                                |
| Hydrogen                                                                     |                                                            |                                                                                          |                                |
| Nuclear                                                                      |                                                            |                                                                                          |                                |
| Solar                                                                        |                                                            |                                                                                          |                                |
| Stored Energy (all stored energy irrespective of the original energy source) | Grid intensity                                             | Pumped hydro, CAES, thermal energy storage, Lithium Ion, Zinc, Flow, Sodium Sulphur \[C] |                                |
| Waste Water (flowing water or head of water)                                 |                                                            |                                                                                          |                                |
| Wind                                                                         |                                                            |                                                                                          |                                |
| Other                                                                        |                                                            |                                                                                          |                                |

### 1.4. Report Format

DNOs should include the following paragraph in their Distribution Flexibility Services Procurement Report to summarise the methodology to readers and references this methodology document.

The carbon impact calculation presented in this report follows the standard methodology laid out by the market facilitator. The calculation varies depending on whether the flexibility asset is generation, storage (export), or demand / storage (import). The impacts include direct impacts (such as burning fuel) and consequential impacts (such as demand payback) but not indirect impacts (such as embodied carbon). The conversion factors used are generally industry standard which include grid-intensity, plant efficiencies, fuel emission factors, and payback assumptions. Asset specific factors are not used to maintain consistency between DNO reports which means that the methodology reports an approximation of carbon impacts. The detailed methodology is available on the Market Facilitator Repository \[_insert link to the latest methodology_].

A table in the following format should be included in the Distribution Flexibility Services Procurement Report showing energy (requested and delivered) and carbon impact (broken into direct and consequential). An accompanying narrative should explain what the data shows and use of charts to present the information is encouraged.

Energy delivered can differ to energy requested due to under or over delivery. Over-delivery is capped at 150% (captures over-delivery but excludes scenarios where over delivery may not be a consequence of the dispatch). Delivered energy is used to calculate carbon impacts.

Subject to agreement with Ofgem to update the data template, the carbon impact per dispatch should be added as another column in the template. In addition, technology sub categorisations based on Embedded Capacity Register / G99 should also be added to reflect different solutions within each Licence Condition 31E category, for example if demand is shifted or reduced or the different types of Stored Energy.

For bioenergy, add an additional column to “Direct carbon impact”. In the first of these columns, report on the carbon impact exclusive of biogenic CO<sub>2</sub> using the default emission factors, and in the second column report on the biogenic CO<sub>2</sub> using the “outside of scope” emission factors, from the BEIS/Defra conversion factors (full set). The former calculation nets off the CO<sub>2</sub> released at combustion with the CO<sub>2</sub> absorbed during the growth phase of the bioenergy, whilst the latter calculation reports the CO<sub>2</sub> released at combustion. This is in line with the GHG Protocol guidance for corporate accounting.

Provide the dispatch intensity metric (total carbon impact divided by the total energy delivered).

| Licence condition 31E Technology Category | Requested energy (MWh) | Delivered energy (MWh) | Direct carbon impact (kgCO2e) | Consequential carbon impact (kgCO2e) |
| ----------------------------------------- | ---------------------- | ---------------------- | ----------------------------- | ------------------------------------ |
| Fossil – Gas                              |                        |                        |                               |                                      |
| Demand                                    |                        |                        |                               |                                      |
| Stored Energy                             |                        |                        |                               |                                      |
| …                                         |                        |                        |                               |                                      |
| Total                                     |                        |                        |                               |                                      |

\\

***

\[a] Conversion factors for company reporting - [https://www.gov.uk/government/collections/government-conversion-factors-for-company-reporting](https://www.gov.uk/government/collections/government-conversion-factors-for-company-reporting)

\[b] Conversion factors for company reporting - [https://www.gov.uk/government/collections/government-conversion-factors-for-company-reporting](https://www.gov.uk/government/collections/government-conversion-factors-for-company-reporting)

\[c] Electricity generation costs 2020 - [https://www.gov.uk/government/publications/beis-electricity-generation-costs-2020](https://www.gov.uk/government/publications/beis-electricity-generation-costs-2020)

\[d] DUKES - [https://www.gov.uk/government/statistics/electricity-chapter-5-digest-of-united-kingdom-energy-statistics-dukes](https://www.gov.uk/government/statistics/electricity-chapter-5-digest-of-united-kingdom-energy-statistics-dukes)

\[e] Storage cost and assumptions 2018 - [https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment\_data/file/910261/storage-costs-technical-assumptions-2018.pdf](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/910261/storage-costs-technical-assumptions-2018.pdf)

\[f] Low Carbon London - [LCL-Learning-Report-A7-Distributed-Generation-and-Demand-Side-Response-services-for-smart-Distribution-Networks.pdf (ukpowernetworks.co.uk)](https://innovation.ukpowernetworks.co.uk/wp-content/uploads/2019/05/LCL-Learning-Report-A7-Distributed-Generation-and-Demand-Side-Response-services-for-smart-Distribution-Networks.pdf)

## 2. Implementation details

{% include "../../../.gitbook/includes/implementation-details-dnos.md" %}

Table 1: Implementation requirements

|                                | All DNO Sub-Markets                                                                                                                                         | All NESO Sub-Markets | Innovation Trials |   |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- | ----------------- | - |
| Applicable to Sub-Market       | Yes                                                                                                                                                         | No                   | No                |   |
| Version in use for submarket   | 1.0                                                                                                                                                         |                      |                   |   |
| Effective From                 | 30/01/2026                                                                                                                                                  |                      |                   |   |
| Effective to                   | Null                                                                                                                                                        |                      |                   |   |
| Implementation Requirements    | DNO shall use the methodology as part of reporting under Licence Condition 31E. It may also be used in other contexts, if the appropriate data is available |                      |                   |   |
| Variations Allowed?            | N                                                                                                                                                           |                      |                   |   |
| Terms of variations            | N/A                                                                                                                                                         |                      |                   |   |
| Directly Impacted Stakeholders | DNOs                                                                                                                                                        |                      |                   |   |
|                                |                                                                                                                                                             |                      |                   |   |

### 1.1. Implementation tracking

The DNOs must update the Market Facilitator with the following data (as set out in Table 2) for each Sub-Market in scope of this rule no later than 20 working days after the “Created” date of this Flexibility Market Rule and subsequently within 10 working days of change. This should accurately reflect their implementation of each Sub-Market whilst aligning with the required values as set out in Table 1 above.

\\

Table 2: Implementation tracking requirements

| FMR-CR Version 1.0         | Parameter                                                                                                                                                                                                       | Required value (per Sub-Market) |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| Implementation Status      | <p>Dependent on date:</p><p>· Before Effective From: Not yet started, Implementing, Paused, Implemented</p><p>· Between Effective From and Effective to: Implemented</p><p>· After Effective to: Superseded</p> |                                 |
| Target Implementation Date | No later than Effective From date                                                                                                                                                                               |                                 |

## 2. Flexibility Market Catalogue data

Not used for this rule

## 3. Effectiveness monitoring

The following KPIs (as set out in below) shall be used to track the effectiveness of the rule.

Table 3: Relevant KPIs

| Carbon Reporting Methodology V1.0 KPI 1 | Description                  | Average Carbon Intensity per unit of dispatched Flexibility Services per DNO |
| --------------------------------------- | ---------------------------- | ---------------------------------------------------------------------------- |
| Cadence                                 | Yearly                       |                                                                              |
| Data source                             | DNO C31e Procurement reports |                                                                              |
| What does good look like?               | 0                            |                                                                              |
| Minimum Requirement                     | -                            |                                                                              |

\\

## 4. Glossary

The following definitions are specific to this Flexibility Market Rule. These are supplemented by the definitions in the Market Facilitator Glossary. If there is an inconsistency between definitions, the definition in this document shall prevail.

| Defined Term       | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Conversion factors | Used in this rule as a general term to describe factors that are used in the calculations which can include fuel emission factors, grid intensity factors, and plant efficiency assumptions.                                                                                                                                                                                                                                                                                                                    |
| Grid intensity     | Refers to the carbon intensity of electricity that is imported from the grid in kgCO2e/kWh taking into account the carbon emissions from grid generation, interconnector imports, and potentially network losses.                                                                                                                                                                                                                                                                                               |
| Payback            | Otherwise known as rebound or bounce back, refers to when demand side response load increases after a turn-down event as the site recovers to pre-event conditions, for instance an increase in cooling load in a building having warmed up during the turn-down event. This could also refer to a similar rebound effect following realisation of economic benefits as a result of an energy efficiency saving measure.                                                                                        |
| Reporting Boundary | Defines the scope of the calculation. This can include direct impacts (such as combustion of fuel to generate electricity), consequential impacts (such as the carbon emissions from grid generation to produce and transport electricity imported by a battery), or indirect impacts (such as embedded and end of life emissions attributed to the assets). We also describe narrow or wide boundaries to refer to the extent to which the calculation focuses on direct or whole-life emissions respectively. |

## 5. Amendment record

<table data-header-hidden><thead><tr><th></th><th></th><th></th><th></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td>Version</td><td>Effective From Date</td><td>Document Status</td><td>Description of Changes</td><td valign="top">Change Proposal Reference</td><td valign="top">Market Facilitator Decision Report Ref</td></tr><tr><td>0.1</td><td>30/01/2026</td><td>Draft for Consultation</td><td>Document Created</td><td valign="top">-</td><td valign="top">-</td></tr></tbody></table>

\\

## Annex 1: Associated meta-data

{% content-ref url="snippets/meta-data.md" %}
[meta-data.md](snippets/meta-data.md)
{% endcontent-ref %}

##

[^DNO]: Distribution Network Operator
[^DNOPD]: Distribution Network OperatorPD
