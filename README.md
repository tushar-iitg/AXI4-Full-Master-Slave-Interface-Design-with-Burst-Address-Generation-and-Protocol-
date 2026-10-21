# AXI4-Full Master–Slave Interface Design with Burst Address Generation and Protocol Checking

A robust Verilog implementation of an AXI4-Full master-slave interface featuring complete support for read and write burst transactions, dynamic address generation, FSM-based channel control, and automated protocol checking.

---

## Features

- **AXI4-Full Protocol Support**: Implements full master and slave interfaces adhering to the AMBA AXI4 specification.
- **Burst Address Generation**: Supports all standard AXI burst types:
  - `FIXED`: Address remains constant for all beats within the burst.
  - `INCR`: Incrementing address calculated per transfer based on burst size.
  - `WRAP`: Wrapping burst behavior handling boundary limits for cache-line or circular buffer access.
- **FSM-Based Channel Control**: Dedicated Finite State Machines managing independent read and write address, data, and response channels.
- **Built-in Protocol Checker**: Real-time monitoring and assertions to validate handshaking rules (`VALID`/`READY`), burst length/size constraints, and transaction response codes.

---

## Architecture & Signals

The design coordinates the core AXI4 channels:
- **Write Address Channel** (`AW*`)
- **Write Data Channel** (`W*`)
- **Write Response Channel** (`B*`)
- **Read Address Channel** (`AR*`)
- **Read Data Channel** (`R*`)

---

## Repository Structure

```text
├── README.md
└── tb/              # Testbenches and protocol checker verification scripts
