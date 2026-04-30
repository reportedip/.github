# ReportedIP

**Open Threat Intelligence for a Safer Internet — made in Germany.**

[reportedip.de](https://reportedip.de) · [Check an IP](https://reportedip.de) · [API & Docs](https://reportedip.de) · contact: `1@reportedip.de`

---

ReportedIP is an open IP threat intelligence platform. It collects, scores and shares IP reputation data so sysadmins, security teams and hosting providers can block bad actors **before** they cause damage. The platform is fed by honeypot networks, automated sensors and the wider community — every report is cross-referenced, weighted and made available through a public REST API, live feed and an attack map.

All systems are hosted and operated in Germany, fully GDPR-compliant.

## What we build

| Repository | What it is | Stack | License |
|---|---|---|---|
| [**reportedip-blacklist**](https://github.com/reportedip/reportedip-blacklist) | Community-driven IP threat intelligence feed with curated and dynamic blacklists, updated daily. Plain-text, JSON, CSV and firewall-ready configs (nginx / Apache / iptables). | Shell | CC BY 4.0 |
| [**reportedip-hive**](https://github.com/reportedip/reportedip-hive) | Community-powered WordPress security plugin — 12 attack sensors, a complete 2FA suite (TOTP, WebAuthn/FIDO2, Email, SMS), progressive blocks and opt-in herd-immunity threat sharing. | PHP | GPL-2.0-or-later |
| [**honeypot-server**](https://github.com/reportedip/honeypot-server) | Standalone PHP honeypot that emulates WordPress, Drupal and Joomla. 36 threat analyzers feed detections directly into the ReportedIP API. | PHP | BSL 1.1 → Apache-2.0 (2030) |

## How it works

1. **Collect** — Honeypots, network sensors and community members worldwide report suspicious IP addresses (failed logins, comment spam, XML-RPC abuse, port scanning, …).
2. **Score** — Every report is cross-checked and fed into the reputation engine. The confidence score (0–100) factors in report volume, source diversity, threat severity, recency and whether honeypots were involved. Old reports decay over time.
3. **Protect** — Query the API to check any IP, set up automatic blocking based on confidence thresholds, pull curated blacklists for your firewall, or use the Hive plugin to protect WordPress without writing a line of code.

30 distinct threat categories are tracked — from brute-force and spam to malware, DDoS, fraud, infrastructure abuse and APT activity.

## Get involved

- **Run a honeypot** — every instance contributes attack data and makes everyone safer. Request a free Community Access Key at `1@reportedip.de`.
- **Protect your WordPress site** with [Hive](https://github.com/reportedip/reportedip-hive) and feed back attacks into the network.
- **Pull the blacklist** for your firewall, SIEM or reverse proxy from [reportedip-blacklist](https://github.com/reportedip/reportedip-blacklist).
- **Report false positives or malicious IPs** to `abuse@reportedip.de`.

Bug reports, feature requests and pull requests are welcome on every repository.

## Patronage & team

ReportedIP runs under the patronage of **Patrick Schlesinger** ([LinkedIn](https://www.linkedin.com/in/contex/)), who initiated the project. It is built and maintained by the team at **CMS ADMINS**, a German infrastructure company with years of experience in server administration, web hosting and IT security. Development happens in the open and the platform evolves based on real feedback from the people who use it.

## Privacy & compliance

- 100% German infrastructure
- Fully GDPR-compliant (Art. 6(1)(f) lawful basis documented in-product for Hive)
- Privacy-minimal logging, anonymisation and short retention windows
- No personal data exposed in public feeds — only IP reputation

---

© 2025–2026 ReportedIP / Patrick Schlesinger. Code is released under the license listed in each repository.
