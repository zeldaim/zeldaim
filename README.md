<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF6B6B,25:FFD93D,50:6BCB77,75:4D96FF,100:9B5DE5&height=210&section=header&text=Hi,%20I'm%20Zen%20👋&fontColor=ffffff&fontSize=60&fontAlignY=36&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3000&pause=800&color=4D96FF&center=true&vCenter=true&width=820&lines=Software+Supply+Chain+Security+%F0%9F%94%97;Detection+Engineering+%F0%9F%9B%A1%EF%B8%8F;Aspiring+Open+Source+Security+Engineer+%F0%9F%8C%B1;Not+just+finding+bugs+%E2%80%94+making+fixes+verifiable" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-Supply%20Chain%20Security-FF6B6B?style=flat-square" />
  <img src="https://img.shields.io/badge/Focus-Detection%20Engineering-FFB703?style=flat-square" />
  <img src="https://img.shields.io/badge/Interest-OpenSSF-6BCB77?style=flat-square" />
  <img src="https://img.shields.io/badge/Seoul-Korea-4D96FF?style=flat-square" />
</p>

---

### 🌈 About me

> 🔍 I don't stop at running security tools — I **check whether their results are right**.<br>
> 🧪 My own analyzers and rules get **tested before I trust them**.<br>
> 📝 I record **what failed** as carefully as what worked.<br>
> 🔧 Career switcher into security, with a **hardware** background (KAIST IDEC · 831 h of semiconductor design courses).

---

### 🎯 What I'm Working On

| | Area | What I actually did |
|:-:|---|---|
| 🔗 | **Software supply chain** | API-BOM (CycloneDX) + SBOM (Syft → Dependency-Track) linked endpoint → code path → package → CVE. **309 of 403 CVEs (77%) unreachable** from any endpoint — measured after fixing 5 bugs in my own analyzer |
| 🛡️ | **Detection engineering** | Wazuh rules generated from an approved OpenAPI allowlist, verified with `wazuh-logtest`. Found and fixed a deployed BOLA rule that **worked backwards** |
| ☁️ | **Infrastructure security** | Terraform checked without a cloud account (`terraform test` + mocks, Trivy, Checkov). Replaced an `AdministratorAccess` role with split **least-privilege** roles and an IAM action checker |
| 🧬 | **Next: software → kernel correlation dashboard** | One view linking API endpoint → process → **libraries actually loaded at runtime (strace · eBPF)** → SBOM package → CVE → kernel. Today the kernel-layer graph is a static sketch; the goal is to replace its edges with runtime evidence |
| 📘 | **Study → apply** | [openssf-study](https://github.com/zeldaim/openssf-study) — each OpenSSF concept applied to my own project and verified before / after (first: least privilege) |

---

### 🤝 Open Source

<p>
  <a href="https://github.com/wazuh/wazuh/issues/35707"><img src="https://img.shields.io/badge/wazuh%2Fwazuh-%2335707-3595F9?style=for-the-badge" /></a>
  <a href="https://github.com/wazuh/wazuh/issues/36029"><img src="https://img.shields.io/badge/wazuh%2Fwazuh-%2336029-9B5DE5?style=for-the-badge" /></a>
</p>

- **#35707** — Sysmon EventID 13 reaches `archives.json` but no alert fires (4.9.0) → traced the rule-chain difference between Security- and Sysmon-channel events
- **#36029** — Custom `if_sid` rules for `windows_eventchannel` stop firing in 4.9.0 (`if_group` works) → behavior change since 4.7.5, and `wazuh-logtest` differing from live `analysisd`

---

### 🧰 Tech Stack

**🔗 Supply chain**&nbsp; <img src="https://img.shields.io/badge/CycloneDX%20%C2%B7%20VEX-FF6B6B?style=for-the-badge" /> <img src="https://img.shields.io/badge/Syft%20%C2%B7%20Grype-FF8E72?style=for-the-badge" /> <img src="https://img.shields.io/badge/Dependency--Track-FFA94D?style=for-the-badge" /> <img src="https://img.shields.io/badge/Trivy%20%C2%B7%20Checkov-1904DA?style=for-the-badge&logo=trivy&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" /><br>
**🛡️ Detection**&nbsp; <img src="https://img.shields.io/badge/Wazuh-3595F9?style=for-the-badge" /> <img src="https://img.shields.io/badge/Event--Driven%20Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white" /><br>
**☁️ Infra**&nbsp; <img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" /> <img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge" /> <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" /> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />

---

### 🗂️ Projects

| | Project | Highlight |
|:-:|---|---|
| ☁️ | **[Multi-Cloud DR — AWS → Azure](https://github.com/zeldaim/multicloud-dr-petclinic)** | Site-to-Site VPN · DMS · Route 53 / CloudFront failover (team). Re-verified locally: <img src="https://img.shields.io/badge/RTO-18.7s-6BCB77?style=flat-square" /> <img src="https://img.shields.io/badge/RPO-0-4D96FF?style=flat-square" /> <img src="https://img.shields.io/badge/terraform%20test-8%2F8-9B5DE5?style=flat-square" /> |
| 🔗 | **API Security · Supply Chain** | API-BOM / SBOM / VEX / reachability + automated Wazuh rules (team final project) <img src="https://img.shields.io/badge/release-in%20preparation-FFB703?style=flat-square" /> |
| 🛡️ | **[SOC Detection Notes](https://github.com/zeldaim/soc-detection-notes)** | Wazuh home SOC lab — MITRE rules (T1547, T1046) and SIEM incident write-ups |
| 🔔 | **[ZenSOC — Wazuh → Slack](https://github.com/zeldaim/wazuh-slack-alertbot)** | Grouping cut duplicate alerts <img src="https://img.shields.io/badge/32%E2%86%923-FF6B6B?style=flat-square" />; the entropy hypothesis came out the opposite way — recorded as such |

---

### 🔧 Hardware Background

| | |
|:-:|---|
| 🧩 | **KAIST IDEC semiconductor design training** — 67 courses · 831 h (2024.04 – 2026.03): digital design (Verilog, RTL-to-GDSII), computer architecture, AI accelerators, embedded networks (CAN · FlexRay) |
| 📟 | **Embedded systems coursework** — in progress |

---

### 📜 Certifications

**RHCSA** · **AWS Advanced Networking – Specialty** · **AWS Data Engineer – Associate** · **AWS AI Practitioner** · **정보처리기사** · CKA *(in progress)*

---

### 📰 Writing & Contact

<p>
  <a href="https://zeldaim.substack.com/"><img src="https://img.shields.io/badge/Substack-Signal%20%26%20Threat-FF6719?style=for-the-badge&logo=substack&logoColor=white" /></a>
  <a href="https://github.com/zeldaim"><img src="https://img.shields.io/badge/GitHub-zeldaim-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:9B5DE5,25:4D96FF,50:6BCB77,75:FFD93D,100:FF6B6B&height=120&section=footer" />
</p>
