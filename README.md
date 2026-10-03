# 🚚 SwiftShip Tracker

**Book. Track. Deliver. Smarter.**

SwiftShip Tracker is a **Salesforce-based parcel management solution** designed to simplify parcel booking, shipment tracking, and delivery management. It combines **Salesforce Custom Objects, Flows, Agentforce AI, and Prompt Builder** to provide centralized parcel management and conversational parcel tracking.

## 📌 Project Overview

SwiftShip Tracker manages the complete parcel lifecycle from **booking and dispatch to tracking and delivery confirmation**.

Customers can access parcel information and track shipments, while delivery agents can update parcel status. Agentforce AI allows users to retrieve parcel details through conversational interaction.

## 🎯 Objectives

* Centralize parcel and delivery information
* Simplify parcel booking and tracking
* Provide shipment status visibility
* Automate parcel operations using Salesforce Flow
* Enable AI-powered parcel tracking using Agentforce
* Improve delivery-agent efficiency
* Provide secure, role-based access

## ✨ Key Features

* 📦 Parcel booking and record creation
* 🔍 Parcel status tracking
* 📍 Current-location tracking
* ⚖️ Parcel weight management
* 📅 Estimated delivery date management
* 👤 Sender and receiver information management
* 🔄 Automated parcel updates using Salesforce Flow
* 🤖 AI-powered parcel tracking using Agentforce
* 💬 Conversational support using Prompt Builder
* 🔐 Role-based and field-level security
* 📊 Reports and dashboards *(planned)*

## 🏗️ System Architecture

The system consists of the following layers:

**Users**

* Customer
* Delivery Agent
* Support Staff
* Administrator

**Interface**

* Salesforce Lightning
* Experience Cloud *(planned)*
* Mobile App *(planned)*

**Data Layer**

* `Parcel__c`
* `Delivery__c`
* `Sender__c`
* `Receiver__c`

**Automation Layer**

* Salesforce Flows
* Apex Classes *(planned)*
* Batch Apex *(planned)*

**AI Layer**

* Agentforce AI
* Prompt Builder
* Parcel Tracking Agent

**Security Layer**

* Permission Sets
* Field-Level Security
* Profiles and Roles *(planned)*

The documented architecture connects users, parcel data, automation, AI assistance, security, and reporting into a centralized Salesforce solution.

## 🗂️ Data Model

### Parcel

Stores the main parcel information:

* Parcel ID
* Status
* Weight
* Estimated Delivery Date
* Sender

### Delivery

Stores delivery-related information:

* Current Location
* Estimated Delivery Date
* Sender
* Parcel

### Sender

Stores:

* Sender Address
* Contact Number
* Email

### Receiver

Stores:

* Receiver Address
* Contact Number
* Email
* Sender
* Parcel

The project uses Salesforce Custom Objects and lookup relationships to connect these records.

## 🤖 Agentforce AI

The **SwiftShip Tracker Agent** provides conversational parcel tracking.

A user can ask for parcel details and provide a Parcel ID. The Agentforce agent uses the **Parcel Details Flow** and **Prompt Builder** to retrieve information from Salesforce.

Example:

```text
User: Can I get my parcel details?

Agent: Sure, please provide your Parcel ID.

User: My Parcel ID is P-123.

Agent:
Parcel Tracking Update
- Parcel Name: ...
- Parcel ID: P-123
- Status: In Transit
- Weight: ...
- Estimated Delivery Date: ...
```

The Prompt Builder template retrieves the parcel name, ID, status, weight, and estimated delivery date.

## 🔄 Flow

The main AI tracking flow works as:

```text
Start
  ↓
Get Parcel Records
  ↓
Retrieve Parcel Details
  ↓
Assignment
  ↓
End
```

The flow accepts a Parcel ID, retrieves the corresponding parcel record, invokes the Prompt Builder template, and returns the generated tracking response.

## 🔐 Security

SwiftShip Tracker uses role-based and field-level access controls.

| Role           | Access                                    |
| -------------- | ----------------------------------------- |
| Administrator  | Full access                               |
| Delivery Agent | Read/Edit parcel and delivery information |
| Customer       | Access to own parcel details              |
| Support Staff  | Cases and parcel details                  |

Sensitive information such as contact details and location data can be restricted using Field-Level Security.

## 🛠️ Technology Stack

| Technology                   | Purpose                     |
| ---------------------------- | --------------------------- |
| Salesforce Developer Edition | Main platform               |
| Salesforce Custom Objects    | Parcel data management      |
| Salesforce Flow              | Automation                  |
| Agentforce AI                | Conversational AI           |
| Prompt Builder               | AI-powered parcel responses |
| Permission Sets              | Access control              |
| Field-Level Security         | Data protection             |
| Lightning App                | Salesforce interface        |
| Experience Cloud             | Customer access *(planned)* |

## 🧪 Testing

The project was tested in a Salesforce Developer Org.

Tested areas include:

* Custom object creation
* Object relationships
* Prompt Builder response
* Flow execution
* Permission assignment
* Agent topic selection
* Parcel tracking
* Data validation

The documented test cases were marked **Pass**.

## 📈 Advantages

* Centralized parcel and customer information
* Better shipment visibility
* Reduced manual effort
* AI-powered customer assistance
* Automated parcel operations
* Secure access control
* Scalable architecture

## 🔮 Future Scope

Future enhancements include:

* Advanced Agentforce parcel-management queries
* Real-time delivery tracking
* Experience Cloud customer self-service
* Automated email and SMS notifications
* Delivery-performance dashboards
* Apex and Batch Apex automation
* External logistics-system integration
* Improved AI prompts
* Enterprise-level sandbox and CI/CD deployment

## 👥 Team

**Team Name:** Parcel Trackers

* **Yazhini M** — 23CS118 — Team Leader
* **Vinotha S** — 23CS114
* **Vishnupriya U** — 23CS116

**College:** A.V.C College of Engineering

**Project Guide:** M. Ashley Monica

## 📄 Project Status

**Platform:** Salesforce Developer Edition
**Project Type:** Academic Prototype
**AI:** Agentforce + Prompt Builder
**Automation:** Salesforce Flow
**Status:** Implemented and tested in Developer Org

## 📜 Conclusion

SwiftShip Tracker demonstrates how Salesforce can be used to build a centralized parcel management and tracking system. By combining **Custom Objects, Salesforce Flow, Agentforce AI, Prompt Builder, and security controls**, the project provides a practical foundation for conversational and scalable parcel management.
