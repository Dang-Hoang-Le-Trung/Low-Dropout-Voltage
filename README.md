# Design and Comparison of Internal vs. External Compensation for LDO Regulators

## 📌 Project Overview
[cite_start]This project focuses on the design process of a **Low-Dropout (LDO) Voltage Regulator** using **65nm CMOS technology**. [cite_start]The primary goal is to evaluate and compare the performance of **Internal Compensation** (Miller RC) versus **External Compensation** in terms of stability, Power Supply Ripple Rejection (PSRR), and transient response.

## 🛠 Technical Specifications
[cite_start]The regulator is designed to provide a stable output of **0.75V** from a **1.2V** supply[cite: 485, 773]:

| Parameter | Value |
| :--- | :--- |
| **Technology** | [cite_start]65nm CMOS [cite: 484] |
| **Input Voltage ($V_{IN}$)** | [cite_start]1.2 V [cite: 485, 773] |
| **Output Voltage ($V_{OUT}$)** | [cite_start]0.75 V [cite: 485, 773] |
| **Reference Voltage ($V_{REF}$)** | [cite_start]0.6 V [cite: 485, 773] |
| **Load Current ($I_L$)** | [cite_start]10 $\mu$A – 1 mA  |
| **Pass Device** | [cite_start]PMOS [cite: 484, 578] |

## 🔍 Key Analysis & Results
[cite_start]The project provides a deep dive into the trade-offs between two compensation techniques[cite: 911]:

* [cite_start]**External Compensation:** Offers higher **PSRR** and superior stability but requires a larger silicon area, making it less ideal for System-on-Chip (SoC) applications[cite: 877, 905].
* **Internal Compensation:** Utilizes a Miller RC network to shift the dominant pole, providing a compact solution at the cost of increased mid-frequency noise[cite: 879, 904].

## 📊 Simulations
Detailed simulations were performed using **Cadence Virtuoso** (ADE-XL)[cite: 797, 834], including:
* [cite_start]**DCOP Analysis:** Ensuring all transistors operate in the saturation region[cite: 649, 834].
* [cite_start]**AC Analysis:** Evaluating Loop Gain, Phase Margin, and PSRR[cite: 839, 911].
* **Transient Response:** Testing $V_{OUT}$ stability against sudden load and line changes[cite: 845, 862].

---
*Author: **Đặng Hoàng Lê Trung** - Ho Chi Minh City University of Technology (HCMUT - VNU)* [cite: 471, 481]
