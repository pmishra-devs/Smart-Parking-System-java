
# 🚗 Smart Parking Management System

A console-based, city-wide **Smart Parking Management & Congestion Control System** written in pure Java (Zero external dependencies). It simulates real-time slot allocation, predictive availability forecasting, dynamic surge pricing, and multi-lot traffic load balancing.

---

## ✨ Key Features

- **Live Availability & Forecasting:** View real-time zone-by-zone slot status (`FREE`, `RSVD`, `BUSY`) or forecast occupancy up to **48 hours** ahead.
- **Smart Slot Allocation:** Balances vehicle distribution across zones to prevent single-gate/aisle bottlenecks while prioritizing walk distance and preserving specialized bays (`EV`, `ACCESSIBLE`, `LARGE`).
- **Dynamic Surge Pricing:** Automatically adjusts hourly rates based on real-time occupancy (`0.9x` off-peak discount up to `2.0x` critical load) and peak rush hours (`08:00–09:59` & `17:00–18:59`).
- **City-Wide Congestion Routing:** Recommends the optimal parking lot across the city based on a weighted score of **distance**, **lot occupancy**, and **hourly rate**.
- **Full Reservation Lifecycle:**
  - Advance reservations (up to 48h ahead) & instant walk-in entries
  - Automatic alternative lot suggestions when a chosen lot is full
  - Grace-period enforcement (`15 min` early check-in / `15 min` late no-show auto-release)
  - Overstay detection with automatic slot reassignment and overstay penalty billing
  - Early checkout immediately frees the slot for incoming drivers
- **Time-Travel Simulation:** Built-in simulated clock (`SimClock`) and traffic generator to test rush-hour surges, no-shows, and overstays instantly.

---

## 🛠️ Tech Stack & Requirements

- **Language:** Java 11 or higher (uses `String.repeat` and `java.time` APIs)
- **Dependencies:** None (100% Standard Library)
---

