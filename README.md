<!-- HEADER BANNER -->
<div align="center">

# Rajesh Reddy M

### Embedded Security · Trusted Execution · Low-Level Systems

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=00C9A7&center=true&vCenter=true&width=600&lines=ARM+TrustZone+%7C+OP-TEE+%7C+Firmware+Attestation;M.Tech+Cyber+Security+%40+IIT+Delhi;Security+that's+enforced+%E2%80%94+not+assumed.)](https://git.io/typing-svg)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rajesh%20Reddy-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/m-rajesh-reddy-463658170)
[![Email](https://img.shields.io/badge/Email-reddy.rajesh011%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reddy.rajesh011@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-10GiC10V38-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/10GiC10V38)

</div>

---

## 👋 Who I am

I work at the intersection of **embedded security, trusted execution, and low-level systems**. I build things that run close to the metal — firmware, secure enclaves, attestation systems — in environments where getting it wrong has real consequences.

Currently finishing my M.Tech in Cyber Security at **IIT Delhi**, where my thesis involves building a hardware-rooted attestation system for UAV flight controllers using ARM TrustZone and OP-TEE. Before this, I spent two years deploying and securing mission-critical SCADA networks for a power grid operator, and interned with the **Army Cyber Group (Ministry of Defence)** doing security testing on hardened systems.

> *I care about security that's actually enforced — not assumed.*

---

## 🛠️ What I work on

<table>
<tr>
<td valign="top" width="50%">

**🔐 Trusted Execution & Attestation**
- ARM TrustZone · OP-TEE · TF-A
- Global Platform TEE API · Secure Boot
- Control-flow attestation (BLAST, CCS 2023)
- SHA-256 hash attestation · S-EL0 / EL3

**⚙️ Embedded Systems & Firmware**
- Cortex-M4 / ARMv7-M · ARMv8
- ChibiOS RTOS · ArduPilot · MAVLink
- Pixhawk fmuv2 · NVIDIA Jetson · Linux

</td>
<td valign="top" width="50%">

**⚡ Low-Level Performance**
- AVX2 SIMD · Cache-aware algorithms
- OpenMP wavefront parallelism · CUDA
- Perf · GDB · QEMU

**🌐 Network & Security Engineering**
- Sophos NGFW · ACL & Firewall Policy
- L2/L3: RSTP, RIP, VLAN · SNMP
- SCADA/IED · Wireshark · OpenSSL
- PQC (Post-Quantum Cryptography) evaluation

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
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)

---

## 🚀 Projects

### 🛡️ UAV Mission Integrity Attestation System *(IIT Delhi Thesis — ongoing)*

Defense-in-depth security architecture for UAV flight controllers. Cross-compiled ArduPilot onto Pixhawk (Cortex-M4, ChibiOS), with NVIDIA Jetson running OP-TEE as the secure enclave. Adapted the **BLAST control-flow attestation algorithm (CCS 2023)** for Cortex-M4 using Ball-Larus path profiling. Mission commands are hash-attested using SHA-256, with offline baselines provisioned into a Trusted Application via Global Platform TEE API. Validated end-to-end on real hardware.

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![ARM TrustZone](https://img.shields.io/badge/ARM%20TrustZone-0091BD?style=flat-square&logo=arm&logoColor=white)
![OP-TEE](https://img.shields.io/badge/OP--TEE-009900?style=flat-square&logoColor=white)
![Pixhawk](https://img.shields.io/badge/Pixhawk-Cortex--M4-important?style=flat-square)
![NVIDIA Jetson](https://img.shields.io/badge/NVIDIA-Jetson-76B900?style=flat-square&logo=nvidia&logoColor=white)

---

### 🔐 [SHA-256 Trusted Application on OP-TEE (ARM TrustZone)](https://github.com/10GiC10V38/optee-rpi3-work)

SHA-256 running inside a Secure World TEE on Raspberry Pi 3. Built a custom benchmarking framework using **inline ARM64 assembly (`cntpct_el0`)** to measure the exact cost of world-switching — isolating system latency, pure algorithm time, and memory copy overhead. Had to patch TEE Core kernel initialization to unlock PMU access from S-EL0. Real hardware, real numbers.

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

Took a naive O(N²) sequence alignment algorithm from 0.11 GCUPS to 7.10 GCUPS — a **65× speedup**. Cache-tiled blocking, wavefront diagonal parallelism, AVX2 SIMD with 16-bit unsigned saturation arithmetic.

| Metric | Before | After |
|---|---|---|
| Throughput | 0.11 GCUPS | **7.10 GCUPS** |
| Speedup | — | **65×** |
| L1 Cache Misses | baseline | −99.4% |
| Branch Mispredictions | baseline | −99.5% |

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![AVX2](https://img.shields.io/badge/AVX2%20SIMD-Intel-0071C5?style=flat-square&logo=intel&logoColor=white)
![OpenMP](https://img.shields.io/badge/OpenMP-Wavefront-informational?style=flat-square)

---

### 🖥️ XV6 OS Enhancements

Extended the xv6 teaching kernel with secure login, syscall-level access control, a priority-boosting scheduler, and demand paging with disk swap.

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Systems](https://img.shields.io/badge/Systems%20Programming-kernel-blueviolet?style=flat-square)


---

## 🏫 Background

| | |
|---|---|
| 🎓 **IIT Delhi** | M.Tech Cyber Security · 2024–Present · GPA 8.06 |
| 🏛️ **Army Cyber Group, MoD** | Security Testing Intern · May–Jul 2025 |
| ⚡ **TGTRANSCO** | Sub Engineer (Network & SCADA Security) · 2022–2024 |
| 💻 **Cloudio Pvt. Ltd.** | Associate Software Engineer · 2021–2022 |

---

## 📬 Get in touch

<div align="center">

[![Email](https://img.shields.io/badge/reddy.rajesh011%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reddy.rajesh011@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/m-rajesh-reddy-463658170)

*If you're working on something interesting in security — hardware, firmware, network, or otherwise — I'm happy to talk.*

</div>


