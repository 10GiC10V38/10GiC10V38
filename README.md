<!-- HEADER BANNER -->
<div align="center">

# Rajesh Reddy M

### Embedded Security · Trusted Execution · Control-Flow Attestation

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=00C9A7&center=true&vCenter=true&width=600&lines=ARM+TrustZone+%7C+OP-TEE+%7C+Firmware+Attestation;M.Tech+Cyber+Security+%40+IIT+Delhi;Security+that's+enforced+%E2%80%94+not+assumed.)](https://git.io/typing-svg)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rajesh%20Reddy-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/m-rajesh-reddy-463658170)
[![Email](https://img.shields.io/badge/Email-reddy.rajesh011%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reddy.rajesh011@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-10GiC10V38-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/10GiC10V38)

</div>

---

## 👋 Who I am

I work at the intersection of **embedded security, trusted execution, and compiler instrumentation**. I build things that run close to the metal — firmware, secure enclaves, attestation systems — in environments where getting it wrong has real consequences.

Currently finishing my M.Tech in Cyber Security at **IIT Delhi**, where my thesis builds a hardware-rooted attestation system for UAV flight controllers using ARM TrustZone and OP-TEE. My research involves implementing and empirically comparing three control-flow attestation systems (C-FLAT, OAT, BLAST) on AArch64 using LLVM instrumentation — the first unified comparison of these systems on 64-bit ARM with OP-TEE. Before this, I spent two years deploying and securing mission-critical SCADA networks for a power grid operator, and interned with the **Army Cyber Group (Ministry of Defence)** doing security testing on hardened systems.

> *Security that's enforced — not assumed.*

---

## 🔬 Research

I've implemented and empirically compared three control-flow attestation (CFA) systems on **AArch64 with ARM TrustZone / OP-TEE** — the first known LLVM-based implementations of all three on 64-bit ARM:

| System | Paper | World Switches (syringe pump) | Verified Against Paper? |
|---|---|---|---|
| **C-FLAT** | CCS 2016 | ~7,516 | ✅ Exact iteration counts |
| **OAT** | IEEE S&P 2020 | ~1,946 TEE calls | ✅ Table III (488 branches, 1946 returns) |
| **BLAST** | CCS 2023 | **~4–8** | ✅ Table 3 within 0.001% (5 benchmarks) |

**Key result:** BLAST achieves a **1000–2000× reduction** in TEE world switches vs C-FLAT on identical hardware and benchmarks.

All implementations use LLVM IR compile-time instrumentation and the OP-TEE TEEC Client API on Raspberry Pi 3 (Cortex-A53).

---

## 🛠️ What I work on

<table>
<tr>
<td valign="top" width="50%">

**🔐 Trusted Execution & Attestation**
- ARM TrustZone · OP-TEE · TF-A
- Global Platform TEE API · Secure Boot
- C-FLAT · OAT · BLAST (CCS 2023)
- SHA-256 hash attestation · S-EL0 / EL3

**⚙️ Embedded Systems & Firmware**
- Cortex-M4 / ARMv7-M · ARMv8 / AArch64
- ChibiOS RTOS · ArduPilot · MAVLink
- Pixhawk fmuv2 · NVIDIA Jetson · Linux

</td>
<td valign="top" width="50%">

**🔧 Compiler & Instrumentation**
- AArch64 inline assembly · Register reservation
- Guard page / SIGSEGV-based buffer management

**🌐 Network & Security Engineering**
- Sophos NGFW · ACL & Firewall Policy
- L2/L3: RSTP, RIP, VLAN · SNMP
- SCADA/IED · Wireshark · OpenSSL
- PQC evaluation

</td>
</tr>
</table>

---

## 💻 Languages & Tools

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-004488?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Assembly](https://img.shields.io/badge/ARM64%20Assembly-0091BD?style=flat-square&logo=arm&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![GDB](https://img.shields.io/badge/GDB-A8212B?style=flat-square&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![OpenSSL](https://img.shields.io/badge/OpenSSL-721412?style=flat-square&logo=openssl&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logoColor=white)
![LLVM](https://img.shields.io/badge/LLVM-18-262D3A?style=flat-square&logo=llvm&logoColor=white)

---

## 🚀 Projects

### 🛡️ [UAV Mission Integrity Attestation System] *(IIT Delhi Thesis — ongoing)*

Defense-in-depth attestation for UAV flight controllers: Pixhawk fmuv2 (Cortex-M4, ChibiOS/ArduPilot) as the untrusted edge node, NVIDIA Jetson running OP-TEE as the secure verifier. SHA-256 hash-attests mission commands; BLAST (CCS 2023) attests control-flow via Ball-Larus path profiling.

| Metric | Value |
|---|---|
| End-to-end attestation latency | ~104 ms |
| Jetson OP-TEE TA round-trip | 75.2 ms (72.3% of total) |
| CFA overhead on Cortex-M4 | 170 µs per mission emit |
| Flash footprint (instrumentation) | +2,940 B (0.30% of budget) |
| Net RAM increase | 0 |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![ARM TrustZone](https://img.shields.io/badge/ARM%20TrustZone-0091BD?style=flat-square&logo=arm&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![Pixhawk](https://img.shields.io/badge/Pixhawk-Cortex--M4-important?style=flat-square)
![NVIDIA Jetson](https://img.shields.io/badge/NVIDIA-Jetson-76B900?style=flat-square&logo=nvidia&logoColor=white)

---

### 📊 [BLAST Control-Flow Attestation on AArch64](https://github.com/10GiC10V38/blast-attestation)

First LLVM-based implementation of BLAST (CCS 2023) on AArch64 with OP-TEE. Register-based path accumulation using reserved AArch64 registers (x28/w20) with guard-page double buffering — reducing TEE world switches from ~7,516 (C-FLAT) to ~4–8 per operation.

| Metric | Value |
|---|---|
| World switches vs C-FLAT | **~1000–2000× reduction** |
| Log count accuracy (5 Embench benchmarks) | **< 0.001% error** vs paper Table 3 |
| Optimization level required | -O0 (inlining breaks instrumentation) |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/LLVM%20Pass-C++-004488?style=flat-square&logo=cplusplus&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![RPi3](https://img.shields.io/badge/Raspberry%20Pi%203-C51A4A?style=flat-square&logo=raspberrypi&logoColor=white)

---

### 🔍 [C-FLAT Control-Flow Attestation on AArch64](https://github.com/10GiC10V38/C-FLAT-RPi3-Implementation)

LLVM IR implementation of C-FLAT (CCS 2016) on Raspberry Pi 3 with OP-TEE — ported from ARMv7 binary hooks to AArch64 compile-time instrumentation. Includes shadow call stack, loop record tracking, and a syringe pump case study with exact iteration verification.

| Syringe Command | Expected Steps | Measured |
|---|---|---|
| 10 µL bolus | 68 | ✅ 68 |
| 20 µL bolus | 136 | ✅ 136 |
| 100 µL bolus | 682 | ✅ 682 |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/LLVM%20Pass-C++-004488?style=flat-square&logo=cplusplus&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![RPi3](https://img.shields.io/badge/Raspberry%20Pi%203-C51A4A?style=flat-square&logo=raspberrypi&logoColor=white)

---

### 🔒 [OAT Operation Attestation on AArch64](https://github.com/10GiC10V38/OAT-RPi3-Implementation)

LLVM IR implementation of OAT (IEEE S&P 2020) on Raspberry Pi 3 with OP-TEE. Includes shadow stack for ROP detection, SHA-256 hash chain over all control-flow events, and a Python verifier for offline attestation proof verification. Demonstrated live ROP attack detection on a drone controller test case.

| Metric | Value |
|---|---|
| Syringe pump branches | 488 ✅ matches paper Table III |
| Syringe pump returns | 1946 ✅ matches paper Table III |
| ROP detection | ✅ Shadow stack mismatch → TEE_ERROR_SECURITY |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/LLVM%20Pass-C++-004488?style=flat-square&logo=cplusplus&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![RPi3](https://img.shields.io/badge/Raspberry%20Pi%203-C51A4A?style=flat-square&logo=raspberrypi&logoColor=white)

---

### 🔐 [SHA-256 TEE Benchmarking](https://github.com/10GiC10V38/tee-sha256-benchmark)

SHA-256 inside OP-TEE Secure World on RPi3. Custom cycle-accurate benchmarking using inline ARM64 assembly (`cntpct_el0`) to isolate World Switch latency, memory copy cost, and algorithm time. Diagnosed and patched a TEE Core kernel panic (`0xdeadbeef`) by setting `PMUSERENR_EL0` at S-EL1 to enable PMU access from S-EL0.

| Metric | Value |
|---|---|
| Throughput (Secure World) | ~11 MB/s |
| World Switch Latency | ~131 µs |
| Overhead vs native sha256sum | 1.4× (38%) |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![ARM TrustZone](https://img.shields.io/badge/ARM%20TrustZone-0091BD?style=flat-square&logo=arm&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![RPi3](https://img.shields.io/badge/Raspberry%20Pi%203-C51A4A?style=flat-square&logo=raspberrypi&logoColor=white)

---

### ⚡ [Accelerated Smith-Waterman (AVX2 + OpenMP)](https://github.com/10GiC10V38/accelerated-smith-waterman)

65× speedup on sequence alignment using cache-aware tiling, wavefront parallelism, and AVX2 SIMD.

| Metric | Before | After |
|---|---|---|
| Throughput | 0.11 GCUPS | **7.10 GCUPS** |
| L1 Cache Misses | baseline | −99.4% |
| Branch Mispredictions | baseline | −99.5% |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![AVX2](https://img.shields.io/badge/AVX2%20SIMD-Intel-0071C5?style=flat-square&logo=intel&logoColor=white)
![OpenMP](https://img.shields.io/badge/OpenMP-Wavefront-informational?style=flat-square)

---

## 🏫 Background

| | |
|---|---|
| 🎓 **IIT Delhi** | M.Tech Cyber Security · 2024–Present · GPA 8.06 |
| 🏛️ **Army Cyber Group, MoD** | Security Testing Intern · May–Jul 2025 |
| ⚡ **TGTRANSCO** | Sub Engineer (Network & SCADA Security) · 2022–2024 |

---

## 📬 Get in touch

<div align="center">

[![Email](https://img.shields.io/badge/reddy.rajesh011%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reddy.rajesh011@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/m-rajesh-reddy-463658170)

*Open to roles in embedded security, TEE/firmware engineering, and systems security research.*

</div>
