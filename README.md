# Legibus Sovereign Legal Stack – NGI Fediversity 2025

This repository hosts the open-source deliverables of the **Legibus Fediverse Legal Stack**, a project funded under the NGI Fediversity program (Horizon Europe Cascade Funding).

The goal of this project is to provide **reproducible, privacy-compliant, and self-hostable infrastructure templates** for legal professionals and public institutions using open Fediverse tools like **Matrix** and **Nextcloud**.

---

## 📦 Project Structure

├── flake.nix # Declarative system config (optional Docker alternative available)
├── deploy/
│ ├── matrix.nix # NixOS module for Matrix (Synapse, Coturn)
│ ├── nextcloud.nix # NixOS module for Nextcloud (with Collabora optional)
│ └── config/
│ ├── users.nix
│ └── network.nix├── scripts/
│ └── deploy.sh # Shell-based fallback for quick start
├── docs/│ ├── user-guide.en.md
│ ├── user-guide.fr.md
│ ├── admin-checklist.pdf
│ └── rgpd-models/
│ ├── audit-log-policy.md
│ └── legal-retention.md
├── tests/
│ └── ci-regression.nix # Nix-based test suite for reproducibility
├── ci/
│ └── .gitlab-ci.yml # CI/CD pipeline with compliance tests
├── LICENSES/
│ ├── AGPL.txt
│ └── MIT.txt
└── CONTRIBUTING.md 

________________________________________
---

## 🧭 Who is this for?

- 🇪🇺 Legal professionals & bar associations
- 🏛️ Public administrations, municipalities, courts
- 🛡️ Digital rights NGOs & privacy-conscious organizations
- 🧑‍💻 System integrators for regulated sectors

---

## 📚 Outputs & Roadmap

This project delivers:
- ✅ NixOS modules and Docker-compatible templates
- ✅ Secure-by-default setups (TLS, E2EE, RBAC, GDPR logs)
- ✅ Admin & user guides (EN/FR)
- ✅ Compliance test cases (CI-ready)
- ✅ Upstream contributions to `nixpkgs` and NUR

> **Expected project duration:** Sept 2025 → March 2026  
> All outputs licensed under **AGPL v3**, **MIT**, or **CC BY-SA**

---

## 🤝 Community & Contributions

We welcome contributions, especially:
- Translations (FR/EN)
- Testing & deployment feedback
- Issue reporting for compliance or reproducibility

---

## 🔗 Related

- [Project site on NLnet](https://nlnet.nl/project/LegibusStack)
- [NGI Fediversity](https://nlnet.nl/fediversity)
- [Legibus.eu](https://legibus.eu)

---

## 💼 Legal & Funding Information

- PIC Number: **875203647**  
- Funded by the **European Union’s Horizon Europe Programme** under grant agreement via NGI Fediversity cascade scheme.  
- Incubated at **EuraTechnologies**, supported by **France 2030** and **Bpifrance**.
