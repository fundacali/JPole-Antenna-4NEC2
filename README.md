# JPole-Antenna-4NEC2
JPole Antenna Project with 4NEC2
## J-Pole Antenna Simulation Project with 4NEC2

This repository contains the **4NEC2 (.nec) file** for a J-Pole Antenna designed for the **146 MHz VHF band**. The project demonstrates proficiency in **Computational Electromagnetics (CEM)** and utilizing simulation tools for antenna design and critical performance analysis.

### 1. Design & Modeling Details

* **Design Goal (Target):** To create a **vertically polarized, omnidirectional** antenna optimized for **50 Ohm** impedance matching at 146 MHz.
* **Operating Frequency:** **146.00 MHz**.
* **Matching Principle:** The antenna uses a J-stub impedance transformer. The feed point location (Tag 7, Segment 20) was chosen to achieve the $50 \ \Omega$ match.

### 2. Simulation Results (Actual Data)

The simulation was executed using the NEC-2D engine at 146.00 MHz. The results show the performance of the **initial, unoptimized** design:

| Metric | Target Specification | **Actual Simulated Result** | Technical Analysis |
| :--- | :--- | :--- | :--- |
| **Input Impedance ($Z_{in}$)** | $50 + j0 \ \Omega$ | **$6.66 + j457.18 \ \Omega$** | **Severely Mismatched:** High imaginary (X) component indicates the need for significant physical length adjustments. |
| **VSWR** (Voltage Standing Wave Ratio) | $\leq 1.5:1$ | **$635.70:1$** | Confirms a critical mismatch with the $50 \ \Omega$ feed line. |
| **Peak Gain** | $\approx 2 \ \text{dBi}$ | **$3.15 \ \text{dBi}$** | The radiator geometry successfully achieved a strong peak gain, confirming the radiation pattern is effective. |
| **Radiation Pattern** | Omnidirectional | **Successfully Omnidirectional** | Pattern is vertically polarized and stable, but feed mismatch limits practical use. |

### 3. Engineering Conclusion & Next Steps (Problem Solving)

The model successfully confirms a high peak gain ($3.15 \ \text{dBi}$) and the desired radiation pattern. However, the simulation results clearly identify a **critical impedance mismatch** (VSWR $635.70:1$). This demonstrates that the physical dimensions of the J-stub require further tuning to effectively transform the impedance to $50 \ \Omega$.

**Next Steps for Optimization:**
The engineering task requires using **Optimization** techniques (e.g., genetic algorithms or parametric sweeps) to iteratively adjust the element lengths and the feed point location (`dist2source`) to reduce the imaginary component ($X$) and drive the real component ($R$) to $50 \ \Omega$. This is the essential next step to produce a functional antenna.

****
