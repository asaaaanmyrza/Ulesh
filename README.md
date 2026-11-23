# Ulesh
Ulesh connects restaurants with charitable organizations across Kazakhstan to help reduce food waste and get surplus food to people in need.
"Ulesh" (үлес) means "share" or "portion" in Kazakh.
Note: Ulesh is a student project created for the "Introduction to Open Source Development" course (DPG track). Features marked as planned are not yet implemented.

# Why Ulesh
Restaurants often have food that is still safe to eat but cannot be sold, while charitable organizations struggle to find reliable food sources. According to the FAO, roughly one third of food produced for human consumption is lost or wasted globally [TODO: add exact source link]. Ulesh makes it easier for both sides to find each other and coordinate donations.
Ulesh contributes to the UN Sustainable Development Goals:
* SDG 2 - Zero Hunger: surplus food reaches people who need it.
* SDG 12 - Responsible Consumption and Production (target 12.3): less food is wasted along the supply chain.
* SDG 17 - Partnerships for the Goals: the platform builds partnerships between businesses and non-profit organizations.
  
# How it works
1. Restaurant posts a donation. A verified restaurant publishes a listing: what food is available, quantity, expiry or "best before" time, pickup address and pickup window.
2. Charity claims it. A verified charitable organization browses nearby listings and sends a pickup request. The restaurant confirms it.
3. Pickup and distribution. The charity collects the food during the agreed window and distributes it. Both sides mark the donation as completed.
   
# Features
| Feature | Status | 
|----------|----------|
| Registration for restaurants and charities (with manual verification)   | MVP  |
| Create, edit and cancel donation listings    | MVP   |
| Browse listings and request pickup    | MVP   |
| Confirm / complete donations   | MVP   |
| Map view of nearby listings (OpenStreetMap)    | Planned   |
| Notifications (email)    | Planned   |
| Kazakh / Russian / English interface    | Planned   |
| Donation statistics (meals saved, weight)    | Planned  |

# Documentation
* [Code of Conduct](https://github.com/asaaaanmyrza/Ulesh/blob/main/CODE_OF_CONDUCT.md)
* [Privacy and Data Collection Plan](https://github.com/asaaaanmyrza/Ulesh/blob/main/PRIVACY.md)
* [Licence](https://github.com/asaaaanmyrza/Ulesh/blob/main/LICENSE)
* [Contribution](https://github.com/asaaaanmyrza/Ulesh/blob/main/CONTRIBUTING.md)
* [System Architecture](https://github.com/asaaaanmyrza/Ulesh/blob/main/docs/architecture.md)
* [User Guidelines](https://github.com/asaaaanmyrza/Ulesh/blob/main/docs/user-guide.md)

# Safety and Do No Harm
Food donation involves real health risks, so Ulesh is built around a few principles:

* Food safety first. Restaurants must only list food that is safe to eat, correctly stored, and within its expiry or best-before time. Responsibility for food quality stays with the donating restaurant, and listings must show handling and allergen information.
* Verified participants. Restaurants and charities are manually verified before they can post or claim donations.
* Non-discrimination. All verified charitable organizations have equal access to listings, regardless of size, location, or the beneficiaries they serve. Ulesh does not allow content or behavior that discriminates against people.
* Respectful community. All participants and contributors follow our Code of Conduct.

# Privacy and Data Security
Ulesh follows a data-minimization approach:
* What we collect: organization name, contact person, email, phone number, and pickup address. We do not collect data about the people who receive food.
* How we protect it: passwords are hashed, connections use HTTPS, access is role-based, and secrets are kept in environment variables, never in the repository.
* Retention and deletion: data is kept only as long as needed, and organizations can request deletion of their account and data at any time.
* Legal alignment: we aim to comply with the Law of the Republic of Kazakhstan on Personal Data and Their Protection.
* Self-hosting: each deployment is controlled by its operator, so data is not sent to third-party platforms.
To report a security issue, please email the maintainers (see Contact) instead of opening a public issue.

# Contributing
Contributions are welcome. Please read [CONTRIBUTING.md](https://github.com/asaaaanmyrza/Ulesh/blob/main/CONTRIBUTING.md) for how to report bugs, suggest features, and submit pull requests. By participating you agree to follow our Code of Conduct.

# License and Ownership
Ulesh is licensed under the MIT License.
Copyright (c) 2026 the Ulesh team. The project is owned and maintained by our student team:
* Assan Myrzakhmetov
* Zholdasbekova Aidana
* Talgatov Eldiyar
* Ayanbek Sultanbek
* Aisultan Suleimenov

# Contact
* Issues and feature requests: [GitHub Issues](https://github.com/asaaaanmyrza/Ulesh/issues)
