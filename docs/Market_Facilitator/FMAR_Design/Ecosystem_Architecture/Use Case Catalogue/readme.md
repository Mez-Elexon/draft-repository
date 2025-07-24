# FMAR Use Case Catalogue: Complete Summary


| Version | Date       | Changes                      | Author   |
|---------|------------|------------------------------|----------|
| v1.x  | 2025-07-23 | New draft pre-release | MB   |



This document outlines the core use cases for the Flexibility Market Asset Registration (FMAR) solution.

FMAR could support asset registration, unit qualification and data sharing for flexible assets participating in GB flexibility markets.

It is designed to operate through modular components and may leverage a federated architecture via the Data Sharing Infrastructure (DSI). These modules are logical groups of xyz and would have a unified API and reporting layer to support role-based access control on a non-discriminatory basis, underpinned by a common data standard and a shared ontology.

### Module Key

- **SPUM** – Service Provider & User Module  
- **ARM** – Asset Registration Module  
- **PSQM** – Product & Service Qualification Module  
- **GICM** – Grid Interaction & Constraints Module  
- **API Layer** – Federated data access layer for authorised consumers  
- **Reporting Layer** – Common reporting interface drawing from all modules

**🔶 = Expected to be out of scope for go-live. May be prioritised depending on stakeholder workshop outcomes.**
| UC ID    | Use Case Grouping                      | Use Case Name                                          | Description                                                                                                                                              | 🔶 |
|----------|----------------------------------------|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|----|
| UC-01.01 | Customer Onboarding / Offboarding      | Register User                                          | Support the registration of user identities (individuals, organisations) within the FMAR ecosystem, managed via a central trust framework.              |    |
| UC-01.02 | Customer Onboarding / Offboarding      | Register Organisation                                  | Onboard an organisation as a recognised commercial entity, creating an authoritative identity record accessible through FMAR.      |    |
| UC-01.03 | Customer Onboarding / Offboarding      | Update Organisation                                    | Manage the lifecycle of an organisation's core entity data and status within the FMAR ecosystem.                                                                  |    |
| UC-01.04 | Customer Onboarding / Offboarding      | De-register Organisation                               | The formal, auditable process for an organisation to be de-registered from FMAR.                                                                         |    |
| UC-02.01 | Asset Registration & Maintenance       | Maintain Asset Categories                              | (Admin) Define and manage the standard categories and associated schemas for flexible assets recognisable within the FMAR ecosystem.                    |    |
| UC-02.02 | Asset Registration & Maintenance       | Register and Validate Asset                            | The primary process for an FSP or user to submit asset data, ensure it is authentic and conforms to FMAR ontology, resulting in a unique FMAR ID.       |    |
| UC-02.03 | Asset Registration & Maintenance       | De-register Asset                                      | The formal process for removing an asset from FMAR, ensuring auditability and traceability.                                                              |    |
| UC-02.04 | Asset Registration & Maintenance       | Update Asset Details                                   | Modify the attributes of a registered asset, including its link to an FSP, ensuring the updated view is propagated.                                     |    |
| UC-02.05 | Asset Registration & Maintenance       | Export Asset Data                                      | Allow an authorised entity to securely extract its managed asset data from FMAR via a standardised interface.                                           |    |
| UC-02.06 | Asset Registration & Maintenance       | Manage Connection Limit                                | Manage the connection limits of assets via the Grid Interaction & Constraints Module (GICM), ensuring safe operational thresholds.                      | 🔶 |
| UC-03.01 | Market Unit Registration & Maintenance | Create Market Unit                                     | Enable an FSP to group one or more of its registered assets into a new Market Unit (e.g., SPU or SPG).                                                  | 🔶 |
| UC-03.02 | Market Unit Registration & Maintenance | Reassign Market Unit to New Service Provider           | Manage the change of the FSP responsible for a Market Unit, ensuring the update is reflected consistently.                                               | 🔶 |
| UC-03.03 | Market Unit Registration & Maintenance | Update Market Unit Composition                         | Modify the composition of a Market Unit by adding or removing assets, potentially triggering re-qualification.                                          | 🔶 |
| UC-03.04 | Market Unit Registration & Maintenance | Process Owner-Initiated Asset Switch Between FSPs      | Handle the process of transferring consumer-owned assets between FSPs, initiated and authorised by the consumer.                                         |    |
| UC-03.05 | Market Unit Registration & Maintenance | De-register Market Unit                                | The formal, auditable process for removing a Market Unit from FMAR.                                                                                      | 🔶 |
| UC-04.01 | Product & Qualification Management     | Create and Maintain Product Catalogue                  | (Admin) Create and maintain the central catalogue of all flexibility products accessible through the FMAR Hub.                                          |    |
| UC-04.02 | Product & Qualification Management     | Record Market Unit Qualification Status                | Manage the workflow for FSPs to apply for qualification, and for SOs to record outcomes of external assessments in FMAR.                                | 🔶 |
| UC-04.03 | Product & Qualification Management     | Discover Market Opportunities                          | Enable FSPs to identify applicable products for their Market Units via CMZ or a Table of Equivalences managed in PSQM.                                  | 🔶 |
| UC-05.01 | System-Wide Functions & Integrations   | Share FMAR System Details                              | Provide authorised stakeholders with access to unified data views via FMAR Hub APIs, integrating all modules.                                            |    |
| UC-05.02 | System-Wide Functions & Integrations   | Provide Analytics                                      | Enable Ofgem and the Market Facilitator to generate consolidated reports and insights from FMAR data.                                                   |    |
| UC-05.03 | System-Wide Functions & Integrations   | Dispute Resolution & Data Correction                   | A formal process for managing data disputes and corrections raised by authorised parties.                                                                |    |
| UC-05.04 | System-Wide Functions & Integrations   | Onboard & Manage Third-Party Platforms                 | Register and manage access rights for Independent Market Platforms (IMPs) and other software providers integrating with FMAR.                           |    |
| UC-05.05 | System-Wide Functions & Integrations   | Consumer Consent Interface & Verification              | Define API interactions between FMAR and the national Consumer Consent solution to manage and verify user permissions.                                  |    |
| UC-05.06 | System-Wide Functions & Integrations   | Audit Trail Access & Reporting                         | Allow authorised parties to access a secure, immutable audit trail of changes across FMAR modules.                                                      |    |


