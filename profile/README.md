# ProjectWork-Team69 🚀

<!-- Typing animation -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=2196F3&width=435&lines=AXI4+Compliant+RISC-V+MCU;Team+69+%7C+BMSCE+ECE;Building+the+Future+of+IoT)](https://git.io/typing-svg)


Welcome to the official repository of **Team 69** for the Major Project Work at **B.M.S College of Engineering**. This project focuses on developing a modern, high-performance AXI4 compliant RISC-V based Microcontroller Unit (MCU) designed for IoT applications and edge computing.

## 🎯 Project Overview

In the era of Internet of Things (IoT) and edge computing, traditional microcontrollers face significant limitations due to legacy interconnect protocols like AHB and APB. Our project addresses these challenges by implementing a complete System-on-Chip (SoC) built on the **AXI4 lite protocol**, enabling true parallelism and high-performance data processing.

### Key Features
- 🔥 **32-bit RISC-V Processor Core** with native AXI Master interface
- ⚡ **High-Performance DMA Controller** for efficient data transfers  
- 🔌 **Modular AXI-Lite Slave Peripherals** (GPIO, UART, SPI, Timers)
- 🧠 **Custom Multi-Channel Interrupt Controller**
- 💾 **Integrated SRAM Block** with AXI interface

## 👥 Team Members

| Name | USN |
|------|-----|
| **Sateesh Y A** | 1BM22EC223 |
| **Rohit Vishnu Achari** | 1BM22EC201 |
| **Ojas Kudari** | 1BM22EC154 |
| **Bhargavi S V** | 1BM22EC058 |

**Project Guide:** Dr. Maligi Anantha Sunil, Assistant Professor, ECE Department

## 🏗️ System Architecture

```
┌─────────────────┐                           ┌─────────────────┐
│   RISC-V CPU    │                           │ Interrupt Ctrl  │
│  (AXI Master)   │                           │  (AXI Slave)    │
└─────────┬───────┘                           └─────────┬───────┘
          │                                             │
          └──────────────┬───────────────────┬──────────┘
                         │                   │
                ┌────────▼───────────────────▼────────┐
                │          AXI4 Interconnect          │
                └─┬─────┬─────┬─────┬─────┬─────┬─────┘
                  │     │     │     │     │     │
              ┌───▼─┐ ┌─▼──┐ ┌▼───┐ ┌▼────┐ ┌─▼──┐ ┌▼────┐
              │GPIO │ │UART│ │SPI │ │Timer│ │SRAM│ │ ... │
              │Slave│ │Slv │ │Slv │ │ Slv │ │Slv │ │     │
              └─────┘ └────┘ └────┘ └─────┘ └────┘ └─────┘
```

## 📋 Project Execution Roadmap

### Phase 1: Foundation (Weeks 1-3)
- [x] **Requirement Analysis & Specification**
  - Define RISC-V ISA requirements
  - Specify AXI interface parameters
  - Document peripheral specifications

### Phase 2: Core Development (Weeks 4-8)  
- [ ] **RISC-V Core Design & Verification**
  - Implement 32-bit RISC-V core with AXI master interface
  - Develop comprehensive simulation testbenches
  - Verify instruction execution and pipeline functionality

### Phase 3: Peripheral Integration (Weeks 9-12)
- [ ] **Peripheral Development**
  - Implement AXI-Lite slave peripherals (GPIO, Timers)
  - Design complex peripherals with AXI adapters (UART, SPI, I²C)
  - Independent verification of each peripheral module

### Phase 4: System Integration (Weeks 13-15)
- [ ] **AXI Integration & System Wrapping**
  - Connect all components through AXI interconnect
  - Implement interrupt controller and power management
  - Create unified memory-mapped address space

### Phase 5: Validation (Weeks 16-18)
- [ ] **System Verification & Testing**
  - End-to-end system testing and validation
  - FPGA synthesis and hardware testing
  - Performance benchmarking and optimization

## 🛠️ Technical Specifications

### RISC-V Core
- **Architecture:** 32-bit RISC-V RV32I base instruction set
- **Interface:** Native AXI4 Master with burst support
- **Pipeline:** Multi-stage pipeline with hazard detection
- **Performance:** Target frequency of 100+ MHz

### AXI4 Implementation
- **Protocol:** AXI4 with 5 independent channels
- **QoS:** Quality of Service signaling for priority management

### Peripheral Suite
| Peripheral | Interface | Features |
|------------|-----------|----------|
| GPIO | AXI-Lite | 32-bit configurable I/O ports |
| UART | AXI-Lite + Adapter | Hardware flow control, FIFO buffers |
| SPI | AXI-Lite + Adapter | Master/Slave modes, configurable clock |
| Timer | AXI-Lite | 32-bit timers with interrupt generation |
| Interrupt Controller | AXI-Lite | Multi-channel priority-based controller |
| SRAM | AXI | High-speed on-chip memory |

## 🔬 Design Philosophy

Our approach emphasizes **strategic IP reuse** and **modular design**:

1. **Maximize Efficiency:** Focus on high-level integration of proven components
2. **Minimize Risk:** Leverage existing, validated IP blocks where possible  
3. **Enable Scalability:** Design modular, extensible architecture
4. **Ensure Performance:** Eliminate protocol bottlenecks through native AXI implementation

## 📚 Repository Structure

```
ProjectWork-Team69/
├── docs/                    # Documentation and specifications
├── rtl/                     # RTL source code
│   ├── cpu/                # RISC-V core implementation  
│   ├── peripherals/        # Peripheral modules
│   ├── interconnect/       # AXI interconnect logic
│   └── soc/               # Top-level SoC integration
├── testbench/              # Simulation and verification
├── synthesis/              # FPGA synthesis files  
├── software/               # Test software and drivers
└── tools/                  # Build scripts and utilities
```

## 🧪 Verification Strategy

- **Unit Testing:** Individual module verification with dedicated testbenches
- **Integration Testing:** System-level verification with complete SoC testbench
- **Hardware Validation:** FPGA implementation and testing on development board
- **Performance Analysis:** Benchmarking against industry standards

## 🎯 Target Applications

- **IoT Edge Devices:** Sensor fusion and real-time data processing
- **Embedded Systems:** High-performance control applications  
- **Automotive Electronics:** ADAS and vehicle control systems
- **Industrial Automation:** Real-time monitoring and control

## 📖 References & Literature

Our project builds upon extensive research in RISC-V and AXI-based systems:

1. **Low-Power RISC-V SoCs** for IoT applications
2. **Open-Source RISC-V Platforms** for democratized silicon design
3. **AXI Interconnect Design** for multi-core processor systems
4. **High-Performance AXI Controllers** using SystemVerilog
5. **Automotive Low-Power Technologies** for next-generation vehicles

## 🤝 Contributing

This is an academic project for BMSCE ECE Department. For questions or collaboration:

- **Email:** Contact team members through college email
- **Issues:** Use GitHub issues for technical discussions
- **Documentation:** Refer to `/docs` for detailed specifications

## 📄 Note

This project is developed for academic purposes at B.M.S College of Engineering as part of the PROJECT WORK-2 course (23EC7PWPJ2) for the 2025-26 academic year.

## 🏆 Acknowledgments

- **Dr. Maligi Anantha Sunil** - Project Guide and Mentor
- **Open Source Community** - RISC-V and AXI IP contributions

---

<div align="center">

**🎓 B.M.S College of Engineering**  
*Bull Temple Road, Basavanagudi, Bangalore - 560 019*  
*Department of Electronics and Communication Engineering*

[![BMSCE](https://img.shields.io/badge/BMSCE-blue?style=for-the-badge)](https://bmsce.ac.in)

[![Profile views](https://komarev.com/ghpvc/?username=ProjectWork-Team69&style=for-the-badge&color=brightgreen)](https://github.com/ProjectWork-Team69)
[![GitHub followers](https://img.shields.io/github/followers/ProjectWork-Team69?style=for-the-badge&logo=github)](https://github.com/ProjectWork-Team69)
[![GitHub User's stars](https://img.shields.io/github/stars/ProjectWork-Team69?style=for-the-badge&logo=github)](https://github.com/ProjectWork-Team69)

</div>
