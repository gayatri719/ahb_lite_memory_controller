# ahb_lite_memory_controller
Verilog-based AHB-Lite memory controller with testbench, simulation results, and GDS layout generated using Cadence Virtuoso.
# 🧠 AHB-Lite Memory Controller (RTL to GDSII Implementation)

### 📘 Course:
**VLSI System Design Practice (EC307)**  
**Indian Institute of Information Technology, Design and Manufacturing, Kurnool**

---

## 🏁 Project Overview

This project involves the **design and implementation of an AHB-Lite Memory Controller** using **Verilog HDL**, followed by the **RTL-to-GDSII flow** using **Cadence EDA tools**.  
The goal is to bridge the gap between **RTL design** and **physical implementation**, ensuring correct functionality, timing closure, and a clean layout ready for fabrication.

---

## 🎯 Aim

To design, simulate, synthesize, and implement an **AHB-Lite Memory Controller** that supports read and write operations over the AHB-Lite protocol, and to perform **physical design using Cadence Genus and Innovus**.

---

## 🧰 Tools and Technologies Used

| Category | Tool / Language |
|-----------|-----------------|
| HDL Design | Verilog HDL |
| Functional Simulation | Cadence INCISIVE / ModelSim |
| Synthesis | Cadence Genus |
| Physical Design | Cadence Innovus |
| OS / Environment | Linux (RHEL / Ubuntu) |
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
- Implemented in **Verilog HDL**.
- Verified for functional correctness using a **testbench**.

### 2️⃣ Functional Simulation
- Simulated using Vivado.
- Verified read/write behavior and data integrity.

### 3️⃣ Synthesis (Cadence Genus)
- RTL synthesized into **gate-level netlist**.
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
|------------|--------------|
| **Timing Report** | Slack and critical path delay after synthesis |
| **Area Report** | Total cell area and utilization |
| **Power Report** | Dynamic and leakage power analysis |
| **GDSII Layout** | Final 2D physical design layout exported from Innovus |

---




