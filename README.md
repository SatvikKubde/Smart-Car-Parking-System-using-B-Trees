# 🚗 Smart Car Parking System using B+ Trees

A smart car parking management system built in **C**, using **B+ Trees** to efficiently store, search, and sort vehicle data. This system simulates real-world parking operations such as vehicle registration, dynamic slot allocation, membership-based privileges, and revenue calculation — all handled without arrays.

---

## 🔧 Features

- Register vehicles with full owner details
- Allocate parking space based on membership level
- Track real-time **arrival** and **departure** of vehicles
- Automatically compute:
  - Parking duration
  - Parking charges
- Apply membership-based discounts
- Maintain vehicle history: total parkings, total hours, total revenue
- **B+ Tree-based operations**:
  - Insert, search, delete by vehicle number
  - Sort vehicles by revenue or parking frequency
  - Perform range queries efficiently
- File handling for persistent data storage

---

## 🧠 Project Summary

This C program replicates a real-life parking system that scales efficiently using **B+ Trees**. Each vehicle entry is stored and indexed dynamically for fast lookups and sorted access. Parking slot assignment adheres to a structured policy based on membership, and all records are saved using file I/O.

---

## 📌 Allocation Policy

| Membership     | Parking Slots Allocated |
|----------------|--------------------------|
| 🥇 Gold         | Slots 1–10               |
| 🥈 Premium      | Slots 11–20              |
| ❌ Non-member   | Slots 21–50              |

---

## 🎖 Membership Policy

| Total Parking Hours | Membership Level |
|---------------------|------------------|
| < 100 hours         | ❌ Non-member     |
| ≥ 100 hours         | 🥈 Premium        |
| ≥ 200 hours         | 🥇 Gold           |

---

## 💰 Payment Policy

- ₹100 for first 3 hours
- ₹50 per additional hour
- 10% discount for Gold and Premium members

---

## 🌳 B+ Tree Applications

- **Vehicle Record Indexing**: Indexed by vehicle number
- **Sorted Queries**:
  - By total revenue
  - By total number of parkings
- **Range Queries**:
  - Vehicles with revenue > ₹X
  - Vehicles with parking hours between X and Y
- Enables fast disk-like access performance

---

## 📂 Sample Data

- System loads 10–20 vehicle records on startup from `data.txt`
- Each record includes:
  - Vehicle number
  - Owner name
  - Arrival and departure times
  - Membership level
  - Parking duration
  - Revenue
  - Slot number

---

## 💻 Technologies Used

- Language: C
- Data Structure: B+ Tree
- Standard Libraries: `stdio.h`, `stdlib.h`, `string.h`, `time.h`
- File Handling for persistence
- Command-Line Interface (CLI)

---
