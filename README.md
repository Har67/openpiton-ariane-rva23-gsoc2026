# openpiton-ariane-rva23-gsoc2026
GSoC 2026 — Architectural Improvements to OpenPiton+Ariane for RISC-V RVA23 Profile Compliance | FOSSi Foundation

# Architectural Improvements to OpenPiton + Ariane (CVA6) for RVA23 Compliance

## 📌 Overview
This project explores architectural enhancements to the OpenPiton + Ariane (CVA6) platform to move toward compliance with the RISC-V RVA23 profile.

OpenPiton is a scalable manycore framework developed at Princeton, and Ariane (CVA6) is a 64-bit RISC-V core from ETH Zurich. Together, they form a powerful open-source research platform.

## 🎯 Objective
- Analyze the integration of OpenPiton with CVA6
- Identify missing or disabled RISC-V RVA23 profile features
- Propose architectural and configuration-level improvements
- Prepare the platform for future FPGA and silicon optimization

## 🛠️ Work Done

### 1. Repository Setup
Successfully cloned required repositories:
- OpenPiton (Princeton University)
- CVA6 (OpenHW Group)

### 2. CVA6 Core Exploration
Explored core architecture modules including:
- Pipeline stages (fetch, decode, execute, commit)
- Load-store unit
- CSR handling
- Cache subsystem
- MMU and TLB

### 3. Configuration Analysis
Analyzed key configuration file:cva6/core/include/cv64a60ax_config_pkg.sv


### 🔍 Key Findings (RVA23 Gaps)

The following features are currently **disabled or missing**, which are relevant for RVA23 compliance:

| Feature | Status |
|--------|--------|
| Svnapot (NAPOT memory) | ❌ Disabled |
| Hypervisor Extension | ❌ Disabled |
| Vector Extension (V) | ❌ Disabled |
| Bit Manipulation (B) | ❌ Disabled |
| Shared TLB | ❌ Disabled |
| Debug Triggers (SDTRIG, Mcontrol6) | ❌ Disabled |

### 4. Supported Extensions
Already enabled:
- Zicntr (Counters)
- Zihpm (Performance counters)

## 🧠 Proposed Improvements

- Enable and validate Svnapot support
- Add support for Hypervisor extension
- Integrate Vector extension for performance scaling
- Enable Bit Manipulation instructions
- Improve TLB architecture with shared TLB support
- Extend debug capabilities (SDTRIG, Mcontrol6)

## 📸 Screenshots Included
- OpenPiton repository cloned
- CVA6 repository cloned
- Core module structure
- Configuration files showing disabled features

## 🚀 Future Work
- Implement missing extensions in RTL
- Verify functionality using simulation (Verilator/UVM)
- Benchmark performance improvements
- Ensure compliance with RVA23 profile

## 🧑‍💻 Skills & Tools
- Verilog / SystemVerilog
- RISC-V ISA
- Computer Architecture
- Git & Linux

## 📚 References
- OpenPiton: https://github.com/PrincetonUniversity/OpenPiton
- CVA6: https://github.com/openhwgroup/cva6

---

## ✨ Author
Harshitha Shetty  
GSoC 2026 Aspirant
