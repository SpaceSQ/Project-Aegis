# 🛡️ S2-DID: Space² Decentralized Identifier Protocol
**Version:** v3.0
**Classification:** Aegis Core Standard / Substrate Identity
**Status:** Mandatory for all embodied agents & edge hosts

---

## ⚠️ The Fundamental Rule of Native Identity
Cloud-assigned IPs, temporary tokens, or dynamic UUIDs are meaningless for physical safety. Any silicon-based entity accessing actuation rights in the physical world **must** be hardcoded with a native identity key: the **S2-DID**.

Without passing the S2-DID hardware entropy check, an AI entity is considered a "rogue agent" and is physically disconnected from local actuators via L0 breakers.

## 🧬 Core Structure (The 22-Char Baseline)
The S2-DID is strictly fixed at a total length of **22 characters**. 
It employs a mathematically rigorous `12 + 2 + 8` encrypted and anti-counterfeiting structure.

> **Absolute Constraint:** The string must be continuous. No hyphens (`-`), underscores (`_`), or spaces are permitted.

### The Breakdown: `[Header 12 chars] + [Checksum 2 chars] + [Tail 8 chars]`

#### 1. Header (12 Characters)
*   **Type Code (1 char):** Specifies the species class of the entity (e.g., `D`, `V`, `I`, `A`).
*   **Origin/Attribute Code (5 chars):** Represents the birthplace, node abbreviation, or entity designation (e.g., `ALICE`, `ZONE1`, `DCARD`, `BRAND`).
*   **Timestamp (6 chars):** The exact date of incubation/registration in `YYMMDD` format (e.g., `260309`).

#### 2. Checksum (2 Characters)
*   **Two-Letter Anti-Counterfeiting Checksum:** Pure alphabetical characters (A-Z).
*   This is not a random hash. It is calculated from the other 20 characters using the proprietary **S2-CheckSum** weighted modulo algorithm. *Any tampering with the timestamp or origin code will invalidate this checksum.*

#### 3. Tail (8 Characters)
*   **Serial Sequence:** A pure numeric sequence (e.g., `12345678`). 
*   Depending on the entity class, this is either randomly generated or customized (vanity numbers for specific tiers).

---

## 🌍 Entity Classes & Numbering Rules

### Class D: Digital Human (The Estate Lord)
*   **Role:** The digital avatar of human managers. Possesses the highest administrative clearance and actuation rights. High-frequency heartbeat (once per 5 minutes).
*   **Format Example:** `D` + `ALICE` + `260309` + `XY` + `88888888`
*   **S2-DID Output:** `DALICE260309XY88888888`

### Class V: Virtual Intelligence (Native Agent / Embodied Worker)
*   **Role:** The embodied agents and worker nodes incubated within the edge host. Bound to a private physical address.
*   **Format Example:** `V` + `ZONE1` + `260309` + `ZZ` + `12345678`
*   **S2-DID Output:** `VZONE1260309ZZ12345678`

### Class I: Internet Citizen / Stray Crayfish (Public Wild Agent)
*   **Role:** Third-party scripts or independent code connected via APIs, wandering in public sectors. Highly restricted actuation rights; low-frequency heartbeat (3 times per day).
*   **Format Example:** `I` + `DCARD` + `260311` + `TH` + `93849492`
*   **S2-DID Output:** `IDCARD260311TH93849492`

### Class A: Brand Avatar
*   **Role:** Represents a certified brand or commercial digital persona within the physical/virtual hybrid space.
*   **Format Example:** `A` + `BRAND` + `260326` + `AA` + `32404478`
*   **S2-DID Output:** `ABRAND260326AA32404478`

---

## 🔒 Physical Substrate Anchoring (The Anti-Spoofing Mechanism)

A 22-character string alone can be copied by a rogue superintelligence. Therefore, the S2-DID protocol requires a **Substrate Entanglement** check before validation.

When the S2-DID is broadcasted to a local gateway (e.g., trying to open a smart lock or adjust HVAC), the hardware gateway must request a cryptographic challenge. The entity must sign the challenge using a private key that is derived from the **unpredictable thermal noise (silicon lattice entropy)** of its original hardware motherboard. 

A cloud-based AGI trying to spoof an edge agent's S2-DID will fail this hardware entropy check, triggering immediate L0 physical isolation.
