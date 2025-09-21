# Chirp-Based Impedance Spectroscopy — A Wideband Alternative

**Authors:** Adam Gottesman (methodology, firmware, circuit design), Georgi Korchakov (PCB layout, circuit & simulation)  
**Affiliation:** Imperial College London • **Date:** March 2025

This repository hosts the final PDF for a fast, wideband impedance spectroscopy method based on **chirp excitation**. The system implements an I–V approach on an STM32 Nucleo (STM32F446RE), generating the stimulus on the 12-bit DAC and sampling three synchronized ADC channels. Impedance is computed from the DFT of the measured voltage/current, with discussion of chirp design, spectral leakage, and **matched-filter pulse compression** to counter quadratic phase dispersion. :contentReference[oaicite:0]{index=0}

## File
- [`chirp_impedance.pdf`](chirp_impedance.pdf) — complete report (background, design, implementation details, and results) :contentReference[oaicite:1]{index=1}

## Highlights (what’s inside)
- **Method:** I–V measurement; compute \( Z(f)=V(f)/I(f) \) from DFT of captured waveforms. :contentReference[oaicite:2]{index=2}  
- **Hardware/DSP path:** 12-bit DAC stimulus; 3× ADC channels at 250 kHz; LUT-based chirp generation (16,384 samples) with 1 MHz DAC clock; 4,096-sample acquisitions. :contentReference[oaicite:3]{index=3}  
- **Excitation design:** Linear vs **Gaussian-tapered** linear chirps; leakage reduction and practical limits. :contentReference[oaicite:4]{index=4}  
- **Phase issue & fix:** Quadratic phase accumulation in chirps and **pulse-compression matched filtering** as the remedy. :contentReference[oaicite:5]{index=5}  
- **Firmware:** Bare-metal **CMSIS** implementation with timers, DMA, synchronized DAC/ADC, and autoranging flow. :contentReference[oaicite:6]{index=6}  
- **Schematic:** Final measurement front-end and signal path. :contentReference[oaicite:7]{index=7}

## How to cite
> Gottesman, A., & Korchakov, G. *Chirp-Based Impedance Spectroscopy: A Wideband Alternative to Traditional Sinusoidal Methods.* Imperial College London, March 2025. :contentReference[oaicite:8]{index=8}

## Keywords
impedance spectroscopy, chirp excitation, matched filtering, pulse compression, EEG/biopotential front-ends, STM32, CMSIS, DMA, DFT/FFT :contentReference[oaicite:9]{index=9}

---

*The PDF includes all methodology, equations, implementation details, and figures; this repository intentionally contains just the final document.* :contentReference[oaicite:10]{index=10}
