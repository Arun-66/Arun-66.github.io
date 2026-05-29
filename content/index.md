---
layout: main
title: Arun Murugappan I
subtitle: "Digital design, hardware verification, and FPGA systems."
position: NoC Verification Intern
company: InCore Semiconductors
location: Bengaluru, Karnataka
social_links:
  - {name: Email, url: "mailto:arun.i.murugappan@gmail.com", icon: email}
  - {name: GitHub, url: "https://github.com/Arun-66", icon: github}
  - {name: LinkedIn, url: "https://www.linkedin.com/in/arun-murugappan-i", icon: linkedin}
news:
  - date: "Jan 2026"
    text: "Joined InCore Semiconductors as a NoC Verification Intern, working on AMBA AHB/APB verification using Embedded UVM in D."
  - date: "Nov 2024"
    text: "CNR Rao Scholarship recipient — merit certificate and 40% tuition fee refund for ranking in the top 20 students by SGPA at PES University."
  - date: "Nov 2024"
    text: "Started Dynamic Partial Reconfiguration project at CHIPS PES University — run-time adaptive reconfiguration of a RISC-V co-processor using Xilinx Vivado DFX."
featured_pubs:
  - title: "Nanoclay-Based Conductive EMI Shielding Silver Decorated PANI"
    venue: "Research Publication"
    abbr: "Ag-PANI"
    coauthors: "Arun Murugappan I et al."
---

I'm a final-year Electronics and Communications Engineering student at [PES University](https://pes.edu/), graduating in June 2026 with a GPA of 7.93/10. I'm currently a NoC Verification Intern at [InCore Semiconductors](https://incoresemi.com/), where I work on AMBA AHB/APB/AXI4 verification using Embedded UVM in the D language — rewriting golden reference models, scoreboards, sequences, and drivers for scalable, design-independent verification frameworks.

My work spans the full hardware stack: RTL design and verification in SystemVerilog and Verilog, physical design through RTL-to-GDSII flows using Cadence toolchains, and FPGA implementation on Xilinx platforms. Projects have ranged from a complete RV32IM SoC with UART and SPI peripherals to a full FIFO implementation taken from RTL to GDSII using the SCL180 PDK, to hardware-software co-design for AES encryption on PYNQ-Z2.

### Research interests

**Processor and SoC design** — I've built multiple RISC-V cores from scratch: an RV32I core, an RV32IM core with full integer and multiply/divide support, and a complete SoC integrating UART and SPI peripherals with FPGA validation. The questions that interest me are around microarchitecture trade-offs, pipeline design, and how processors integrate with the rest of a system.

**FPGA-based neural network acceleration** — I've implemented both LeNet-5 and AlexNet on FPGAs using Vitis HLS, targeting the ZCU104 and PYNQ platforms. The challenge of mapping compute-intensive inference workloads onto fixed hardware — making the right decisions about parallelism, memory bandwidth, and precision — is what draws me here.

**Hardware security** — I've built AES encryption accelerators twice: once in Intel Quartus Prime (The Enigma) and once as a hardware-software co-design on PYNQ-Z2, with the datapath on the FPGA fabric and key generation in software over AXI. Cryptographic hardware is an area I want to go deeper in.

**Hardware verification** — At InCore Semiconductors I work on AMBA AHB/APB/AXI4 verification using Embedded UVM in D, building scalable verification frameworks that can be reused across multiple DUTs. Formal and functional correctness of hardware is a problem I find genuinely interesting.

**Physical design** — I've taken a FIFO from RTL through the full Cadence flow to GDSII using the SCL180 PDK, covering synthesis, placement and routing, timing closure, and DRC/LVS. I'm interested in the constraints that physical implementation puts on digital design decisions.

I also hold a publication on silver-decorated polyaniline nanocomposites (Ag-PANI) for EMI shielding, from my time as a Student Researcher at Quanad Lab.

### Leadership

I was Club Lead of Team Vegavath Racing Club at PES University from September 2022 to December 2024, and participated in Bootstrap 2k24 under the Department of Mechanical Engineering.

### Outside the lab

I build things — hardware and otherwise. If you're working on digital design, verification, or FPGA systems and want to talk, reach out.
