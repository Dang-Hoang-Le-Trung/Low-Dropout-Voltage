# Design and Comparison of Internal vs. External Compensation for LDO Regulators

## 📌 Project Overview
This project focuses on the design process of a **Low-Dropout (LDO) Voltage Regulator** using **65nm CMOS technology**. The primary goal is to evaluate and compare the performance of **Internal Compensation** (Miller RC) versus **External Compensation** in terms of stability, Power Supply Ripple Rejection (PSRR), and transient response.

## 🛠 Technical Specifications
The regulator is designed to provide a stable output of **0.75V** from a **1.2V** supply:

| Parameter | Value |
| :--- | :--- |
| **Technology** | 65nm CMOS |
| **Input Voltage ($V_{IN}$)** | 1.2 V |
| **Output Voltage ($V_{OUT}$)** | 0.75 V |
| **Reference Voltage ($V_{REF}$)** | 0.6 V |
| **Load Current ($I_L$)** | 10uA – 1 mA |
| **Pass Device** | PMOS |

## 🔍 Key Analysis & Results
The project provides a deep dive into the trade-offs between two compensation techniques:

* **External Compensation:** Offers higher **PSRR** and superior stability but requires a larger silicon area, making it less ideal for System-on-Chip (SoC) applications.
* **Internal Compensation:** Utilizes a Miller RC network to shift the dominant pole, providing a compact solution at the cost of increased mid-frequency noise.

## 📊 Simulations
Detailed simulations were performed using **Cadence Virtuoso** (ADE-XL), including:
* **DCOP Analysis:** Ensuring all transistors operate in the saturation region.
* **AC Analysis:** Evaluating Loop Gain, Phase Margin, and PSRR.
* **Transient Response:** Testing $V_{OUT}$ stability against sudden load and line changes.

---
*Author: **Dang Hoang Le Trung** - Ho Chi Minh City University of Technology (HCMUT - VNU)*
