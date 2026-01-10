# Design and Comparison of Internal vs. External Compensation for LDO Regulators

## 📌 Project Overview
This project focuses on the design and performance analysis of a **Low-Dropout (LDO) Voltage Regulator** implemented using **65nm CMOS technology**. The study evaluates the trade-offs between two primary stability techniques: **Internal Compensation** (using a Miller RC network) and **External Compensation**.

## 🛠 Technical Specifications
The regulator is designed to provide a stable 0.75V output from a 1.2V supply:

| Parameter | Value |
| :--- | :--- |
| **Technology** | 65nm CMOS |
| **Input Voltage ($V_{IN}$)** | 1.2 V |
| **Output Voltage ($V_{OUT}$)** | 0.75 V (Regulated) |
| **Reference Voltage ($V_{REF}$)** | 0.6 V |
| **Load Current Range ($I_L$)** | 10 uA – 1 mA |
| **Pass Device** | PMOS |

## 🏗 Circuit Architecture
* **Error Amplifier:** A 2-stage architecture featuring a 6-transistor differential pair with an NMOS active load.
* **Pass Device:** A PMOS transistor designed to remain in the saturation region to ensure precise regulation across the full load range.
* **Control Loop:** Utilizes negative feedback to compare the sampled output voltage against the reference.

## 🔍 Compensation & Stability Analysis
The project compares two methods to ensure the control loop does not oscillate:

| Metric | Internal (Miller RC) | External Compensation |
| :--- | :--- | :--- |
| **Stability Method** | Miller RC network to shift the dominant pole. | Large load capacitor (nF to uF). |
| **Unity Gain Bandwidth (UGB)** | 304 KHz | 171.9 KHz |
| **Phase Margin** | 88.7527° (stable) | 84.86° (Stable) |
| **PSRR @ 1MHz** | 0.234 dB | 48.95 dB |

### Key Findings:
* **External Compensation** provides superior **PSRR** and high stability but requires significant silicon area (off-chip capacitor), making it less suitable for high-density SoC applications.
* **Internal Compensation** allows for a more compact, capacitor-less design but requires careful optimization to manage mid-frequency noise and stability.

## 📊 Simulation Environment
Simulations were performed using **Cadence Virtuoso (ADE-XL)**, including:
* **DCOP Analysis:** To verify saturation for all transistors across the load current sweep.
* **AC Analysis:** To extract Loop Gain, Phase Margin, and PSRR characteristics.
* **Transient Response:** To measure $V_{OUT}$ stability during abrupt load or line transitions.

---
**Author:** Dang Hoang Le Trung
**University:** Ho Chi Minh City University of Technology (HCMUT - VNU)
