# 🏦Daily Pay Collection System

## 📌 Overview

CoreLend is a mainframe-based banking application developed using **COBOL, CICS, JCL, and VSAM**.
It simulates real-world loan management and payment processing systems with both **online (CICS)** and **batch (JCL)** components.

The system supports end-to-end banking operations including **account management, payment processing, transaction tracking, and delinquency handling**.

---

## ⚙️ Features

* 💳 **Online Payment Processing (CICS)**

  * Supports Exact, Partial, and Excess payments
  * Real-time updates to loan accounts

* 🏦 **Account Management (CRUD Operations)**

  * Create, Read, Update, Delete customer and loan records

* 📜 **Transaction History**

  * Maintains a ledger of all transactions for auditing

* 🔄 **Batch Processing (JCL)**

  * Daily file preparation (clean/fresh datasets)
  * File merging and transformations
  * Delinquency calculation and updates

* 📊 **Report Generation**

  * Daily collection reports
  * Paid vs Delinquent account reports
  * Header and trailer formatted outputs

* 📂 **VSAM File Handling**

  * KSDS for master and transaction data
  * GDG for versioned outputs

---

## 🏗️ System Architecture

```
CICS Screens (Online Layer)
        ↓
COBOL Programs (Business Logic)
        ↓
VSAM Files (KSDS / ESDS)
        ↓
Batch Jobs (JCL, SORT, IDCAMS)
        ↓
Reports & GDG Outputs
```

---

## 📂 Project Modules

| Module                 | Description                                        |
| ---------------------- | -------------------------------------------------- |
| Account Management     | Handles customer and loan CRUD operations          |
| Payment Processing     | Processes Exact, Partial, and Excess payments      |
| Transaction Ledger     | Stores all transaction records                     |
| Daily Target System    | Prepares daily collection targets                  |
| Delinquency Processing | Identifies overdue accounts and updates status     |
| Reporting Module       | Generates structured reports with headers/trailers |

---

## 🧾 File Structures

* **Loan Account File (KSDS)**
* **Customer File (KSDS)**
* **Transaction Ledger (KSDS/ESDS)**
* **Daily Target File**
* **Daily Payment File**
* **Delinquency File**
* **Report Files (PS & GDG)**

---

## 🔧 Technologies Used

* COBOL
* CICS
* JCL
* VSAM (KSDS, ESDS)
* SORT Utility
* IDCAMS

---

## 🔁 Sample Workflow

```
User enters payment via CICS screen
        ↓
COBOL program validates and processes payment
        ↓
Loan file updated (KSDS REWRITE)
        ↓
Transaction recorded in ledger
        ↓
Batch job runs at end-of-day
        ↓
Delinquency and reports generated
```

---

## 🧠 Key Concepts Demonstrated

* VSAM operations (READ, REWRITE, STARTBR, READNEXT)
* CICS transaction handling
* Batch vs Online integration
* File merging and transformation using SORT
* GDG handling for daily data
* Data reconciliation and system balancing

---

## 🚀 How to Run

1. Define required VSAM files (KSDS/ESDS)
2. Configure CICS programs and FCT entries
3. Run online transactions via CICS screens
4. Execute batch jobs (JCL) for:

   * File preparation
   * Merging
   * Reporting

---

## 📌 Future Enhancements

* Tokenization for secure transactions
* API integration with external systems
* Real-time notifications
* Advanced reconciliation engine
* Dashboard reporting

---

## 👨‍💻 Authors

Guru Charan
LOKESH ATLA
VVS PRAVEEN
VVS NAVEEN
SATHVIKA

---

## ⭐ Project Tagline

*A mini core banking system built entirely on mainframe technologies.*
