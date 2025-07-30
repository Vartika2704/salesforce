# 🚗 WhatNext Vision Motors: Salesforce CRM Project

Welcome to the official GitHub repository for the **Salesforce CRM Implementation** for *WhatNext Vision Motors*, an innovative leader in the automotive industry.

This project aims to digitally transform customer and operations management through Salesforce automation, Apex development, and Lightning UI enhancements.

---

## 📌 Project Overview

WhatNext Vision Motors has implemented Salesforce CRM to improve:

- 📍 Nearest dealer assignment based on customer address
- ❌ Prevention of orders for out-of-stock vehicles
- 📧 Auto-email reminders for test drives
- 🔁 Periodic stock-based order status updates using Batch Apex

This solution blends (Flows, Process Builder) with **custom Apex triggers** and **scheduled jobs** for a seamless, efficient user experience.

---

## 🎯 Objectives

- ✅ Automate dealer assignment and test drive workflows
- 🚫 Prevent invalid orders via stock validation
- 📊 Improve reporting and dashboard visibility
- ⚙️ Reduce manual workload through Apex automation
- 🔐 Maintain strong security and data visibility via profiles and roles

---

## 📁 Custom Objects

| Object Name                | Purpose                          | Relationships                     |
|---------------------------|----------------------------------|-----------------------------------|
| `Vehicle__c`              | Stores vehicle inventory         | Linked to Orders, Test Drives     |
| `Vehicle_Order__c`        | Tracks vehicle purchases         | Linked to Customer & Vehicle      |
| `Vehicle_Customer__c`     | Stores customer details          | Linked to Orders, Test Drives     |
| `Vehicle_Dealer__c`       | Stores dealer information        | Linked to Orders                  |
| `Vehicle_Test_Drive__c`   | Tracks test drive bookings       | Linked to Customer & Vehicle      |
| `Vehicle_Service_Request__c` | Tracks service requests        | Linked to Customer & Vehicle      |

---

## 🧩 Key Features & Automation

### 🔄 Record-Triggered Flows
- Auto-assign nearest dealer on order creation
- Send email on test drive booking

### 🔐 Validation Rule
- Blocks order placement if vehicle stock is 0

### 🧠 Apex Triggers & Handler
- Validates stock
- Updates vehicle stock post-confirmation

### ⏰ Batch Apex Jobs
- Scheduled job updates order statuses daily at 12 PM
- Stock re-verified using `VehicleOrderBatch` logic

---

## 🖥️ UI/UX Development

### Lightning App
- Custom Lightning app "WhatNext Vision Motors"
- Quick access to key objects via custom tabs

### Page Layouts & Forms
- Compact and full layouts with relevant fields
- Optimized for both desktop and mobile views


## 🔐 Security Model

- Profiles: Admin, Dealer Manager, Support
- Role hierarchy: Regional access segmentation
- Permission Sets: Granular dashboard/report access

---

## 🧪 Testing & Validation

- Unit tested with 85%+ coverage on triggers and batch jobs
- Functional UI testing performed via record entry

---

## 🚀 Deployment Strategy

- Migrated using Change Sets from Sandbox to Production
- Scheduled jobs reviewed weekly in Setup
- Debug logs configured for error tracking

---

## 🌟 Future Enhancements

- Integration with SMS/WhatsApp APIs
- AI-based dealer matching via Salesforce Einstein
- Expansion to external partner portal using Experience Cloud