---



Out-of-scope modules:
- 🔶 PSQM = Product & Service Qualification Management
- 🔶 GICM = Grid Integration & Constraint Management


### **FMAR Use Case to Module Mapping**

This table outlines the full scope of defined use cases for the FMAR programme and maps them to the logical data module(s) responsible for their delivery. This illustrates the interconnected nature of the FMAR Hub and supports the need for a holistic design approach, even though capabilities will be delivered in phased releases.

| UC ID      | Use Case Grouping                        | Use Case Name                                    | Delivered By Module(s)                |
| :--------- | :--------------------------------------- | :----------------------------------------------- | :---------------------------------- |
| `UC-01.01` | **Customer Onboarding / Offboarding**    | Register User                                    | `SPUM`                              |
| `UC-01.02` | Customer Onboarding / Offboarding        | Register Organisation                            | `SPUM`                              |
| `UC-01.03` | Customer Onboarding / Offboarding        | Update Organisation                              | `SPUM`                              |
| `UC-01.04` | Customer Onboarding / Offboarding        | De-register Organisation                         | `SPUM`                              |
| `UC-02.01` | **Asset Registration & Maintenance**     | Maintain Asset Categories                        | `ARM` (Admin Function)              |
| `UC-02.02` | Asset Registration & Maintenance         | Register and Validate Asset                      | `ARM`, `SPUM`                       |
| `UC-02.03` | Asset Registration & Maintenance         | De-register Asset                                | `ARM`, `PSQM`                       |
| `UC-02.04` | Asset Registration & Maintenance         | Update Asset Details                             | `ARM`, `SPUM`                       |
| `UC-02.05` | Asset Registration & Maintenance         | Export Asset Data                                | `ARM`                               |
| `UC-02.06` | Asset Registration & Maintenance         | Manage Connection Limit                          | `GICM`, `ARM`                       |
| `UC-03.01` | **Market Unit Registration & Maintenance** | Create Market Unit                               | `PSQM`, `ARM`, `SPUM`                 |
| `UC-03.03` | Market Unit Registration & Maintenance   | Reassign Market Unit to New Service Provider     | `PSQM`, `SPUM`                      |
| `UC-03.04` | Market Unit Registration & Maintenance   | Update Market Unit Composition                   | `PSQM`, `ARM`                       |
| `UC-03.05` | Market Unit Registration & Maintenance   | Process Owner-Initiated Asset Switch Between FSPs  | `ARM`, `SPUM`, `PSQM` (Orchestration) |
| `UC-03.06` | Market Unit Registration & Maintenance   | De-register Market Unit                          | `PSQM`                              |
| `UC-04.01` | **Product & Qualification Management**   | Create and Maintain Product Catalogue            | `PSQM` (Admin Function)             |
| `UC-04.02` | Product & Qualification Management       | Record Market Unit Qualification Status          | `PSQM`                              |
| `UC-04.03` | Product & Qualification Management       | Discover Market Opportunities                    | `PSQM`, `ARM`                       |
| `UC-05.01` | **System-Wide Functions & Integrations** | Share FMAR System Details                        | All Modules (API Layer)             |
| `UC-05.02` | System-Wide Functions & Integrations     | Provide Analytics                                | All Modules (Reporting Layer)       |
| `UC-05.03` | System-Wide Functions & Integrations     | Dispute Resolution & Data Correction             | All Modules (Governance Layer)      |
| `UC-05.04` | System-Wide Functions & Integrations     | Onboard & Manage Third-Party Platforms           | `SPUM`                              |
| `UC-05.05` | System-Wide Functions & Integrations     | Consumer Consent Interface & Verification        | `ARM` (Interface)                   |
| `UC-05.06` | System-Wide Functions & Integrations     | Audit Trail Access & Reporting                   | All Modules (Logging/Audit Layer)   |

