---
layout: home
title: Home
nav_order: 1
description: "AZ-305 Microsoft Azure Solutions Architect Expert — complete study notes covering all four exam domains with Mermaid diagrams, SKU comparisons, SLA tables, and exam caveats."
permalink: /
mermaid: true
---

# 📘 AZ-305 Study Notes
{: .no_toc }

**Microsoft Azure Solutions Architect Expert**
{: .fs-5 .fw-300 }

[Start Studying →](#-exam-overview){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View on GitHub](https://github.com/marcogrimaldi29/az-305-study-notes){: .btn .fs-5 .mb-4 .mb-md-0 target="_blank" }

---

> 🏠 These notes are maintained by **[Marco Grimaldi](https://www.linkedin.com/in/marco-grimaldi29/){:target="_blank"}** and based on the **[official Microsoft documentation](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/){:target="_blank"}**.
> Find more certification guides, study tips, and tech content at **[marcogrimaldi29.com](https://marcogrimaldi29.com){:target="_blank"}**.
> *Not affiliated with or endorsed by Microsoft. Always verify against the latest Microsoft documentation.*

---

## 🎯 Exam Overview

| Detail | Value |
|--------|-------|
| 🏅 Certification | **Microsoft Certified: Azure Solutions Architect Expert** |
| 📝 Passing Score | **700 / 1000** |
| 💶 Price (EU) | **~€126** *(varies by country, VAT may apply)* |
| ⏱️ Duration | **~120 minutes** |
| 🔁 Renewal | **Annual** — free online assessment on Microsoft Learn |
| 🛡️ Prerequisite | **AZ-104: Azure Administrator Associate** *(active cert required)* |

---

## 📊 Domain Weights

```mermaid
pie title AZ-305 — Official Exam Domain Weights
    "Design Infrastructure Solutions (30–35%)" : 32
    "Design Identity, Governance & Monitoring (25–30%)" : 25
    "Design Data Storage Solutions (25–30%)" : 25
    "Design Business Continuity Solutions (15–20%)" : 18
```

| # | Domain | Weight | Key Focus Areas |
|---|--------|--------|----------------|
| 1 | [Design Identity, Governance & Monitoring](./01-identity-governance-monitoring/) | **25–30%** | Entra ID, RBAC, PIM, Azure Policy, Monitor, Sentinel |
| 2 | [Design Data Storage Solutions](./02-data-storage-solutions/) | **25–30%** | Azure SQL, Cosmos DB, Blob, ADLS Gen2, Synapse |
| 3 | [Design Business Continuity Solutions](./03-business-continuity/) | **15–20%** | HA, DR, SLAs, Backup, ASR, geo-replication |
| 4 | [Design Infrastructure Solutions](./04-infrastructure-solutions/) | **30–35%** | Compute, Networking, Migrations, App Architecture |

---

## 🗂️ Notes Index

<div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap:1rem; margin: 1.5rem 0;">

<div style="border:1px solid #5f6368; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">📘 Prerequisites</h3>
<p>Core Azure architecture: regions, availability zones, VNets, compute, storage, and identity fundamentals.</p>
<a href="./00-azure-prerequisites/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #1a73e8; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🔐 Domain 1 — Identity & Governance</h3>
<p><strong>25–30%</strong> of exam. Entra ID, RBAC, PIM, Conditional Access, Azure Policy, Azure Monitor, Sentinel.</p>
<a href="./01-identity-governance-monitoring/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #1a73e8; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🗄️ Domain 2 — Data Storage</h3>
<p><strong>25–30%</strong> of exam. SQL family, Cosmos DB consistency, Blob tiers, ADLS Gen2, Synapse, ADF.</p>
<a href="./02-data-storage-solutions/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #34a853; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🔄 Domain 3 — Business Continuity</h3>
<p><strong>15–20%</strong> of exam. SLA math, HA patterns, Azure Backup, ASR, auto-failover groups.</p>
<a href="./03-business-continuity/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #ea4335; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🏗️ Domain 4 — Infrastructure</h3>
<p><strong>30–35%</strong> of exam — heaviest domain. Compute, networking, migrations, messaging, API Management.</p>
<a href="./04-infrastructure-solutions/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #f4b400; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🏛️ Well-Architected & CAF</h3>
<p>WAF 5 pillars (Reliability, Security, Cost, Ops, Performance) + Cloud Adoption Framework lifecycle.</p>
<a href="./05-well-architected-framework/" class="btn btn-outline fs-5">Read →</a>
</div>

<div style="border:1px solid #ab47bc; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">⚡ Quick Reference Cheatsheet</h3>
<p>Key numbers, SLA tables, decision matrices, EU pricing, exam traps, and pre-exam checklist.</p>
<a href="./06-quick-reference-cheatsheet/" class="btn btn-outline fs-5">Read →</a>
</div>
<div style="border:1px solid #0078d4; border-radius:8px; padding:1rem; background:#2d2f31;">
<h3 style="margin-top:0;">🏗️ Azure Architectures (AAC)</h3>
<p>Architecture choices by type (compute, messaging, routing, data, security) and compliance implications for financial services, healthcare, government, retail, energy, and manufacturing.</p>
<a href="./07-azure-architectures/" class="btn btn-outline fs-5">Read →</a>
</div>

</div>

---

## 🧠 How to Use These Notes

These notes are structured to follow the **official AZ-305 study guide** domain order. The recommended reading flow:

```mermaid
flowchart LR
    PRE["📘 Prerequisites\n(fundamentals)"]
    D1["🔐 Domain 1\nIdentity & Governance\n25–30%"]
    D2["🗄️ Domain 2\nData Storage\n25–30%"]
    D3["🔄 Domain 3\nBusiness Continuity\n15–20%"]
    D4["🏗️ Domain 4\nInfrastructure\n30–35%"]
    WAF["🏛️ WAF & CAF\n(cross-domain)"]
    SHEET["⚡ Cheatsheet\n(last-minute)"]
    ARCH["🏗️ AAC Appendix\n(architectures)"]

    PRE --> D1 --> D2 --> D3 --> D4 --> WAF --> SHEET --> ARCH
```

### 💡 Study Tips

- 🎯 The exam tests **"why this service?"** — think in trade-offs and constraints, not just definitions
- 💶 Know **SKU tier feature gates** — what's in Premium that Standard doesn't have often decides exam answers
- 📊 **SLA uptime percentages** appear regularly in scenario questions — the cheatsheet has a full table
- ⚠️ Each section has **`Exam Caveats`** callouts — these are high-frequency exam traps
- 🔄 Each domain ends with a **quick-reference scenario table** — great for final review

---

## 📚 Official Resources

| Resource | Link |
|----------|------|
| 🎓 Microsoft Certification Path | [AZ-305 Certification Path](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/){:target="_blank"} |
| 📋 Skills Measured Guide | [Official Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305){:target="_blank"} |
| 🧪 Free Practice Assessment | [Practice Test](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-305/practice/assessment?assessment-type=practice&assessmentId=15){:target="_blank"} |
| 🏗️ Architecture Center | [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/){:target="_blank"} |
| 💶 EU Exam Booking | [Pearson VUE Microsoft](https://home.pearsonvue.com/microsoft){:target="_blank"} |

---

## 🌐 Published Website

These notes are hosted on **GitHub Pages** and published as a searchable website on this URL:

👉 **[marcogrimaldi29/az-305-study-notes](https://marcogrimaldi29.com/az-305-study-notes/)**

The site includes full-text search, Mermaid diagram rendering, and mobile-friendly navigation for on-the-go review. 

These notes are designed to be a structured, exam-focused summary of the most important concepts and services baseds on the official [Microsoft Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305) and its criteria.

---

## ✍️ About the Author

These notes are maintained by **[Marco Grimaldi](https://www.linkedin.com/in/marco-grimaldi29/){:target="_blank"}** — Cloud Consultant, Language Trainer & Lifelong Learner.

📍 **Find more content at [marcogrimaldi29.com](https://marcogrimaldi29.com){:target="_blank"}**

> The website is continuously updated and based on my personal study notes and experiences. If you have any feedback, suggestions, or corrections, feel free to [reach out](https://marcogrimaldi29.com/contact/)!

---

## ©️ Credits & Acknowledgements

The [Just the Docs](https://github.com/just-the-docs/just-the-docs) theme is used for a clean, documentation-style layout that emphasizes readability and quick reference. Licensed under [MIT](https://opensource.org/license/MIT).

[Claude Sonnet 4.6](https://www.anthropic.com/news/claude-sonnet-4-6) was used for initial content generation and structuring, with all final edits, fact-checking, and formatting done by the author.

---
