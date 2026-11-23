# The Final DPG Application "Ulesh"

**SIS №12**, Introduction to Open Source

Kazakh-British Technical University,
School of Information Technology and Engineering.
Almaty, 2026.

## Prepared by
- Suleimenov A. A.
- Talgatov E.
- Ayanbek S.
- Myrzakhmetov A.
- Zholdasbekova A.

**Checked by:** Gerassimov M. G., Lecturer SITE (MScE)

## Contents
1. [Introduction](#introduction)
2. [Evidence map](#evidence-map)
3. [Assessment by criterion](#assessment-by-criterion)

## Introduction
Restaurants and cafés in Kazakhstan regularly throw away food that is
still safe to eat at the end of the day, while charities, shelters and
food banks struggle to source enough food for the people they serve. The
two sides rarely have a simple, trusted way to coordinate quickly.

Ulesh (Kazakh: "sharing") is designed as a free, open-source web
application that any organisation can host itself. Restaurants post
surplus food listings with quantity, pickup window and safe-until time;
verified charities see nearby listings, claim them and confirm pickup.
An administrator verifies organisations and monitors for misuse.

The project is currently at the concept stage. This self-assessment
evaluates the repository's governance, documentation and design
artefacts against the DPG criteria; it does not claim that the
application is already deployed or that the described features are
implemented.

All the references are presented in Table 1.

**Table 1. Basic information**

| Field | Value |
|---|---|
| Project | Ulesh — open-source, self-hosted platform connecting restaurants and charity organisations in Kazakhstan to reduce food waste |
| Repository | https://github.com/asaaaanmyrza/Ulesh |
| Branch assessed | `main` |
| Project stage | Concept (documentation, architecture and governance complete; application features in design) |
| Team | Suleimenov A., Talgatov E., Ayanbek S., Myrzakhmetov A., Zholdasbekova A. |
| Course / assignment | Introduction to Open Source, SIS №12 |
| Date | 23.11.2026 |

## Evidence map
Table 2 shows the evidence for each DPG criterion: each criterion is
justified by one or more project documents.

**Table 2. Evidence map**

| № | DPG criterion | Evidence in repository | Status |
|---|---|---|---|
| 1 | Relevant to SDGs | [README.md](../README.md) | Meets |
| 2 | Open-source licence | [LICENSE](../LICENSE) | Meets |
| 3 | Clear ownership | [README.md](../README.md) | Meets |
| 4 | Platform independence | [docs/architecture.md](architecture.md) | Meets (by design) |
| 5 | Documentation | [README.md](../README.md), [docs/user-guide.md](user-guide.md), [CONTRIBUTING.md](../CONTRIBUTING.md) | Meets |
| 6 | Non-discrimination & Do No Harm | [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md), [docs/safety-principles.md](safety-principles.md) | Meets |
| 7 | Privacy & data security | [PRIVACY.md](../PRIVACY.md) | Meets (by design) |

## Assessment by criterion

### 1. Relevant to the Sustainable Development Goals
The README.md section **Why Ulesh** names the problem directly:
restaurants often have food that is still safe to eat but cannot be
sold, while charitable organisations struggle to find reliable food
sources. It links Ulesh to three SDGs: SDG 2 (Zero Hunger), because
surplus food reaches people in need; SDG 12 (Responsible Consumption and
Production), specifically Target 12.3 on halving food waste and reducing
losses along supply chains; and SDG 17 (Partnerships for the Goals),
because the platform builds partnerships between businesses and
non-profit organisations.

The **How it works** section shows how the planned three-step workflow
(a restaurant posts a donation, a charity claims it, both sides confirm
pickup and distribution) delivers on these goals in Kazakhstan. The
README cites the FAO estimate that about one third of food produced for
human consumption is lost or wasted globally as context for the
problem's scale.

### 2. Use of an approved open-source licence
Ulesh is released under the MIT License, an OSI-approved open-source
licence. The full text is in the LICENSE file at the root of the `main`
branch, and the README.md section **License and Ownership** states the
licence explicitly.

CONTRIBUTING.md adds an inbound-licensing rule: by contributing, every
contributor agrees that their contributions are licensed under the same
MIT License. This keeps the whole repository under one permissive
licence, so anyone may use, study, modify, redistribute or self-host
Ulesh free of charge.

### 3. Clear ownership
The README.md section **License and Ownership** states "Copyright (c)
2026 the Ulesh team" and names the five students who own and maintain
the project: Assan Myrzakhmetov, Zholdasbekova Aidana, Talgatov Eldiyar,
Ayanbek Sultanbek and Aisultan Suleimenov. The README also states the
project's origin: it is a student project for the "Introduction to Open
Source Development" course (DPG track).

The repository is hosted at github.com/asaaaanmyrza/Ulesh, with all five
team members as collaborators. The README **Contact** section points to
GitHub Issues as the public channel for issues and feature requests.
Because the code is MIT-licensed, the team's ownership does not restrict
reuse: any organisation may fork the project and run its own instance.

### 4. Platform independence
docs/architecture.md sets out a modular architecture built entirely on
open-source technologies: a Vue.js frontend, a FastAPI (Python) backend
and an SQLite database for the initial stage, with PostgreSQL named as a
possible future option. None of these components requires a proprietary
licence, a paid cloud service or a specific vendor.

Section 6 **Platform Independence** lists the design principles that
prevent vendor lock-in: open technologies, separated frontend, backend
and data layers, portable data storage, replaceable external services,
and open communication standards. Section 7 notes that hosting
infrastructure has not been finalised; the README **Self-hosting**
principle states that each deployment is controlled by its operator, so
a charity network or municipality can run Ulesh on infrastructure it
chooses.

### 5. Documentation
The README.md explains the project's purpose, the SDGs it serves, the
planned workflow, a feature table that marks which features belong to
the MVP scope and which are planned for later, and its safety, privacy,
licensing and ownership principles. docs/user-guide.md walks through the
intended scenarios for both user groups: restaurants (create an account,
publish a food offer, review requests, confirm a donation) and
charitable organisations (create an account, browse food, submit a
request, receive confirmation, collect the food).

docs/architecture.md documents the technology stack, the main system
components, a nine-step data flow and the deployment strategy.
CONTRIBUTING.md defines the contribution workflow: Issue, branch from
`main` (no direct commits to `main`), commit, Pull Request linked to the
Issue, review by another team member, and merge after approval. Every
document clearly states that Ulesh is at the concept stage and that the
scenarios it describes are planned, not implemented.

### 6. Non-discrimination and Do No Harm
CODE_OF_CONDUCT.md commits the project to a safe, inclusive and
respectful environment. It requires fair treatment regardless of
background, nationality, religion, gender, disability or other personal
characteristics, and prohibits harassment, discrimination, publishing
private information, fraud and exploitation. Its **Non-Discrimination
and Fair Access** section requires participation decisions to rest on
legitimate operational and safety requirements. The README and
architecture.md (§5.3) add that all verified charities get equal access
to listings regardless of their size, location or the beneficiaries they
serve.

Because food redistribution carries real health risks, the Code of
Conduct includes a dedicated **Food Safety and Do No Harm** section:
food must not be offered if it is expired, contaminated, improperly
stored or otherwise unsafe; restaurants must give accurate information
on food type, quantity, expiry date, storage and allergens; receiving
organisations may inspect and reject donations; and unsafe listings must
be reported and reviewed. Manual verification of every restaurant and
charity (README, architecture.md §5.2) is designed to reduce misuse. The
Code of Conduct states openly that Ulesh is a coordination platform, not
a food-inspection authority, and that platform-level moderation will be
designed before deployment.

### 7. Privacy and applicable laws; data security
PRIVACY.md is a preliminary data-protection plan built on data
minimisation. It lists the limited data the future platform may process
(organisation name and type, contact details of an authorised
representative, business e-mail and phone, pickup location, listing and
request details, basic security logs) and excludes sensitive data such
as health records or national ID numbers unless a lawful, justified need
is established. The README adds that no data is collected about the
people who receive food, and PRIVACY.md commits that personal data will
never be sold to advertisers or unrelated third parties.

The plan defines role-based access, so that restaurants, charities and
administrators see only what they need, and lists planned security
measures: HTTPS, strong password hashing, role-based access control,
restricted database access, secure credential management, backups and
logging. It also states the project's aim to comply with the legislation
of the Republic of Kazakhstan, including the Law on Personal Data and
Their Protection, and sets out the steps required before going live:
defined retention periods, data access and deletion requests, lawful
grounds and consent, incident response, and a privacy contact. The
document says plainly that these controls are not yet implemented or
audited, and that open-source code never means open access to personal
data.
