# Communication System Lab

My labs and final project for **Communication System Laboratory** (通訊系統實驗) at National Tsing Hua University (Fall 2024). A software-defined radio course: transmitters and receivers are built in **LabVIEW** and run over the air on **NI USRP B210** radios.

- **Instructor:** Prof. Shin-Lin Shieh (謝欣霖)
- **Author:** Yu-Shuo Chang (張育碩)
- **Lab partner:** 蘇采宜

## Labs at a glance

| Folder | Topic | My blocks |
|---|---|---|
| [`Lab1-LabVIEW-USRP`](Lab1-LabVIEW-USRP) | Introduction to LabVIEW and the USRP | `student_BER.vi` (bit-error-rate measurement), simple `Tx.vi` / `Rx.vi`, a Simulink model (`lab1_2.slx`) |
| [`Lab2-Modulation`](Lab2-Modulation) | Digital modulation and demodulation (BPSK / QPSK) | `student_modulate.vi`, `student_decode.vi`, constellation captures |
| [`Lab3-Pulse-Shaping-Matched-Filter`](Lab3-Pulse-Shaping-Matched-Filter) | Raised-cosine pulse shaping and matched filtering | `student_pulse_shaping.vi`, `student_matched_filtering.vi`. The report shows eye diagrams over noise power and roll-off factor |
| [`Lab4-Symbol-Timing-Recovery`](Lab4-Symbol-Timing-Recovery) | Symbol timing recovery | `student_align_MaxEnergy.vi`: maximum-energy symbol alignment, with oversampling-factor and roll-off sweeps |
| [`Lab5-Frequency-Offset-Correction`](Lab5-Frequency-Offset-Correction) | Carrier frequency offset (CFO) estimation and correction | `Student_add_freq_offset.vi`, `Student_Moose.vi` (Moose CFO estimator), with constellations before and after correction |
| [`Final-Key-Fob`](Final-Key-Fob) | **Final project: car key-fob receiver** | Receives an ASK-modulated, pulse-encoded remote-control frame and recovers which key was pressed. The chain is envelope detection, integrate-and-dump, synchronization, and decoding. Report and slides only |

Every lab folder has `report.pdf`, a lab report written with my lab partner.

**Opening the files:** the `.vi` files need **LabVIEW** (with the NI-USRP driver). They call the course's shared libraries (`digital_comm.llb`, `wcl_RF1.0.llb`, the top-level Tx/Rx VIs), which are not included here, so they will not run on their own.

## Tools

- LabVIEW
- NI USRP B210
- MATLAB / Simulink
