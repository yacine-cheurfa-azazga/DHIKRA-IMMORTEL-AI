<div align="center">

# DHIKRA QUAD SYSTEM AI

### An ethical control layer between a human and an AI, with an offline deterministic kernel and explicit abstention

**Technical Report TR-2026-QUAD-0018 · Version 2.5 · Public Showcase**

[![Zenodo](https://img.shields.io/badge/Zenodo-v2.5-0057B8)](https://doi.org/10.5281/zenodo.23671062)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-C0392B)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0005--1982--7176-2E9E44)](https://orcid.org/0009-0005-1982-7176)

</div>

---

## Author

| | |
|---|---|
| **Author** | Yassa Yacine |
| **Affiliation** | Independent Researcher, QUAD SYSTEM AI Project |
| **ORCID** | [![ORCID](https://img.shields.io/badge/0009--0005--1982--7176-2E9E44)](https://orcid.org/0009-0005-1982-7176) |
| **License contact** | [dhikraemmortel@proton.me](mailto:dhikraemmortel@proton.me) |
| **Web address** | https://github.com/yacine-cheurfa-azazga/DHIKRA-IMMORTEL-AI |

## Zenodo Versions

All versions are archived on Zenodo. The all-versions DOI always resolves to the latest one.

[![All versions DOI](https://img.shields.io/badge/All%20versions%20DOI-10.5281%2Fzenodo.23671062-0057B8)](https://doi.org/10.5281/zenodo.23671062)

| Version | Date | DOI |
|---|---|---|
| **v2.5** | 2026-11-10 | Latest, via the all-versions DOI |
| v2.4 | 2026-11-09 | [![v2.4](https://img.shields.io/badge/10.5281%2Fzenodo.24092901-0057B8)](https://doi.org/10.5281/zenodo.24092901) |
| v2.3 | 2026-11-04 | [![v2.3](https://img.shields.io/badge/10.5281%2Fzenodo.23964487-0057B8)](https://doi.org/10.5281/zenodo.23964487) |
| v2.2 | 2026-11-04 | [![v2.2](https://img.shields.io/badge/10.5281%2Fzenodo.23944074-0057B8)](https://doi.org/10.5281/zenodo.23944074) |
| v2.1 | 2026-10-31 | [![v2.1](https://img.shields.io/badge/10.5281%2Fzenodo.23847692-0057B8)](https://doi.org/10.5281/zenodo.23847692) |
| v2.0 | 2026-10-28 | [![v2.0](https://img.shields.io/badge/10.5281%2Fzenodo.23717622-0057B8)](https://doi.org/10.5281/zenodo.23717622) |
| v1.1 | 2026-10-27 | Via the all-versions DOI |
| v1.0 | 2026-10-26 | Via the all-versions DOI |

## Abstract

DHIKRA QUAD SYSTEM AI is the public showcase of the QUAD SYSTEM AI architecture (TR-2026-QUAD-0018, v2.5). It describes an ethical, verifiable **control layer placed between a human and an AI**. The human types and decides, the AI proposes, and the control layer filters, records and may abstain. The AI can be a conventional AI; the control layer does not depend on any particular one.

The control layer rests on an inference kernel based on validated rules, with three core properties:

1. **Determinism.** Given identical inputs, software version, configuration and rule set, the kernel produces identical, reproducible results.
2. **Explicit abstention.** If the certainty score C(x) is below the threshold τ = 0.85, the system returns an explicit abstention message and no substantive answer. The threshold is an uncalibrated design choice: it must be set from a risk-coverage analysis on a held-out labelled set. Abstention limits unjustified answers; it does not make the answers given correct.
3. **Sealed memory.** Validated entries are append-only and chained by cryptographic hash (SHA-256). Any modification of an entry invalidates the subsequent chain, which allows tampering to be detected without guaranteeing confidentiality. Temporary session data is kept separately and purged on request.

The kernel source code, full protocols, detailed formulas, exact inference rules and internal documentation are confidential and unpublished. This repository provides only the public specification and the proof of dating.

> No certification, regulatory approval, formal verification or performance is claimed in this version.

## Principle of Operation

```
Human (keyboard)  →  AI proposes  →  Respect-Check  →  Human validates  →  Sealed memory
```

| Step | Actor | Role |
|---|---|---|
| 1 | **Human** | Types the request and keeps the final decision. Nothing is executed without the human. |
| 2 | **AI** | Proposes a text, a plan or execution instructions (quadrant Q2). |
| 3 | **Respect-Check** | Filters the proposal with a colour code: green, execution possible; orange, review required; red, blocked. |
| 4 | **Human validation** | The human approves or rejects. For physical action, validation goes through the ILM tablet (element No. 3). |
| 5 | **Sealed memory** | The validated entry is recorded append-only, hash-chained, and sealed by SOURCE DHIKRA through the CCSS protocol. |

When the certainty score C(x) is below τ, the kernel abstains instead of answering.

### Operating modes

The control layer is the same in every mode. What changes is where the AI runs, and therefore which claims apply.

| Mode | Where the AI runs | Offline claim | Determinism claim |
|---|---|---|---|
| **A. Local AI** | On the device, disconnected | Applies to the whole system | Control layer only |
| **B. Institutional-network AI** | On a closed institutional network (ILM tablet, restricted Wi-Fi) | Applies to the control layer; the AI is reached only on the institutional network | Control layer only |
| **C. Conventional online AI** | At an external provider | Does not apply to the AI; the control layer itself stays offline | Control layer only |

The determinism claims never cover the AI's own outputs.

## The Four Quadrants

The quadrants are cross-cutting design axes, applied to the kernel and to each module, independently of the number of modules.

| Quadrant | Axis | Role in the flow |
|---|---|---|
| **Q1** | SOURCE | Values, intent, sealed memory and the RAHMA (رحمة) cultural alignment protocol. Defines why the system acts, which values it respects and which memory it protects. It is the core of the control layer. |
| **Q2** | LOGIC | The language model, local or conventional. Handles text, then the plan, then execution instructions. Its outputs are validated by the MICAE approach before they are sealed. |
| **Q3** | VISION | Predictive modelling of the real world with V-JEPA 2-type latent embeddings. Anticipates states from t+1 to t+3, before any action. |
| **Q4** | ACTION | Kinematic control of a robotic arm (Franka). Executes only after a green Respect-Check and human validation on the ILM tablet, sealed via the CCSS protocol. No physical action without validation. |

*Note: the learned components (Q2, Q3, Q4) fall outside the scope of the deterministic claims of this document. Determinism is specified only for the rule-based kernel.*

## The Five Elements

Each element uses the same control layer: the AI proposes, the system filters, the human decides.

| No. | Element | Description |
|---|---|---|
| 1 | **SOURCE DHIKRA** | Control layer and parent application. Rule-based deterministic kernel, sealed memory, Respect-Check protocol, explicit abstention. Verifiable decisions. Specifications published, kernel unpublished. |
| 2 | **SAHA SCAN AI** | Local reading of food labels, with a three-colour classification (green, orange, red). When uncertain, the system answers "I don't know". For information only; does not replace medical or nutritional advice. |
| 3 | **ILM LIBERATION TABLET** | Offline single-application tablet, with no phone chip and no sound. It is the human validation station. Network access strictly limited to institutional Wi-Fi. Designed for closed institutional networks. POC reference: ILM-TABLET-2626-POC. |
| 4 | **TAFSUT AI** | Civil humanitarian drone. No offensive function. On-board processing. Regulatory compliance required before any deployment. Design specification. |
| 5 | **TUDERT YIWEN** (formerly THUDERT 1) | Veterinary decision support in Kabyle, Arabic and French. Does not replace a veterinarian. Requires field validation. Design specification. |

## Governance and Validation

- **CCSS (Secure Control, Certification and Sealing).** Sealing by cryptographic fingerprints. Certification of action orders by the Respect-Check ethical filter and by human validators. Traceability of the orchestration kernel's decisions.
- **MICAE protocol.** A memory entry is considered valid only when the human, animal and environmental validators agree. SOURCE DHIKRA then seals it.
- **Governance by consent.** Local community decision. Municipal council approval is mandatory for any critical use. Cultural harmonisation ensured by SOURCE and the RAHMA protocol. Right of objection guaranteed before a place of memory is sealed.
- **Respect-Check.** Colour-coded ethical control that filters action orders and memory entries. Green: execution possible. Orange: review required. Red: blocked.

## Requirements

| Ref. | Requirement | Statement |
|---|---|---|
| REQ-1 | Determinism | Identical inputs, software version, configuration and rule set produce identical results from the kernel. |
| REQ-2 | Traceability | Each result records the identifiers of the rules applied, in their order of execution. |
| REQ-3 | Abstention | If the certainty score C(x) < τ, the system returns the explicit abstention message and no substantive answer. |
| REQ-4 | Sealed memory integrity | Validated entries are append-only and chained by cryptographic hash. |
| REQ-5 | Session deletion | Temporary session data is deleted, and the deletion verified, on request. |
| REQ-6 | Offline operation of the control layer | The control layer makes no outbound connection, apart from the restricted institutional Wi-Fi of element No. 3. |
| REQ-7 | Human validation | No action order is executed without explicit human validation. |

## Limitations

- Determinism is specified only for the rule-based kernel, not for the outputs of the AI.
- With a conventional online AI, the requests sent to it leave the device and are subject to that provider's own terms.
- No formal verification has been performed.
- The security properties require an explicit threat model and independent testing.
- Regulatory compliance (civil drone, food and veterinary information) has not been assessed.
- No certification is claimed.
- Abstention and filtering reduce unjustified answers, but do not guarantee the correctness of the answers provided.

## License

[![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-C0392B)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

- **Texts and visuals:** Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0).
- **Software, algorithms, weights and unpublished documentation:** proprietary and closed. Any reproduction, modification, distribution, commercial use, AI training or reverse engineering requires written authorisation from the author.

**Attribution:** QUAD SYSTEM AI © 2026 Yassa Yacine, TR-2026-QUAD-0018.

**License requests:** [dhikraemmortel@proton.me](mailto:dhikraemmortel@proton.me)

## Proof of Dating

- **Zenodo:** versions archived with a permanent DOI (see the versions table).
- **Timestamping:** OpenTimestamps, SHA-256 prefixes recorded.

## Changelog

| Version | Date | Change |
|---|---|---|
| v1.0 | 2026-10-26 | First public release |
| v1.1 | 2026-10-27 | Added CCSS documentation |
| v2.0 | 2026-10-28 | README structure and copyright notices |
| v2.1 | 2026-10-31 | Showcase published without source code |
| v2.2 | 2026-11-04 | Intermediate update |
| v2.3 | 2026-11-04 | Complete academic reorganisation |
| v2.4 | 2026-11-09 | Corrected public showcase |
| v2.5 | 2026-11-10 | Control-layer framing, principle of operation, operating modes, single creator, CC BY-NC-ND 4.0 on Zenodo |

## Citation

> Yassa, Y. (2026). *DHIKRA QUAD SYSTEM AI: An ethical control layer between a human and an AI, TR-2026-QUAD-0018, Version 2.5* [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.23671062

---

<div align="center">

© 2026 Yassa Yacine · All rights reserved unless otherwise stated · [ORCID](https://orcid.org/0009-0005-1982-7176) · [Zenodo](https://doi.org/10.5281/zenodo.23671062)

</div>
