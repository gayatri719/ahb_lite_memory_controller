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
The IEEE paper served as the **conceptual foundation** for this work, particularly in understanding the **protocol behavior**, **handshaking mechanism**, and **signal timing** of AHB-Lite.  
Both the paper and this implementation share:
- The development of an **AHB-Lite slave memory controller**.  
- Verification of **read/write data transactions**.  
- Emphasis on **protocol compliance and timing accuracy**.  

The initial Verilog structure and simulation concepts were inspired by the methodology presented in the referenced work.

---

### 🔧 Modifications and Differences
While the paper focuses mainly on **functional verification** using a **UVM-based SystemVerilog testbench**, this project extends beyond verification to **complete physical realization** using Cadence EDA tools.  
Key differences include:
- Implementation written in **pure Verilog HDL** instead of SystemVerilog.  
- Addition of **synthesis, floorplanning, placement, and routing** steps using **Genus** and **Innovus**.  
- Generation of **timing, power, and area** reports for detailed post-synthesis analysis.  
- Export of **final GDSII layout**, completing the **RTL-to-GDSII design flow**.  

---

### 💎 Comparative Advantage — How This Project Improves Upon the Paper

This implementation provides a **broader design perspective** than the original IEEE work by extending beyond simulation into **backend VLSI design**.  
While the paper validates the memory controller at the **functional verification level**, this project demonstrates its **real-world implementability** through the following improvements:

- ✅ **Complete ASIC design coverage:** From RTL to final GDSII, showing every stage of the VLSI pipeline.  
- ✅ **Physical verification integration:** Includes DRC/LVS checks and area/power optimization reports.  
- ✅ **Tool diversity:** Uses both **Xilinx Vivado** for front-end and **Cadence Genus/Innovus** for back-end design, bridging academic and industrial tools.  
- ✅ **Fabrication-ready outcome:** The generated **GDS layout** represents an actual chip-level implementation possibility, which the paper did not achieve.  
- ✅ **Design scalability:** Structured to support future extensions for multi-master or burst-mode operation.  

Thus, this project transforms the conceptual and simulation-oriented IEEE design into a **fully verified and layout-ready hardware model**, demonstrating both **research understanding** and **practical engineering execution**.

---

