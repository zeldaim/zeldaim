# Hi, I'm Zen 👋

### Aspiring Open Source Security Engineer
**Software Supply Chain Security · DevSecOps · Detection Engineering**

I want to do more than use security tools.
I want to understand how they work, investigate security problems, fix what I find, and help make open-source software more secure.

My long-term goal is to become a security engineer who can identify vulnerabilities, understand their root causes, and design practical defensive systems.

---

## 🔬 What I'm Working On

- **Software Supply Chain Security**
  - API-BOM (CycloneDX) and SBOM (Syft → Dependency-Track) for the same service, linked endpoint → code path → package → CVE
  - Reachability + VEX: of 403 unique CVEs, 309 (77%) were not reachable from any endpoint (measured after fixing 5 bugs in my own analyzer)
  - GitHub Actions that regenerate the SBOM / API-BOM on pull requests and on a daily schedule
  - Next: blocking policy checks in CI, image signing (Cosign), provenance (SLSA)

- **Security Monitoring & Detection**
  - Wazuh rules generated from an approved OpenAPI allowlist and verified with `wazuh-logtest`
  - Found a deployed BOLA rule that worked backwards (blocked attempts alerted, successful enumeration missed) and fixed it
  - Entropy-based (Shannon / ApEn) SSH brute-force detection

- **Cloud & Infrastructure Security**
  - AWS, Azure, Linux, Kubernetes (preparing for CKA)
  - Terraform checked without a cloud account: `terraform test` with mock providers, Trivy misconfiguration scan

---

## 🤝 Open Source Security

I believe meaningful open-source contribution starts with understanding problems, not just submitting code.

Investigated and reported issues in the official Wazuh repository:

- **[#35707](https://github.com/wazuh/wazuh/issues/35707)** — Sysmon EventID 13 reaches `archives.json` but no alert is generated (4.9.0 Docker)
  - Traced the difference in rule-chain processing between Security-channel and Sysmon-channel events
- **[#36029](https://github.com/wazuh/wazuh/issues/36029)** — Custom `if_sid` rules for `windows_eventchannel` stop firing in 4.9.0; `if_group` works as a workaround
  - Behavior change between 4.7.5 and 4.9.0, and `wazuh-logtest` output differing from the live `analysisd` pipeline

I'm interested in contributing to the open-source security ecosystem, particularly **OpenSSF** projects, software supply chain security, and security automation.

---

## 🛠 Selected Projects

| Project | What it shows |
|---|---|
| [multicloud-dr-petclinic](https://github.com/zeldaim/multicloud-dr-petclinic) | AWS → Azure DR (Site-to-Site VPN, DMS replication). Failover procedure re-verified locally: RTO 18.7 s, RPO 0 |
| [soc-detection-notes](https://github.com/zeldaim/soc-detection-notes) | Wazuh home SOC lab — MITRE-based rules (T1547, T1046) and SIEM incident write-ups |
| [wazuh-slack-alertbot](https://github.com/zeldaim/wazuh-slack-alertbot) | Wazuh → Slack alerting with entropy-based SSH brute-force analysis |
| API security · supply chain | API-BOM / SBOM / VEX / reachability and automated Wazuh rule generation (public release in preparation) |

---

## 📰 Writing

**[Signal & Threat](https://zeldaim.substack.com/)**

Security research and technical analysis on software supply chain security, application security, and emerging threats.

---

## 🎯 My Direction

I want to contribute to open-source security projects, learn from experienced engineers, and help build safer software ecosystems.

**Not just finding vulnerabilities, but understanding why they exist and helping prevent them.**
