## 🌈 Overview

Airline Crew Scheduling is a **real-world NP-hard optimization problem** where flights must be assigned to crew members following strict operational rules.

This project implements:

- 🔍 **Constraint Satisfaction (CSP)**  
- 🧠 **Backtracking Search**  
- 💸 **Branch & Bound Cost Minimization**  
- 📊 **Scaling & Performance Profiling**  
- 📆 **Gantt Chart Visualization**

It provides a **complete implementation + analytics + visual outputs** suitable for academic submission, GitHub showcase, and DSA demonstration.

---

# 📑 Problem Breakdown

## ✈️ Flight Scheduling Constraints

| Constraint Type | Description |
|-----------------|-------------|
| ⏱️ **No Overlap** | A crew member cannot operate overlapping flights. |
| 😴 **Minimum Rest Time** | Required gap between consecutive flights (e.g., 1 hour). |
| 🧍 **Crew Availability** | Crew assigned must be from available pool. |
| 📋 **All Flights Must Be Assigned** | No flight should remain unattended. |
| 💰 **Optional Cost Rule** | Each crew–flight pair has a cost; goal is to minimize total. |

---

# 🔧 Algorithmic Approach

## 🧠 Algorithms Used

| Algorithm | Purpose | Complexity | When Used |
|----------|----------|------------|-----------|
| **Backtracking (CSP)** | Assign feasible flights | Exponential | Always |
| **Branch & Bound** | Prune costly branches | Depends on pruning | With cost optimization |
| **Feasibility Checker** | Validates overlaps & rest | O(n) per check | For each assignment |
| **Sorting Heuristic** | Order flights by start-time | O(n log n) | Improves pruning |

---

# 🗂️ Project Structure

```

Airline-Crew-Scheduling-Optimization/
│
├── crew_scheduling.ipynb
├── images/
│   ├── gantt.png
│   ├── scaling.png
│
├── tables/
│   ├── crew_assignment.csv
│   ├── scaling.csv
├── README.md
└── requirements.txt

```

---

# 🧮 Input Format

### **Flights Table**
| Flight ID | Start | End |
|-----------|--------|------|
| F1 | 09:00 | 11:00 |
| F2 | 10:00 | 12:00 |
| F3 | 13:00 | 15:00 |
| F4 | 11:30 | 13:00 |
| F5 | 16:00 | 18:00 |

### **Crew Members**
```

C1, C2, C3

```

### **Cost Matrix (Optional)**

| Crew / Flight | F1 | F2 | F3 | F4 | F5 |
|---------------|----|-----|-----|-----|-----|
| **C1** | 100 | 90 | 130 | 80 | 150 |
| **C2** | 120 | 95 | 120 | 85 | 140 |
| **C3** | 110 | 100 | 140 | 90 | 145 |

---

# 🧩 Solution Logic

## ✔️ 1. **Check if Crew Can Take Flight**
- No overlaps  
- Enough rest time  
- Valid cost entry (if cost mode enabled)

---

## ✔️ 2. **Backtracking Assignment**

At each step:

- Pick a flight  
- Try assigning it to each available crew  
- Validate constraints  
- Backtrack if violated  
- Track recursive calls  
- Stop when all flights assigned  

---

## ✔️ 3. **Cost Minimization (Branch & Bound)**

Lower-bound estimation:  
For remaining flights → sum of minimum possible cost per flight.

If **lower bound ≥ current best cost**, prune branch.

---

# 📊 Key Outputs

## ⭐ 1. Gantt Chart — Crew Timeline

<p align="center">
  <img src="images/gantt.png" width="700">
</p>

---

## ⭐ 2. Scaling Plot — Time vs Number of Flights

<p align="center">
  <img src="images/scaling.png" width="650">
</p>

---

## ⭐ 3. Sample Optimal Assignment

| Crew | Flights Assigned |
|------|------------------|
| C1 | F1, F4 |
| C2 | F2 |
| C3 | F3, F5 |

---

## ⭐ 4. Sample Output File (crew_assignment.csv)

| Crew | Flight | Start | End |
|------|---------|--------|------|
| C1 | F1 | 09.0 | 11.0 |
| C1 | F4 | 11.5 | 13.0 |
| C2 | F2 | 10.0 | 12.0 |
| C3 | F3 | 13.0 | 15.0 |
| C3 | F5 | 16.0 | 18.0 |

---

# 🚀 Performance Analysis

## 📈 Complexity Overview

| Method | Time Complexity | Notes |
|--------|------------------|-------|
| Backtracking | Exponential | NP-hard nature |
| Feasibility Check | O(n) | Per crew schedule |
| Sorting Flights | O(n log n) | Preprocessing |
| Branch & Bound | Depends on pruning | Significant reduction |

---

## 📊 Scaling Experiment Table

### **Time vs Number of Flights**

| Flights | Time (s) | Recursive Calls |
|---------|----------|------------------|
| 4 | 0.002 | 10 |
| 5 | 0.006 | 53 |
| 6 | 0.09 | 214 |
| 7 | 1.42 | 3420 |

(*numbers will vary*)

---

# ⚙️ Technologies Used

| Category | Tools |
|----------|--------|
| Language | Python |
| Notebook | Google Colab |
| Libraries | NumPy, Pandas, Matplotlib, Memory Profiler |
| Algorithms | Backtracking, CSP, Branch & Bound |

---

# 📦 Installation

```

pip install pandas matplotlib memory_profiler

```

Or simply open the notebook in **Google Colab**.

---

# 🎉 Final Deliverables

✔️ Fully functioning crew scheduling system  
✔️ Cost-optimized assignment  
✔️ Gantt chart visualization  
✔️ Scaling experiment & tables  
✔️ High-quality CSV outputs  
✔️ GitHub-ready documentation  

---

# 🔗 Connect with Me

**LinkedIn:** https://www.linkedin.com/in/adityagaur19  
**GitHub:** Add your repo link here  

---

<p align="center">
  <b>“Scheduling is not just assigning tasks — it’s optimizing human effort under constraints.”</b>
</p>
```


Just tell me!
