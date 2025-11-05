# ahb_lite_memory_controller
Verilog-based AHB-Lite memory controller with testbench, simulation results, and GDS layout generated using Cadence Virtuoso.

# 🧠 AHB-Lite Memory Controller (RTL to GDSII Implementation)

---

## 🏁 Project Overview

This project involves the **design and implementation of an AHB-Lite Memory Controller** using **Xilinx Vivado**, followed by the **RTL-to-GDSII flow** using **Cadence EDA tools**.  
The goal is to bridge the gap between **RTL design** and **physical implementation**, ensuring correct functionality, timing closure, and a clean layout ready for fabrication.

---

## 🎯 Aim

To design, simulate, synthesize, and implement an **AHB-Lite Memory Controller** that supports read and write operations over the AHB-Lite protocol, and to perform **physical design using Cadence Genus and Innovus**.

---

## 🧰 Tools and Technologies Used

| Category | Tool / Language |
|-----------|-----------------|
| HDL Design | Vivado |
| Functional Simulation | Vivado |
| Synthesis | Cadence Genus |
| Physical Design | Cadence Innovus |
| OS / Environment | Red Hat Linux |
| Reports | Timing, Area, Power |
| Output | GDSII Layout |

---

## 🧩 Theory

**AHB-Lite** is a simplified version of ARM’s Advanced High-Performance Bus protocol, optimized for **single-master systems**.  
The **Memory Controller** acts as an interface between the AHB bus and on-chip memory, handling:

- Address decoding  
- Read/Write data operations  
- Handshaking using `HREADY` and `HRESP` signals  

This controller is implemented using **synchronous logic** and verified through simulation before synthesis.

---

## ⚙️ Design Flow

### 1️⃣ RTL Design
- Implemented and verified for functional correctness using **Vivado**.

### 2️⃣ Functional Simulation
- Simulated using **Vivado**.
- Verified read/write behavior and data integrity.

### 3️⃣ Synthesis (Cadence Genus)
- RTL synthesized into a **gate-level netlist**.
- Generated **timing, area, and power** reports.

### 4️⃣ Physical Design (Cadence Innovus)
- Floorplanning and power planning.
- Placement, Clock Tree Synthesis (CTS), and Routing.
- **DRC/LVS checks** performed.
- Final **GDSII layout** generated.

---

## 🧮 Simulation and Verification

✅ Successful read and write operations were observed in the waveform.  
The controller correctly responded to AHB transactions with valid `HREADYOUT` and `HRESP` signals.

---

## 📊 Reports

| Parameter | Description |
|------------|-------------|
| **Timing Report** | Slack and critical path delay after synthesis |
| **Area Report** | Total cell area and utilization |
| **Power Report** | Dynamic and leakage power analysis |
| **GDSII Layout** | Final 2D physical design layout exported from Innovus |

---

## 📖 Research Reference

> **Shrikant Jadhav, Anila Kommineni, Manoj Kumar Gundu, and Youngsoo Kim**,  
> *Design & Verification of AMBA AHB-Lite Memory Controller*,  
> IEEE Computing and Communication Workshop and Conference (CCWC), March 2023.  
> [🔗 View Paper (PDF)](./Design_amp_Verification_of_AMBA_AHB-Lite_Memory_Controller.pdf)

---

### 🧠 Inspiration and Similarities
The IEEE research paper provided the **conceptual foundation** for this work, particularly in understanding the **signal-level behavior** of the AHB-Lite protocol, its **handshaking mechanism**, and **memory-mapped data access**.  
Both the paper and this implementation emphasize:
- The design of a **slave-side memory controller** compatible with the AHB-Lite bus.  
- Verification of **read/write operations** using simulation waveforms.  
- The importance of maintaining **protocol timing and data integrity**.

This project was inspired by that approach and began with similar RTL signal structures and behavioral modeling.

---

### 🔧 Modifications and Differences
While the paper concentrated on **functional verification using SystemVerilog and UVM**, this implementation expands the scope toward **physical design realization** using the **RTL-to-GDSII flow**.  
Major modifications include:
- **Implementation in Verilog HDL** (instead of SystemVerilog).  
- **Complete synthesis and place-and-route** using **Cadence Genus and Innovus**.  
- Generation of **timing, power, and area reports** for post-synthesis analysis.  
- Export of the final **GDSII layout**, completing the ASIC design cycle.  

Hence, this work bridges **academic research and practical ASIC implementation**, showing how a protocol-level design can be brought to silicon-ready form.

---

