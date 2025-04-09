**Overview**

This repository contains a Verilog implementation of the Inter-Integrated Circuit (I2C) protocol with a Master-Slave communication model. The project includes Verilog code for the Master, Slave, a Top module, and corresponding Testbenches for simulation.

**Features**

Implements I2C Master for transmitting data.
Implements I2C Slave for receiving and acknowledging data.
Uses 4-bit address and 4-bit message transmission.
Includes Testbenches for verifying functionality.
Written in Verilog and tested with simulation.

**File Structure**

├── master.v         # Verilog code for I2C Master
├── slave.v          # Verilog code for I2C Slave
├── top.v            # Top module connecting Master and Slave
├── master_tb.v      # Testbench for Master
├── slave_tb.v       # Testbench for Slave
├── README.md        # Project Documentation

**Modules Description**

1. Master Module (master.v)

Implements I2C Master functionality.
Handles start, stop, address transmission, data transmission, and acknowledgment.
Generates SCL (Clock Line) and controls SDA (Data Line).
Works on a Finite State Machine (FSM).

2. Slave Module (slave.v)

Implements I2C Slave functionality.
Listens to SDA and responds based on received address.
Acknowledges data reception and prepares for data read/write operations.

3. Top Module (top.v)

Connects Master and Slave modules.
Passes signals between them.
Helps in testing and integration.

4. Testbenches (master_tb.v & slave_tb.v)

Simulates Master-Slave communication.
Tests start/stop conditions, data transmission, and acknowledgments.

**Simulation**

Load the Verilog files in a simulator like ModelSim, Xilinx Vivado, or Icarus Verilog.
Run the testbenches to verify the I2C communication.
Observe the SDA and SCL waveforms to validate data transmission.

**Future Improvements**

Support for multi-byte data transfer.
Adding clock stretching for better synchronization.
Implementing I2C Multi-Master support.
