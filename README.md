<div align="center">

# DHIKRA QUAD SYSTEM AI

### Offline deterministic inference kernel with explicit abstention

**Technical Report TR-2026-QUAD-0018 · Version 2.4 · Public Showcase**

[![Zenodo](https://img.shields.io/badge/Zenodo-v2.4-0057B8)](https://doi.org/10.5281/zenodo.24092901)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-C0392B)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0005--1982--7176-2E9E44)](https://orcid.org/0009-0005-1982-7176)

[Version française](README.fr.md)

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
| **v2.4** | 2026-11-09 | [![v2.4](https://img.shields.io/badge/10.5281%2Fzenodo.24092901-0057B8)](https://doi.org/10.5281/zenodo.24092901) |
| v2.3 | 2026-11-04 | [![v2.3](https://img.shields.io/badge/10.5281%2Fzenodo.23964487-0057B8)](https://doi.org/10.5281/zenodo.23964487) |
| v2.2 | 2026-11-04 | [![v2.2](https://img.shields.io/badge/10.5281%2Fzenodo.23944074-0057B8)](https://doi.org/10.5281/zenodo.23944074) |
| v2.1 | 2026-10-31 | [![v2.1](https://img.shields.io/badge/10.5281%2Fzenodo.23847692-0057B8)](https://doi.org/10.5281/zenodo.23847692) |
| v2.0 | 2026-10-28 | [![v2.0](https://img.shields.io/badge/10.5281%2Fzenodo.23717622-0057B8)](https://doi.org/10.5281/zenodo.23717622) |
| v1.1 | 2026-10-27 | Via the all-versions DOI |
| v1.0 | 2026-10-26 | Via the all-versions DOI |

## Abstract

DHIKRA QUAD SYSTEM AI is the public showcase of the QUAD SYSTEM AI architecture (TR-2026-QUAD-0018, v2.4). It describes an ethical, deterministic, offline artificial intelligence system designed to operate in a disconnected local environment, with no cloud dependency and no online learning.

The system relies on an inference kernel based on validated rules, with three core properties:

1. **Determinism.** Given identical inputs, software version, configuration and rule set, the system produces identical, reproducible results.
2. **Explicit abstention.** If the certainty score C(x) is below the threshold τ = 0.85, the system returns an explicit abstention message and no substantive answer. The threshold τ = 0.85 is an uncalibrated design choice: it must be set from a risk-coverage analysis on a held-out labelled set. Abstention limits unjustified answers; it does not make the answers given correct.
3. **Sealed memory.** Validated entries are append-only and chained by cryptographic hash. Any modification of an entry invalidates the subsequent chain, which allows tampering to be detected without guaranteeing confidentiality. Temporary session data is kept separately and purged on request.

The kernel source code, full protocols, detailed formulas, exact inference rules and internal documentation are confidential and unpublished. This repository provides only the public specification and the proof of dating.

> No certification, regulatory approval, formal verification or performance is claimed in this version.

## The Four Quadrants

The quadrants are cross-cutting design axes, applied to the kernel and to each module, independently of the number of modules.

| Quadrant | Axis | Description |
|---|---|---|
| **Q1** | SOURCE | Values, intent, sealed memory and the RAHMA (رحمة) cultural alignment protocol. Defines why the system acts, which values it respects and which memory it protects. |
| **Q2** | LOGIC | Local, offline language model. Handles text, then the plan, then execution instructions. Validated by the MICAE approach. Operates without an Internet connection. |
| **Q3** | VISION | Predictive modelling of the real world with V-JEPA 2-type latent embeddings. Anticipation of states from t+1 to t+3, before any action. |
| **Q4** | ACTION | Kinematic control of a robotic arm (Franka). Execution is subordinate to ILM tablet validations and sealed via the CCSS protocol. No physical action without validation. |

*Note: the learned components (Q2, Q3, Q4) fall outside the scope of the deterministic claims of this document. Determinism is specified only for the rule-based kernel.*

## The Five Elements

| No. | Element | Description |
|---|---|---|
| 1 | **SOURCE DHIKRA** | Kernel, parent application. Offline deterministic inference, sealed memory, Respect-Check protocol. No cloud dependency, no online learning, verifiable decisions. Specifications published, kernel unpublished. |
| 2 | **SAHA SCAN AI** | Local reading of food labels. Offline analysis with a three-colour classification (Green, Orange, Red). When uncertain, the system answers "I don't know". For information only; does not replace medical or nutritional advice. |
| 3 | **ILM LIBERATION TABLET** | Offline single-application tablet, with no phone chip and no sound. Network access strictly limited to institutional Wi-Fi. Designed for closed institutional networks. POC reference: ILM-TABLET-2626-POC. |
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
| REQ-1 | Determinism | Identical inputs, software version, configuration and rule set produce identical results. |
| REQ-2 | Traceability | Each result records the identifiers of the rules applied, in their order of execution. |
| REQ-3 | Abstention | If the certainty score C(x) < τ, the system returns the explicit abstention message and no substantive answer. |
| REQ-4 | Sealed memory integrity | Validated entries are append-only and chained by cryptographic hash. |
| REQ-5 | Session deletion | Temporary session data is deleted, and the deletion verified, on request. |
| REQ-6 | Offline operation | No outbound connection during operation, apart from the restricted institutional Wi-Fi of Element No. 3. |

## Limitations

- Determinism is specified only for the rule-based kernel.
- No formal verification has been performed.
- The security properties require an explicit threat model and independent testing.
- Regulatory compliance (civil drone, food and veterinary information) has not been assessed.
- No certification is claimed.
- Abstention reduces unjustified answers, but does not guarantee the correctness of the answers provided.

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

## Citation

> Yassa, Y. (2026). *DHIKRA QUAD SYSTEM AI: Offline deterministic inference kernel with explicit abstention, TR-2026-QUAD-0018, Version 2.4* [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.24092901

---

<div align="center">

© 2026 Yassa Yacine · All rights reserved unless otherwise stated · [ORCID](https://orcid.org/0009-0005-1982-7176) · [Zenodo](https://doi.org/10.5281/zenodo.23671062)

</div>

<div align="center">

# DHIKRA QUAD SYSTEM AI

### Noyau d'inférence déterministe hors ligne avec abstention explicite

**Rapport technique TR-2026-QUAD-0018 · Version 2.4 · Vitrine publique**

[![Zenodo](https://img.shields.io/badge/Zenodo-v2.4-0057B8)](https://doi.org/10.5281/zenodo.24092901)
[![Licence](https://img.shields.io/badge/Licence-CC%20BY--NC--ND%204.0-C0392B)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.fr)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0005--1982--7176-2E9E44)](https://orcid.org/0009-0005-1982-7176)

[English version](README.md)

</div>

---

## Auteur

| | |
|---|---|
| **Auteur** | Yassa Yacine |
| **Affiliation** | Chercheur indépendant, projet QUAD SYSTEM AI |
| **ORCID** | [![ORCID](https://img.shields.io/badge/0009--0005--1982--7176-2E9E44)](https://orcid.org/0009-0005-1982-7176) |
| **Contact (licence)** | [dhikraemmortel@proton.me](mailto:dhikraemmortel@proton.me) |
| **Adresse web** | https://github.com/yacine-cheurfa-azazga/DHIKRA-IMMORTEL-AI |

## Versions Zenodo

Toutes les versions sont archivées sur Zenodo. Le DOI de toutes les versions renvoie toujours vers la plus récente.

[![DOI de toutes les versions](https://img.shields.io/badge/DOI%20toutes%20versions-10.5281%2Fzenodo.23671062-0057B8)](https://doi.org/10.5281/zenodo.23671062)

| Version | Date | DOI |
|---|---|---|
| **v2.4** | 2026-11-09 | [![v2.4](https://img.shields.io/badge/10.5281%2Fzenodo.24092901-0057B8)](https://doi.org/10.5281/zenodo.24092901) |
| v2.3 | 2026-11-04 | [![v2.3](https://img.shields.io/badge/10.5281%2Fzenodo.23964487-0057B8)](https://doi.org/10.5281/zenodo.23964487) |
| v2.2 | 2026-11-04 | [![v2.2](https://img.shields.io/badge/10.5281%2Fzenodo.23944074-0057B8)](https://doi.org/10.5281/zenodo.23944074) |
| v2.1 | 2026-10-31 | [![v2.1](https://img.shields.io/badge/10.5281%2Fzenodo.23847692-0057B8)](https://doi.org/10.5281/zenodo.23847692) |
| v2.0 | 2026-10-28 | [![v2.0](https://img.shields.io/badge/10.5281%2Fzenodo.23717622-0057B8)](https://doi.org/10.5281/zenodo.23717622) |
| v1.1 | 2026-10-27 | Via le DOI de toutes les versions |
| v1.0 | 2026-10-26 | Via le DOI de toutes les versions |

## Résumé

DHIKRA QUAD SYSTEM AI est la vitrine publique de l'architecture QUAD SYSTEM AI (TR-2026-QUAD-0018, v2.4). Elle décrit un système d'intelligence artificielle éthique, déterministe et hors ligne, conçu pour fonctionner en environnement local déconnecté, sans dépendance au cloud et sans apprentissage en ligne.

Le système repose sur un noyau d'inférence basé sur des règles validées, avec trois propriétés centrales :

1. **Déterminisme.** À entrées, version logicielle, configuration et ensemble de règles identiques, le système produit des résultats identiques et reproductibles.
2. **Abstention explicite.** Si le score de certitude C(x) est inférieur au seuil τ = 0,85, le système renvoie un message d'abstention explicite et aucune réponse substantielle. Le seuil τ = 0,85 est un choix de conception non calibré : il doit être défini à partir d'une analyse de couverture des risques sur un ensemble étiqueté mis de côté. L'abstention limite les réponses non justifiées ; elle ne rend pas les réponses données correctes.
3. **Mémoire scellée.** Les entrées validées sont en mode ajout uniquement (*append-only*) et chaînées par hachage cryptographique. Toute modification d'une entrée invalide la chaîne ultérieure, ce qui permet de détecter les falsifications sans garantir la confidentialité. Les données de session temporaires sont conservées séparément et purgées sur demande.

Le code source du noyau, les protocoles complets, les formules détaillées, les règles d'inférence exactes et la documentation interne sont confidentiels et non publiés. Ce dépôt fournit uniquement la spécification publique et la preuve de datation.

> Aucune certification, aucune approbation réglementaire, aucune vérification formelle et aucune performance ne sont revendiquées dans cette version.

## Les quatre quadrants

Les quadrants sont des axes de conception transversaux, appliqués au noyau et à chaque module, indépendamment du nombre de modules.

| Quadrant | Axe | Description |
|---|---|---|
| **Q1** | SOURCE | Valeurs, intention, mémoire scellée et protocole d'alignement culturel RAHMA (رحمة). Définit pourquoi le système agit, quelles valeurs il respecte et quelle mémoire il protège. |
| **Q2** | LOGIQUE | Modèle de langage local et hors ligne. Gère le texte, puis le plan, puis les instructions d'exécution. Validé par l'approche MICAE. Fonctionne sans connexion Internet. |
| **Q3** | VISION | Modélisation prédictive du monde réel avec des plongements latents de type V-JEPA 2. Anticipation des états de t+1 à t+3, avant toute action. |
| **Q4** | ACTION | Pilotage cinématique d'un bras robotique (Franka). Exécution subordonnée aux validations de la tablette ILM et scellée via le protocole CCSS. Aucune action physique sans validation. |

*Note : les composantes apprises (Q2, Q3, Q4) sortent du périmètre des affirmations déterministes de ce document. Le déterminisme est spécifié uniquement pour le noyau basé sur des règles.*

## Les cinq éléments

| N° | Élément | Description |
|---|---|---|
| 1 | **SOURCE DHIKRA** | Noyau, application mère. Inférence déterministe hors ligne, mémoire scellée, protocole Respect-Check. Aucune dépendance au cloud, pas d'apprentissage en ligne, décisions vérifiables. Spécifications publiées, noyau non publié. |
| 2 | **SAHA SCAN AI** | Lecture locale des étiquettes alimentaires. Analyse hors ligne, classification tricolore (Vert, Orange, Rouge). En cas d'incertitude, le système renvoie « Je ne sais pas ». À titre informatif seulement ; ne remplace pas un avis médical ou nutritionnel. |
| 3 | **ILM LIBÉRATION TABLET** | Tablette hors ligne mono-application, sans puce téléphonique, sans son. Accès réseau strictement limité au Wi-Fi institutionnel. Conçue pour les réseaux institutionnels fermés. Référence POC : ILM-TABLET-2626-POC. |
| 4 | **TAFSUT AI** | Drone humanitaire civil. Aucune fonction offensive. Traitement embarqué. Conformité réglementaire requise avant tout déploiement. Spécification de conception. |
| 5 | **TUDERT YIWEN** (ex-THUDERT 1) | Aide à la décision vétérinaire en kabyle, en arabe et en français. Ne remplace pas un vétérinaire. Nécessite une validation sur le terrain. Spécification de conception. |

## Gouvernance et validation

- **CCSS (Contrôle, Certification et Scellage Sécurisé).** Scellage par empreintes cryptographiques. Certification des ordres d'action par le filtre éthique Respect-Check et par des validateurs humains. Traçabilité des décisions du noyau d'orchestration.
- **Protocole MICAE.** Une entrée de mémoire n'est considérée comme valide que lorsque les validateurs humains, animaux et environnementaux sont d'accord. SOURCE DHIKRA la scelle ensuite.
- **Gouvernance par le consentement.** Décision communautaire locale. Accord du conseil municipal obligatoire pour toute utilisation critique. Harmonisation culturelle assurée par SOURCE et le protocole RAHMA. Droit d'opposition garanti avant la mise sous scellés d'un lieu de mémoire.
- **Respect-Check.** Contrôle éthique à code couleur pour filtrer les ordres d'action et les entrées de mémoire. Vert : exécution possible. Orange : examen requis. Rouge : blocage.

## Exigences

| Réf. | Exigence | Énoncé |
|---|---|---|
| REQ-1 | Déterminisme | Des entrées, une version logicielle, une configuration et un ensemble de règles identiques produisent des résultats identiques. |
| REQ-2 | Traçabilité | Chaque résultat enregistre les identifiants des règles appliquées, dans leur ordre d'exécution. |
| REQ-3 | Abstention | Si le score de certitude C(x) < τ, le système renvoie le message d'abstention explicite et aucune réponse substantielle. |
| REQ-4 | Intégrité de la mémoire scellée | Les entrées validées sont en mode ajout uniquement et chaînées par hachage cryptographique. |
| REQ-5 | Suppression de session | Les données de session temporaires sont supprimées et vérifiées sur demande. |
| REQ-6 | Fonctionnement hors ligne | Aucune connexion sortante pendant le fonctionnement, hors cadre Wi-Fi institutionnel restreint de l'élément N°3. |

## Limites

- Le déterminisme est spécifié uniquement pour le noyau basé sur des règles.
- Aucune vérification formelle n'a été effectuée.
- Les propriétés de sécurité nécessitent un modèle de menaces explicite et des tests indépendants.
- La conformité réglementaire (drone civil, information alimentaire et vétérinaire) n'a pas été évaluée.
- Aucune certification n'est revendiquée.
- L'abstention réduit les réponses non justifiées, mais ne garantit pas la justesse des réponses fournies.

## Licence

[![Licence](https://img.shields.io/badge/Licence-CC%20BY--NC--ND%204.0-C0392B)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.fr)

- **Textes et visuels :** Creative Commons Attribution - Pas d'Utilisation Commerciale - Pas de Modification 4.0 International (CC BY-NC-ND 4.0).
- **Logiciel, algorithmes, poids et documentation non publiée :** propriétaires et fermés. Toute reproduction, modification, distribution, usage commercial, entraînement d'IA ou ingénierie inverse exige une autorisation écrite de l'auteur.

**Attribution :** QUAD SYSTEM AI © 2026 Yassa Yacine, TR-2026-QUAD-0018.

**Demandes de licence :** [dhikraemmortel@proton.me](mailto:dhikraemmortel@proton.me)

## Preuve de datation

- **Zenodo :** versions archivées avec DOI permanent (voir le tableau des versions).
- **Horodatage :** OpenTimestamps, préfixes SHA-256 enregistrés.

## Historique

| Version | Date | Modification |
|---|---|---|
| v1.0 | 2026-10-26 | Première publication publique |
| v1.1 | 2026-10-27 | Ajout de la documentation CCSS |
| v2.0 | 2026-10-28 | Structuration du README et mentions de copyright |
| v2.1 | 2026-10-31 | Publication de la vitrine sans code source |
| v2.2 | 2026-11-04 | Mise à jour intermédiaire |
| v2.3 | 2026-11-04 | Réorganisation académique complète |
| v2.4 | 2026-11-09 | Vitrine publique corrigée |

## Citation

> Yassa, Y. (2026). *DHIKRA QUAD SYSTEM AI : noyau d'inférence déterministe hors ligne avec abstention explicite, TR-2026-QUAD-0018, version 2.4* [Logiciel]. Zenodo. https://doi.org/10.5281/zenodo.24092901

---

<div align="center">

© 2026 Yassa Yacine · Tous droits réservés sauf mention contraire · [ORCID](https://orcid.org/0009-0005-1982-7176) · [Zenodo](https://doi.org/10.5281/zenodo.23671062)

</div>
