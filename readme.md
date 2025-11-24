# 📅 Contextualized Adaptive Schedule Optimizer

The **Contextualized Adaptive Schedule Optimizer** is a Python-based utility designed to create highly personalized and optimized daily schedules. Unlike rigid schedulers, this tool dynamically adjusts task durations and placement based on several contextual factors, including energy levels, peak focus hours, weather conditions, and task dependencies, ensuring that the most critical and energy-intensive tasks are prioritized during optimal times.

---

## ✨ Features

* **Fixed and Flexible Task Handling:** Manages both time-specific (fixed) and flexible tasks.
* **Energy-Based Optimization:** Tracks a simulated energy level and prioritizes high-difficulty tasks when energy is high. Automatically inserts rest breaks when energy is critically low.
* **Dynamic Duration Adjustment:** Adjusts task duration based on real-time factors like simulated **weather conditions** (for outdoor tasks) and **travel time**.
* **Focus Hour Prioritization:** Uses defined user **Peak Focus Hours** to weigh task priority, ensuring deep work is scheduled during optimal cognitive periods.
* **Dependency Management:** Ensures dependent tasks are not scheduled before their prerequisites.
* **Time Block Allocation:** Efficiently identifies and utilizes available free time slots between fixed commitments.

---

## 🛠️ Requirements & Setup

This project is a standalone Python class and requires only standard built-in libraries.

### Prerequisites

You need **Python 3.x** installed on your system.

### Libraries

The project relies on the following four standard Python libraries:

1.  `datetime`
2.  `random`
3.  `time`
4.  `heapq` (for the priority queue implementation)

### Installation

No special installation is required. Simply save the provided code as `schedule_optimizer.py`.

---

## 🚀 Usage

Run the script from your terminal:

```bash
python schedule_optimizer.py