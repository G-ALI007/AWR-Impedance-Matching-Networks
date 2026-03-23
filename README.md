# RF Impedance Matching Networks Design & Simulation

## 📌 Project Overview
This repository contains the design, analytical calculation, and simulation of various RF impedance matching networks. The goal of this project is to match a complex load impedance to a standard $50\ \Omega$ transmission line at an operating frequency of 2 GHz. 

The simulations were primarily conducted using **AWR Microwave Office**, with analytical verifications performed using **MATLAB** and the **Smith Chart**.

## ⚙️ Design Specifications
* **Operating Frequency ($f_0$):** 2 GHz
* **Characteristic Impedance ($Z_0$):** $50\ \Omega$
* **Load Impedance ($Z_L$):** $200 - j40\ \Omega$

## 🚀 Implemented Matching Techniques

### 1. L-Section Matching (Lumped Elements)
* Calculated using both Smith Chart and analytical MATLAB equations.
* Designed two possible solutions (configurations using Capacitors and Inductors).
* Simulated ideal lumped components to evaluate S11 parameters and bandwidth.

### 2. Single Stub Matching (Distributed Elements)
* Designed using parallel stubs to match the load.
* Calculated transmission line lengths ($d$) and stub lengths ($l$) using the Smith Chart.
* **Physical Implementation:** Converted the ideal electrical lengths into physical Microstrip Lines (MLIN) dimensions using the **TXLine** tool (using a substrate with $\epsilon_r = 3.4$, $H = 0.8\text{ mm}$, $T = 35\ \mu\text{m}$).
* Accounted for physical discontinuities (using MTEE components) and performed tuning to recenter the resonant frequency to exactly 2 GHz.

### 3. Short-Circuited Stub Matching
* Alternative distributed matching technique utilizing short-circuited stubs.
* Compared bandwidths ($\Delta f$) between different solutions to determine the optimal configuration.

## 🛠️ Tools & Technologies Used
* **AWR Microwave Office:** For schematic capture, S-parameter simulation (S11), and tuning.
* **MATLAB:** For executing analytical formulas to verify Smith Chart readings.
* **TXLine:** For calculating physical microstrip dimensions.
* **Smith Chart:** For graphical impedance mapping and stub length calculations.

## 📂 Repository Structure
* `/AWR_Files/`: Contains the AWR Microwave Office project files (`.emp`).
* `/MATLAB/`: Contains the MATLAB scripts used for calculating lumped element values (L & C).
* `/Docs/`: Contains the full project report (PDF) detailing the step-by-step Smith Chart procedures and simulation graphs.

## 👨‍💻 Author
**Ghader Ali**
Telecommunications Engineer | Software Developer

---
*This project was completed as part of the 4th-year Communications Engineering curriculum at the Higher Institute for Applied Sciences and Technology (HIAST).*
