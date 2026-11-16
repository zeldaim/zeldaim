# Hi, I'm Zen 👋

**Software Supply Chain Security · Detection Engineering** | Seoul, Korea

I work on two connected problems: knowing what is actually running (APIs, packages, their vulnerabilities),
and turning that knowledge into detections that are tested before they are trusted.

---

## 🔬 What I'm Working On

- **Software supply chain**
  - API-BOM (CycloneDX) and SBOM (Syft → Dependency-Track) for the same service, linked endpoint → code path → package → CVE
  - Reachability + VEX: of 403 unique CVEs, 309 (77%) were not reachable from any endpoint — after fixing 5 bugs in my own analyzer first
  - GitHub Actions that regenerate the SBOM / API-BOM on pull requests and on a daily schedule
  - Next: image signing (Cosign), provenance (SLSA), least-privilege CI
- **Detection engineering**
  - Wazuh rules generated from an approved OpenAPI allowlist, verified with `wazuh-logtest`
  - Found a deployed BOLA rule that worked backwards (blocked attempts alerted, successful enumeration missed) and fixed it
  - Response with Event-Driven Ansible: block → suspend → auto-release
- **Infrastructure**
  - Terraform (AWS, Azure), Docker, Kubernetes — preparing for CKA

---

## 🤝 Open Source

Reported to the official Wazuh repository:

- **[#35707](https://github.com/wazuh/wazuh/issues/35707)** — Sysmon EventID 13 reaches `archives.json` but no alert is generated (4.9.0 Docker)
  - Traced the difference in rule-chain processing between Security-channel and Sysmon-channel events
- **[#36029](https://github.com/wazuh/wazuh/issues/36029)** — Custom `if_sid` rules for `windows_eventchannel` stop firing in 4.9.0; `if_group` works as a workaround
  - Behavior change between 4.7.5 and 4.9.0, and `wazuh-logtest` output differing from the live `analysisd` pipeline

---

## 🛠 Selected Projects

| Project | What it shows |
|---|---|
| [multicloud-dr-petclinic](https://github.com/zeldaim/multicloud-dr-petclinic) | AWS → Azure DR (Site-to-Site VPN, DMS replication). Failover procedure re-verified locally: RTO 18.7 s, RPO 0 |
| [soc-detection-notes](https://github.com/zeldaim/soc-detection-notes) | Wazuh home SOC lab — MITRE-based rules (T1547, T1046) and SIEM incident write-ups |
| [wazuh-slack-alertbot](https://github.com/zeldaim/wazuh-slack-alertbot) | Wazuh → Slack alerting with Shannon / ApEn entropy for SSH brute-force |
| API security · supply chain | API-BOM / SBOM / VEX / reachability + rule generation (public release in preparation) |

---

## 📰 Writing

**[Signal & Threat](https://zeldaim.substack.com/)** — notes on software supply chain security, application security and detection.

---

*Not just finding vulnerabilities — understanding why they exist and making the fix verifiable.*
