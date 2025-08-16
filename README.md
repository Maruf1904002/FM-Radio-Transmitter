# FM-Radio-Transmitter (Frequency Modulation)

**Duration:** February 2025 – March 2025  
**Platform:** Electronics-based project (no coding)  
**Design based on:** "High Fidelity FM Transmitter" by Joy Mukherji, Electronics‑For‑You, Dec 9 2017 :contentReference[oaicite:1]{index=1}

---

##  Project Overview

This project involves designing, building, and testing a **high-fidelity FM transmitter**, capable of transmitting audio across a short distance with good audio quality (covering audio frequencies up to 15 kHz). The design implements a **Phase-Locked Loop (PLL)** to lock the output frequency at 96 MHz, ensuring stability and fidelity :contentReference[oaicite:2]{index=2}.

---

## Components & Circuit Architecture

- **ICs Used:**
  - 74AC74 — Dual D-type flip-flop (VHF prescaler)
  - CD4060 — Ripple-carry binary counter
  - CD4046 — Phase-Locked Loop (PLL)
  - LM386 — Low-power audio amplifier
  - 7805 — 5 V Voltage regulator

- **Key Circuit Blocks:**
  - **Voltage-Controlled Oscillator (VCO):** Built using T1 (transistor), resistors (R1–R3), capacitors (C2, C5), inductor (L1), trimmer capacitor (VC1), and varactor diode (D1). This forms a Pierce-configured oscillator :contentReference[oaicite:3]{index=3}.
  - **Frequency Division & PLL Locking:**
    - The VCO output is divided by 4 using the flip-flop (IC1), producing ~24 MHz.
    - Further division by 32 via CD4060 (IC3).
    - A reference oscillator via another CD4060 (IC5) generates 750 kHz.
    - CD4046 (IC4) compares the divided signals, ensuring stable output at 96 MHz by feeding back to the VCO :contentReference[oaicite:4]{index=4}.
  - **Audio Amplifier & Modulation:** LM386 conditions input audio and injects frequency modulation into the VCO.

---

## Materials & Tools

- **PCB Design:** EasyEDA  
- **Circuit Diagrams & Block Diagrams:** Edraw Max  
- **Documentation:** Microsoft Word

---

## Performance & Testing

- **Frequency Range:** Centered at 96 MHz, locked via PLL, ensures frequency stability.
- **Audio Fidelity:** High fidelity achieved by transmitting audio up to 15 kHz :contentReference[oaicite:5]{index=5}.
- **Modulation Quality:** Stable and clean due to PLL locking mechanism.

---

## Repository Structure
/Photos/assembled_board.jpg
/Circuit_Diagrams/schematic.png

