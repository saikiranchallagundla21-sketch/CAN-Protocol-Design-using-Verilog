# CAN Protocol Implementation using Verilog

## Overview

This project implements a simplified **CAN (Controller Area Network) protocol** using Verilog HDL. It includes all major components of the CAN data communication system and simulates them on EDA Playground using Icarus Verilog. This project is suitable for FPGA simulation-based demonstration of the CAN protocol at the RTL level.

## Features

- UART-like Bit Timing using Baud Rate Generator
- CAN Frame Generation with:
  - Start of Frame (SOF)
  - Identifier (ID)
  - DLC (Data Length Code)
  - Data Field (DATA)
  - CRC Field (fixed for simulation)
  - ACK Field
  - End of Frame (EOF)
- CAN Frame Receiver
- CRC Checker (hardcoded for simplification)
- Acknowledgment Checker
- Testbench to verify the complete flow

## Modules

### 1. `baud_gen`
Generates baud rate ticks for timing control.

### 2. `can_frame_gen`
Generates a CAN frame from ID, DLC, and DATA inputs.

### 3. `can_frame_rx`
Receives and parses the CAN frame into ID, DLC, DATA.

### 4. `can_crc_checker`
Compares incoming CRC with expected CRC.

### 5. `ack_checker`
Generates and checks the ACK bit.

### 6. `can_top`
Integrates all modules and performs end-to-end CAN communication.

## Simulation Output

✅ Verified waveform showing:
- Frame transmitted and received correctly  
- CRC checked  
- ACK generated and verified  
- Status updates (OK or ERROR) shown on output  

## Tools Used

- **EDA Playground**
- **Icarus Verilog**
- **GTKWave** for waveform visualization

## How to Run

1. Open [EDA Playground](https://edaplayground.com/)
2. Paste the Verilog code of all modules and testbench.
3. Use **Icarus Verilog** as simulator.
4. Include `$dumpfile("dump.vcd"); $dumpvars;` for waveform.
5. Run simulation and view output on GTKWave.

## Applications

- Education and demonstration of CAN protocol basics.
- Entry-level FPGA-based automotive communication projects.
- Understanding of serial communication and framing concepts.

## Author

Challagundla Sai Kiran  
B.Tech – Electrical and Electronics Engineering  

---

**Feel free to fork and improve the design!**
