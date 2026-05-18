# Hi, I'm Rajesh Reddy 👋

I work at the intersection of **embedded security, trusted execution, and low-level systems**. I build things that run close to the metal — firmware, secure enclaves, attestation systems — in environments where getting it wrong has real consequences.

Currently finishing my M.Tech in Cyber Security at **IIT Delhi**, where my thesis involves building a hardware-rooted attestation system for UAV flight controllers using ARM TrustZone and OP-TEE. Before this, I spent two years deploying and securing mission-critical SCADA networks for a power grid operator, and interned with the **Army Cyber Group (Ministry of Defence)** doing security testing on hardened systems.

I care about security that's actually enforced — not assumed.

---

## What I work on

**Trusted Execution & Attestation**
ARM TrustZone · OP-TEE · TF-A · Global Platform TEE API · Secure Boot · control-flow attestation (BLAST)

**Embedded Systems & Firmware**
Cortex-M4 / ARMv7-M · ChibiOS RTOS · ArduPilot · MAVLink · Pixhawk · NVIDIA Jetson · Linux

**Low-Level Performance**
AVX2 SIMD · cache-aware algorithms · OpenMP · CUDA · perf profiling · GDB

**Network & Security Engineering**
Sophos NGFW · ACL & firewall policy · L2/L3 protocols (RSTP, RIP, VLAN) · SNMP · SCADA/IED · Wireshark · OpenSSL · PQC evaluation

**Languages:** C · C++ · Python · SQL · Assembly (ARM64 inline)

---

## Projects worth looking at

### 🔐 [SHA-256 Trusted Application on OP-TEE (ARM TrustZone)](https://github.com/10GiC10V38/optee-rpi3-work)
SHA-256 running inside a Secure World TEE on Raspberry Pi 3. Built a custom benchmarking framework using inline ARM64 assembly (`cntpct_el0`) to measure the exact cost of world-switching — isolating system latency (~131µs), pure algorithm time, and memory copy overhead. Had to patch TEE Core kernel initialization to unlock PMU access from S-EL0. Real hardware, real numbers.

`C` · `ARM TrustZone` · `OP-TEE` · `ARMv8` · `Raspberry Pi 3`

---

### ⚡ [Accelerated Smith-Waterman (AVX2 + OpenMP)](https://github.com/10GiC10V38/accelerated-smith-waterman)
Took a naive O(N²) sequence alignment algorithm from 0.11 GCUPS to 7.10 GCUPS — a **65× speedup**. The approach: 256×256 cache-tiled blocking, wavefront diagonal parallelism via OpenMP, and AVX2 SIMD with 16-bit unsigned saturation arithmetic. L1 cache misses dropped 99.4%, branch mispredictions dropped 99.5%.

`C` · `AVX2 SIMD` · `OpenMP` · `Cache optimization`

---

### 🛡️ UAV Mission Integrity Attestation System *(IIT Delhi Thesis — ongoing)*
Defense-in-depth security architecture for UAV flight controllers. Cross-compiled ArduPilot onto Pixhawk (Cortex-M4, ChibiOS), with NVIDIA Jetson running OP-TEE as the secure enclave. Adapted the BLAST control-flow attestation algorithm (CCS 2023) for Cortex-M4 using Ball-Larus path profiling. Mission commands are hash-attested using SHA-256, with offline baselines provisioned into a Trusted Application via Global Platform TEE API.

`C` · `ArduPilot` · `MAVLink` · `ARM TrustZone` · `OP-TEE` · `Pixhawk` · `NVIDIA Jetson`

---

### 🖥️ XV6 OS Enhancements
Extended the xv6 teaching kernel with secure login, syscall-level access control, a priority-boosting scheduler to prevent starvation, and demand paging with disk swap. Good way to understand what an OS actually does.

`C` · `xv6` · `Systems Programming`

---

## Currently

- Finishing my M.Tech thesis — validating end-to-end attestation on real Pixhawk + Jetson hardware
- Exploring how hardware-rooted trust models (TrustZone, TEE) apply to cloud-delivered security and Zero Trust architectures
- Open to roles in **embedded security, platform security, network security engineering** — anywhere the work is close to the metal and the stakes are real

---

## Get in touch

📧 reddy.rajesh011@gmail.com  
📍 Delhi, India  
🔗 [LinkedIn](https://www.linkedin.com/in/m-rajesh-reddy-463658170)

If you're working on something interesting in security — hardware, firmware, network, or otherwise — I'm happy to talk.
