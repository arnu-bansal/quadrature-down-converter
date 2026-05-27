# quadrature-down-converter

Complete quadrature down conversion system featuring I/Q mixing, FFT phase analysis, RF signal translation, and simulation-to-hardware verification.

## Overview

This project presents the design, simulation, and hardware implementation of a complete **Quadrature Down Converter (QDC)** for RF signal processing applications. The system performs frequency translation by mixing an input RF signal with two quadrature local oscillator signals separated by approximately 90°, generating in-phase (I) and quadrature (Q) intermediate-frequency outputs.

The project was developed as part of the Analog Electronic Circuits course at the International Institute of Information Technology Hyderabad.

## Features

- Quadrature oscillator using UA741 op-amps
- I/Q signal generation with ~90° phase separation
- NMOS switch-based mixer implementation
- RC low-pass filtering for IF extraction
- FFT-based phase and frequency analysis
- Complete LTspice simulation workflow
- Breadboard hardware implementation and validation
- Simulation-to-hardware performance comparison

---

## System Architecture

```text
RF Input
   │
   ▼
+-------------------+
| Quadrature        |
| Oscillator        |
| (I and Q LO)      |
+-------------------+
      │      │
      ▼      ▼
+---------+ +---------+
| I Mixer | | Q Mixer |
+---------+ +---------+
      │      │
      ▼      ▼
+---------+ +---------+
| LPF (I) | | LPF (Q) |
+---------+ +---------+
      │      │
      ▼      ▼
+-------------------+
| Output Amplifiers |
+-------------------+
      │
      ▼
 Final I/Q Outputs
```

---

## Key Concepts

This project explores several important RF and analog signal processing concepts:

- Quadrature (I/Q) signal processing
- Frequency translation
- Mixer nonlinearity
- Image rejection
- Intermediate frequency (IF) extraction
- FFT-based phase analysis
- Analog oscillator design
- Hardware non-idealities and parasitics

---

## Design Specifications

| Parameter | Value |
|---|---|
| Oscillator Frequency | ~170 kHz |
| Phase Difference | ~90° |
| LPF Cutoff Frequency | ~3 kHz |
| RF Input Amplitude | 100 mV |
| Supply Voltage | ±12 V |
| Mixer Technology | NMOS Switch Mixer |

---

## Results

### Oscillator Performance
- Simulated Frequency: 169.3 kHz
- Measured Frequency: ~170.68 kHz
- I-Q Phase Difference: ~90°

### FFT Phase Verification
- Measured FFT phase difference: **89.96°**

### Hardware Validation
- Successful generation of I and Q intermediate-frequency outputs
- Frequency translation verified experimentally
- Practical measurements closely matched LTspice simulations

---

## Tools and Technologies

- LTspice
- Oscilloscope
- Function Generator
- CMOS 180nm Model
- UA741 Op-Amps
- Breadboard Prototyping

---

## Simulation and Hardware Highlights

- Quadrature oscillator generated stable sinusoidal outputs
- NMOS mixers successfully produced sum and difference frequencies
- Low-pass filters extracted the desired IF component
- FFT analysis confirmed near-perfect quadrature behavior
- Hardware implementation validated simulation results within expected tolerances

---

## Authors

- Ekansh Wadhwa
- Arnav Bansal
- Abhinav Ray

Analog Electronic Circuits (EC2.103)  
International Institute of Information Technology Hyderabad

---

## References

1. Behzad Razavi — *RF Microelectronics*
2. Sedra & Smith — *Microelectronic Circuits*
3. IEEE papers on direct-conversion receivers and quadrature oscillators

---

## License

This project is intended for academic and educational purposes.
