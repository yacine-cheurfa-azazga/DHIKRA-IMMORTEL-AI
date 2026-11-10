# DHIKRA QUAD SYSTEM AI

**An ethical control layer between a human and an AI, with an offline deterministic core and explicit abstention**

Technical report TR-2026-QUAD-0018 · Version 2.6 · Public presentation

[![Zenodo](https://img.shields.io/badge/Zenodo-all%20versions-blue)](https://doi.org/10.5281/zenodo.23671062)
[![License](https://img.shields.io/badge/LICENSE-CC%20BY--NC--ND%204.0-red?style=for-the-badge)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![ORCID](https://img.shields.io/badge/ORCID-author-brightgreen)](https://orcid.org/)

---

## 🔴 LICENSE: CC BY-NC-ND 4.0

> ### 🔴 $\color{red}{\textbf{CC BY-NC-ND 4.0 International}}$
> $\color{red}{\textbf{Attribution · NonCommercial · NoDerivatives}}$
>
> **Commercial use is NOT permitted without the author's written authorization.**
> **Modification and derivative works are NOT permitted.**
> This applies to this repository **and** to the Zenodo record (version 2.6 onwards, DOI 10.5281/zenodo.24120357).
>
> Licensing requests: **dhikraemmortel@proton.me**

---

## Author

| | |
|---|---|
| **Author** | Yassa Yacine |
| **Affiliation** | Independent researcher, QUAD SYSTEM AI project |
| **ORCID** | [ORCID profile](https://orcid.org/) |
| **Licensing contact** | dhikraemmortel@proton.me |
| **Web address** | https://github.com/yacine-cheurfa-azazga/DHIKRA-IMMORTEL-AI |

## Zenodo versions

All versions are archived on Zenodo. The concept DOI always resolves to the latest version.

[![All versions DOI](https://img.shields.io/badge/DOI-all%20versions-blue)](https://doi.org/10.5281/zenodo.23671062)

| Version | Date | DOI |
|---|---|---|
| **v2.6** | 2026-11-10 | [10.5281/zenodo.24120357](https://doi.org/10.5281/zenodo.24120357) (latest version, also via the all-versions DOI) |
| v2.5 | 2026-11-10 | [10.5281/zenodo.24095000](https://doi.org/10.5281/zenodo.24095000) |
| v2.4 | 2026-11-09 | v2.4 |
| v2.3 | 2026-11-04 | v2.3 |
| v2.2 | 2026-11-04 | v2.2 |
| v2.1 | 2026-10-31 | v2.1 |
| v2.0 | 2026-10-28 | v2.0 |
| v1.1 | 2026-10-27 | Via the all-versions DOI |
| v1.0 | 2026-10-26 | Via the all-versions DOI |

## Abstract

DHIKRA QUAD SYSTEM AI is the public demonstration of the QUAD SYSTEM AI architecture (TR-2026-QUAD-0018, v2.6). It describes a verifiable ethical control layer placed between a human and an AI. The human enters the data and makes the decision, the AI proposes solutions, and the control layer filters, records, and can abstain. The AI may be a conventional AI; the control layer is independent of any particular AI.

The control layer relies on a validated rule-based inference core with three fundamental properties:

1. **Determinism.** With identical inputs, software version, configuration, and rule set, the core produces identical, reproducible outputs.
2. **Explicit abstention.** If the certainty score C(x) is below the threshold τ = 0.85, the system returns an explicit abstention message and provides no answer. This threshold is an uncalibrated design choice: it must be set from a risk-coverage analysis on a held-out labelled set. Abstention limits unjustified answers; it does not make the answers given correct.
3. **Sealed memory.** Validated entries are append-only and chained by a cryptographic hash (SHA-256). Any modification of an entry invalidates the following chain, which makes tampering detectable without guaranteeing confidentiality. Temporary session data is kept separately and deleted on request.

The core source code, full protocols, detailed formulas, exact inference rules, and internal documentation are confidential and unpublished. This repository provides only the public specification and the proof of dating.

This version claims no certification, regulatory approval, formal verification, or performance.

## Principle of operation

```
Human (keyboard)  →  AI proposes  →  Respect-Check  →  Human validates  →  Sealed memory
```

| Step | Actor | Role |
|---|---|---|
| 1 | Human | Enters the request and keeps the final decision. No action is taken without human intervention. |
| 2 | AI | Proposes a text, a plan, or execution instructions (quadrant Q2). |
| 3 | Respect-Check | Filters the proposal with a colour code: green, execution possible; orange, review required; red, blocked. |
| 4 | Human validation | The human approves or refuses. For a physical action, validation goes through the ILM tablet (element 3). |
| 5 | Sealed memory | The validated entry is recorded append-only, hash-chained, and sealed by DHIKRA SOURCE via the CCSS protocol. |

When the certainty score C(x) is below τ, the core abstains instead of answering.

## Operating modes

The control layer is identical in all modes. What changes is where the AI runs, and therefore which claims apply.

| Mode | Where the AI runs | Offline claim | Deterministic claim |
|---|---|---|---|
| A. Local AI | On the device, disconnected | Applies to the whole system | Control layer only |
| B. Institutional networked AI | On a closed institutional network (ILM tablet, restricted Wi-Fi) | Applies to the control layer; the AI is reachable only on the institutional network | Control layer only |
| C. Conventional online AI | At an external provider | Does not apply to the AI; the control layer itself stays offline | Control layer only |

Deterministic claims never apply to the AI's own outputs.

## The four quadrants

The quadrants are cross-cutting design axes, applied to the core and to every module, regardless of the number of modules.

| Quadrant | Axis | Role in the flow |
|---|---|---|
| Q1 | SOURCE | Values, intent, sealed memory, and the RAHMA (رحمة) cultural alignment protocol. Defines how the system works, which values it respects, and which memory it protects. It is the heart of the control layer. |
| Q2 | LOGIC | The language model, local or conventional, processes first the text, then the plan, then the execution instructions. Its outputs are validated by the MICAE protocol before being sealed. |
| Q3 | VISION | Predictive modelling of the real world using V-JEPA 2-type latent embeddings. Anticipates states t+1 to t+3 before any action. |
| Q4 | ACTION | Kinematic control of a robotic arm (Franka). Executed only after human validation and confirmation by a positive Respect-Check on the ILM tablet, per the CCSS protocol. No physical action is triggered without validation. |

Note: the learned components (Q2, Q3, Q4) are outside the deterministic claims of this document. Determinism is specified only for the rule-based core.

## The five elements

Every element uses the same control layer: the AI proposes, the system filters, the human decides.

| No. | Element | Description |
|---|---|---|
| 1 | DHIKRA SOURCE | Control layer and parent application. Rule-based deterministic core, sealed memory, Respect-Check protocol, explicit abstention. Verifiable decisions. Specifications published, core unpublished. |
| 2 | SAHA SCAN AI | Local reading of food labels, with a colour code (green, orange, red). When in doubt, the system answers "I don't know". Informational only; does not replace medical or nutritional advice. |
| 3 | ILM LIBERATION TABLET | Offline single-application tablet, with no phone chip and no audio function. Serves as the human validation station. Network access strictly limited to institutional Wi-Fi. Designed for closed institutional networks. Prototype reference: ILM-TABLET-2626-POC. |
| 4 | TAFSUT AI | Civil humanitarian drone. No offensive function. Onboard processing. Regulatory compliance required before any deployment. Technical specifications. |
| 5 | TUDERT YIWEN (formerly THUDERT 1) | Veterinary decision-support system in Kabyle, Arabic, and French. Does not replace a veterinarian. Requires field validation. Technical specifications. |

## Governance and validation

- **CCSS (Secure Control, Certification and Sealing).** Sealing by cryptographic fingerprints. Certification of action orders by the Respect-Check ethical filter and by human validators. Traceability of the orchestration core's decisions.
- **MICAE protocol.** A memory entry is considered valid only when the human, animal, and environmental validators agree. DHIKRA SOURCE then seals it.
- **Consent-based governance.** Decision by the local community. Municipal council approval is mandatory for any critical use. Cultural alignment ensured by SOURCE and the RAHMA protocol. Right of objection guaranteed before closing a memory site.
- **Respect-Check.** A colour-coded ethical control system that filters action orders and memory entries. Green: execution possible. Orange: review required. Red: blocked.

## Requirements

| Ref. | Requirement | Statement |
|---|---|---|
| REQ-1 | Determinism | Identical inputs, software version, configuration, and rule set produce identical outputs at the core level. |
| REQ-2 | Traceability | Every output records the identifiers of the rules applied, in execution order. |
| REQ-3 | Abstention | If the certainty score C(x) < τ, the system returns the explicit abstention message and no substantive answer. |
| REQ-4 | Sealed memory integrity | Validated entries are append-only and chained by a cryptographic hash. |
| REQ-5 | Session deletion | Temporary session data is deleted, and the deletion is verified, on request. |
| REQ-6 | Offline operation of the control layer | The control layer makes no outbound connection, except for the restricted institutional Wi-Fi of element 3. |
| REQ-7 | Human validation | No action order is executed without explicit human validation. |

## Limitations

- Determinism is specified only for the rule-based core, not for the AI's outputs.
- With a conventional online AI, the requests sent to it leave the device and are subject to the provider's terms.
- No formal verification has been performed.
- Security properties require an explicit threat model and independent testing.
- Regulatory compliance (civil drones, food and veterinary information) has not been assessed.
- No certification is claimed.
- Abstention and filtering reduce unjustified answers but do not guarantee the correctness of the answers given.

## License

> ### 🔴 $\color{red}{\textbf{CC BY-NC-ND 4.0 International}}$

**Texts and visuals:** [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/).

**Software, algorithms, weights, and unpublished documentation:** exclusive property, restricted access. Any reproduction, modification, distribution, commercial use, AI training, or reverse engineering requires the author's written authorization.

**Attribution:** QUAD SYSTEM AI © 2026 Yassa Yacine, TR-2026-QUAD-0018.

**Licensing requests:** dhikraemmortel@proton.me

## Proof of dating

- **Zenodo:** versions archived with a permanent DOI (see the versions table).
- **Timestamping:** OpenTimestamps, SHA-256 prefixes recorded.

## Changelog

| Version | Date | Change |
|---|---|---|
| v1.0 | 2026-10-26 | First publication |
| v1.1 | 2026-10-27 | Added CCSS documentation |
| v2.0 | 2026-10-28 | README structure and legal notices |
| v2.1 | 2026-10-31 | Presentation published without source code |
| v2.2 | 2026-11-04 | Interim update |
| v2.3 | 2026-11-04 | Full academic reorganisation |
| v2.4 | 2026-11-09 | Corrected public presentation |
| v2.5 | 2026-11-10 | Control-layer framing, principle of operation, operating modes, sole creator, CC BY-NC-ND 4.0 on Zenodo |
| **v2.6** | 2026-11-10 | **CC BY-NC-ND 4.0 made prominent in red; license corrected on Zenodo** |

## Citation

Yassa, Y. (2026). *DHIKRA QUAD SYSTEM AI: an ethical control layer between a human and an AI*, TR-2026-QUAD-0018, Version 2.6 [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.23671062

---

© 2026 Yassa Yacine · All rights reserved unless otherwise stated · ORCID · Zenodo
