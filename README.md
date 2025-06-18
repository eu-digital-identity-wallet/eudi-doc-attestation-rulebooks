# EUDI Wallet – Attestation Rulebooks Catalog

This repository contains the official **attestation rulebooks** used in the European Digital Identity (EUDI) Wallet framework. These rulebooks define the structure, semantics, and validation requirements for **Electronic Attestations of Attributes (EAAs)** that are issued to and used within EUDI Wallets, as mandated by Regulation (EU) No 910/2014 (eIDAS) and the related Implementing Regulations.

## 📘 What is an Attestation Rulebook?

An attestation rulebook provides a **technical and policy specification** for a particular set of attributes or credential type issued as an EAA. It serves as a reference for:

* Attestation providers (issuers)
* EUDI Wallet providers
* Wallet-relying parties (verifiers)
* Conformity Assessment Body and auditors


Each rulebook includes schema definitions, trust and assurance requirements, and procedures for issuance, validation, and revocation.

## 📁 Repository Structure

```
eudi-doc-attestation-rulebooks/
│
├── rulebooks/
│   ├── <usecase1>
│       ├── rulebook-<usecase1>.md
│   ├── <usecase2>
│       ├── rulebook-<usecase2>.md
│   └── ...
│
└── template/
    └── attestation-rulebook-template.md
```

* `rulebooks/`: Contains finalized or draft rulebooks for specific use cases (e.g., driving license, educational credentials, social security).
* `template/`: Contains the official **template** to be used for drafting new rulebooks.

## 📄 Rulebook Template

The `attestation-rulebook-template.md` defines the standard structure that all rulebooks must follow. Key sections include:

* item 1
* item 2
* item 3

This template aligns with the requirements outlined in Implementing Regulation (EU) 2024/2977 and its annexes.

## ✅ Contributing Rulebooks

To propose a new rulebook:

1. Copy the template from `template/attestation-rulebook-template.md`.
2. Fill in all required sections with valid and justifiable content.
3. Submit your rulebook via a pull request under the `rulebooks/` directory.
4. Make sure to align with relevant standards listed in the [Architecture and Reference Framework](https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/architecture-and-reference-framework-main/)

## 📚 References

* [eIDAS Regulation (EU) No 910/2014](https://eur-lex.europa.eu/eli/reg/2014/910/oj)
* [CIR 2024/2977](https://data.europa.eu/eli/reg_impl/2024/2977/oj)
regarding PID and EAA,
* [CIR 2024/2979](https://data.europa.eu/eli/reg_impl/2024/2979/oj)
regarding integrity and core functionalities,
* [CIR 2024/2980](https://data.europa.eu/eli/reg_impl/2024/2980/oj)
regarding ecosystem notifications,
* [CIR 2024/2981](https://data.europa.eu/eli/reg_impl/2024/2981/oj)
regarding certification of Wallet Solutions,
* [CIR 2024/2982](https://data.europa.eu/eli/reg_impl/2024/2982/oj)
regarding protocols and interfaces,
* [CIR 2025/846](https://data.europa.eu/eli/reg_impl/2025/846/oj)
regarding cross border identity matching,
* [CIR 2025/847](https://data.europa.eu/eli/reg_impl/2025/847/oj)
regarding security breaches of European Digital Identity Wallets,
* [CIR 2025/848](https://data.europa.eu/eli/reg_impl/2025/848/oj)
regarding registration of Wallet Relying Parties,
* [CIR 2025/849](https://data.europa.eu/eli/reg_impl/2025/849/oj)
regarding the list of certified European Digital Identity Wallets.
* [EUDI Architecture and Reference Framework](https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/architecture-and-reference-framework-main/)

## 📬 Contact

For feedback or questions, please reach out via GitHub Issues or contact the EUDI Wallet support team via the [official portal](https://ec.europa.eu/digital-identity).
