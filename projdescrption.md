1. Project Title:
Parametric DC Analysis of CMOS Inverter Using Cadence Virtuoso at 90nm Technology Node

2. Objective:
To analyze the impact of varying NMOS and PMOS transistor widths on the Voltage Transfer Characteristics (VTC) of a CMOS inverter using Cadence Virtuoso
and to determine the optimal width ratio for balanced switching behavior and efficient logic performance.

3. Tools & Technology:
EDA Tool: Cadence Virtuoso
Simulator: ADE L
Technology Node: 90nm CMOS process
Simulation Type: DC Analysis (Parametric Sweep)

4. Methodology:
 ->CMOS Inverter Schematic Design:
   * Designed a standard CMOS inverter with one NMOS and one PMOS transistor.
   * Power supply (VDD) set at 2V; input voltage swept from 0V to 2V.
     
 ->Parameter Setup:
   * NMOS width: Initially fixed (e.g., 120nm)
   * PMOS width: Varied from **120nm to 500nm** in 20 uniform steps
   * Later, vice versa: PMOS width fixed, NMOS width swept similarly
   * Length for both devices kept constant (e.g., 90nm)

 ->DC Sweep Analysis:
   * Performed DC analysis to sweep input voltage (Vin) and observed the output voltage (Vout) for each transistor width variation.
   * Overlaid multiple VTC curves for each width in waveform viewer.

 ->Threshold Tracking:
   * Plotted Vin = Vout reference line to estimate VM (inverter threshold)
   * Observed shifts in VM based on device sizing.
     
5. Observations & Results:
* Increasing PMOS width** caused the VTC curve to shift right, indicating a stronger pull-up (logic high) response and higher inverter threshold.
* **Increasing NMOS width** caused the VTC curve to shift left, due to stronger pull-down capability.
* Confirmed that due to the mobility mismatch (μₙ > μₚ), PMOS must be sized wider than NMOS (typically 2–3×) to achieve:
* Balanced rise/fall times
* Symmetric voltage transfer characteristics
* Optimal logic threshold (VM ≈ VDD/2)
* Improved noise margins

6. Conclusion:
This parametric analysis effectively demonstrated the influence of transistor sizing on inverter behavior. 
It validated the common CMOS design rule of sizing PMOS larger than NMOS to counteract mobility imbalance and optimize performance. 
This process is crucial in **standard cell design**, **digital circuit timing optimization**, and **low-power VLSI design**.

7. Keywords:

CMOS Inverter, Cadence Virtuoso, DC Analysis, VTC, 90nm Technology, PMOS Width, NMOS Width, Parametric Sweep, Threshold Voltage, 
Rise/Fall Time, Symmetric Logic, Transistor Sizing, EDA Tools, Analog Design.
				
