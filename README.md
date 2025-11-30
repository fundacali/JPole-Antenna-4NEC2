## J-Pole Antenna Project using 4NEC2

This folder holds the **4NEC2 (.nec) file** for a J-Pole Antenna. We designed this antenna for use in the **146 MHz VHF band**.

The project shows my experience with **Computer Simulation** and analyzing antenna performance.

### 1. Design Basics

* **Main Goal:** To make a **vertical** antenna that sends signals in all directions (**omnidirectional**). It should also perfectly match the standard **50 Ohm** cable.
* **Frequency:** **146.00 MHz**.
* **Matching Idea:** We used the special "J-stub" part of the antenna to try to get a $50 \ \Omega$ match. The feed point is set at **Tag 7, Segment 20**.

### 2. Simulation Results (What the Computer Said)

We ran the simulation at 146.00 MHz. This shows the results from the **first version** of the antenna (unoptimized):

| What We Measured | What We Aimed For (Target) | **What We Actually Got** | What This Means |
| :--- | :--- | :--- | :--- |
| **Input Impedance ($Z_{in}$)** | $50 + j0 \ \Omega$ | **$6.66 + j457.18 \ \Omega$** | **Very Bad Match:** The high 'j' (imaginary) part means the antenna is acting like a bad capacitor/inductor. |
| **VSWR** | Less than $1.5:1$ | **$635.70:1$** | This number is extremely high. It confirms almost all power is **reflected back** to the source, not sent out. |
| **Peak Gain** | Around $2 \ \text{dBi}$ | **$3.15 \ \text{dBi}$** | The shape of the antenna is good for sending out signals. |

### 3. Conclusion & Next Steps (Problem Solving)

The model proved the antenna has great gain ($3.15 \ \text{dBi}$) and a good radiation pattern. However, the simulation clearly found a **major problem** with the impedance match (VSWR $635.70:1$).

**The Engineering Challenge:**
The next step is to **fix this mismatch**. This means we need to repeatedly adjust the physical sizes (like lengths and spacing) of the J-stub. We must continue this process until the imaginary part ($j457.18 \ \Omega$) becomes close to zero, and the real part ($6.66 \ \Omega$) becomes close to $50 \ \Omega$. This process is called **optimization**.

****
