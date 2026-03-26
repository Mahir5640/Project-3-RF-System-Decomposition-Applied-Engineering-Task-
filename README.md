



# RF System Block Analysis: nRF52840

**Student Name:** Mahir Foysol Chowdhury
**Student ID:** s2416471 
**Device:** Nordic Semiconductor nRF52840 SoC  
**Datasheet Link:** [nRF52840 Product Specification](https://www.google.com/search?q=https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.1.pdf)

### RF Block Explanations

| RF System Block | Role & Function |
| :--- | :--- |
| **Information Source / MCU** | The **ARM Cortex-M4F** processor acts as the intelligence. It prepares data packets, handles the Bluetooth stack, and instructs the radio when to transmit or receive. |
| **RF Transceiver** | This is the core 2.4 GHz radio unit. It converts digital data into radio waves for transmission (TX) and converts incoming radio waves back into digital data during reception (RX). |
| **Modulation / Demodulation** | The device uses **GFSK (Gaussian Frequency Shift Keying)** for BLE. During TX, it shifts the carrier frequency to represent 1s and 0s; during RX, it detects these shifts to recover the original bitstream. |
| **Power Amplifier (PA)** | The PA boosts the signal strength before it leaves the chip. It allows the user to configure output power (up to +8 dBm) to ensure the signal can reach the intended destination. |
| **Low Noise Amplifier (LNA)** | The LNA is the first stage of the receiver. It amplifies very weak incoming signals from the antenna while adding as little electronic noise as possible to maintain signal clarity. |
| **RF Filtering / Matching** | This is an external network of inductors and capacitors. It ensures the chip's impedance matches the antenna (usually 50Ω) and filters out unwanted harmonic frequencies to meet regulatory standards. |
| **Antenna Interface** | This is the physical connection point (ANT pin). It transitions the RF signal from the PCB traces into the air via a printed PCB antenna or a chip antenna. |
| **Power Supply (RF Section)** | The RF section is powered by internal **LDOs or a DC/DC converter**. This provides a clean, stable voltage to the radio components to prevent power fluctuations from interfering with signal quality. |


