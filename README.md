# HIL (Hardware-In-The-Loop) Motor Simulation Core

This project implements a real-time motor behavior emulator on an FPGA using **VHDL**. It is designed to simulate the physical response (inertia and acceleration) of a DC motor to PWM control signals.

## Key Features
- **PWM Capture Logic:** Decodes incoming PWM signals into an 8-bit duty cycle (0-255).
- **Motor Plant Emulation:** Implements a behavior model that simulates physical acceleration and deceleration using **Fixed-Point Arithmetic**.
- **Real-Time Performance:** Designed for low-latency HIL (Hardware-In-The-Loop) testing environments.
- **Scalable Architecture:** Easily integrable into larger autonomous vehicle or robotics projects.

## Simulation Results
The following waveform shows the **20ms** simulation of the motor's response. You can clearly see the linear acceleration ramp when the PWM signal is applied, followed by the steady-state performance at maximum speed.

![Motor Simulation Ramp](simulation_result.png)

*The `motor_speed_out` signal follows a precise ramp-up curve, proving the successful emulation of motor inertia.*

## Technical Details
- **Hardware Description Language:** VHDL
- **Simulation Tool:** Vivado Design Suite
- **Target Frequency:** 100 MHz
- **Arithmetic:** 16-bit internal registers for high-precision speed calculation.

## Project Structure
- `src/`: Contains the synthesizable RTL source codes (`hil_top`, `pwm_capture`, `motor_model`).
- `sim/`: Contains the testbench for verification.
- `docs/`: Includes simulation waveforms and documentation assets.

---
**Developed by Mehmet Bera Kaya
