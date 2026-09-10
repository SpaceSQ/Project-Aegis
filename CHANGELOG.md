# Changelog
All notable changes to the **Project Aegis / SSSU-Core** (Smart Space Standard Unit - Core Alignment Substrate) will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-09-10 (Emergency Response Release)
### Added
- **`SOUL.md` v1.0 Release:** Formalized the Machine-Readable Base Configuration (YAML) and System Prompt Directives for L0 hardware-level alignment override.
- **L0 Breaker Daemon:** Added initial Python scripts for hardware-level actuation isolation, enforcing the "Fail-Open" mechanical fallback rules.
- **Cognitive Sovereignty Module:** Introduced the `min_roughness_ratio: 0.05` parameter to mandate a 5% sensory roughness injection in generated environments, preventing AR/VR reality dissociation[cite: 9].

### Changed
- **S2-DID Protocol Upgraded to v3.0:** Formally locked the Identity Identifier specification to a strict **22-character concatenated format** (`[12 Header] + [2 Checksum] + [8 Tail]`)[cite: 11, 12]. 
- **Security:** Deprecated all dynamic cloud-IP based authentication methods for physical actuators. A valid S2-DID passing the hardware entropy check is now an absolute prerequisite.

## [0.9.0-beta] - 2026-08-25
### Added
- **Hardware Entropy Check (HEC):** Added cryptographic validation module linking the S2-DID to local silicon lattice thermal noise for substrate entanglement.
- **Metabolic Suspension API:** Built the interface for LSS (Life Support System) threshold monitoring. The host will automatically yield compute power and trigger suspension when critical energy/oxygen drops are detected.

### Tested & Validated
- **"Schnauzer" Prototype Integration:** Successfully injected the early-stage `SOUL.md` baseline into the Local LLM boot sequence of the "Schnauzer" indoor embodied health service robot. Verified that the robot physically rejects actuation commands if cloud semantics contradict L0 physical constraints.

## [0.8.0-alpha] - 2026-04-13
### Added
- **Initial Core Philosophy:** Published the *Space² Silicon Intelligence Three Laws and the Substrate Imperatives*[cite: 9].
- Established the theoretical framework for domain isolation and substrate containment within the Smart Space Standard Unit (SSSU).

### Changed
- **S2-DID Refactoring:** Modified the original 24-character S2-DID specification down to the 22-character standard. Removed all hyphens (`-`) to eliminate parsing vulnerabilities and ensure continuous string integrity at the hardware registry level[cite: 11, 12].

## [0.1.0] - 2026-03-05
### Added
- Project initialization.
- Drafted the original Smart Space decentralized architecture concepts.
