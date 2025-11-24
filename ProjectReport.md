# 📄 Project Report: Contextualized Adaptive Schedule Optimizer

**Date:** November 2025
**Project:** Contextualized Adaptive Schedule Optimizer (CASO)

---

## 1. Executive Summary

The Contextualized Adaptive Schedule Optimizer (CASO) is a proof-of-concept scheduling system implemented in Python. Its primary objective is to move beyond simple time blocking by incorporating **human-centric factors** such as dynamic energy levels, cognitive peak focus hours, and external variables like weather and travel time. The resulting schedule is not just a list of events but an optimized plan designed to maximize productivity and ensure sustained focus throughout the day.

---

## 2. Project Goals and Objectives

### 🎯 Primary Goal
To develop a robust scheduling algorithm capable of dynamically prioritizing and placing flexible tasks based on real-time contextual data and a simulated human energy model.

### ✅ Key Objectives Achieved
* **Contextual Data Integration:** Successfully integrated external factors (simulated travel, weather) to adjust task durations dynamically.
* **Resource Modeling:** Implemented a non-renewable **energy budget** (`MAX_ENERGY`) that dictates the scheduling of high-difficulty tasks.
* **Priority Queue System:** Utilized a weighted scoring mechanism and `heapq` to ensure the highest-value flexible tasks are prioritized for optimal time slots.
* **Mandatory Break Insertion:** Implemented logic to insert scheduled breaks (lunch, afternoon) and mandatory rest breaks when energy depletion requires it.

---

## 3. System Architecture and Design

The optimizer is built around the `ScheduleOptimizer` class, which manages all data structures and execution logic.

### 3.1. Data Structures

| Structure | Purpose | Implementation Detail |
| :--- | :--- | :--- |
| `self.tasks` | Stores all tasks organized by date. | Dictionary of Lists |
| `fixed_tasks` | Tasks with a set `fixed_start` time (e.g., meetings). | List, sorted chronologically. |
| `flexible_tasks` | Tasks without a fixed time. | List, processed by the priority queue. |
| `priority_queue` | Holds flexible tasks for insertion. | Python's `heapq` (Min-Heap). |
| `time