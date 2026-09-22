# Summary: Supply Chain Attacks — Most Notable Incidents of 2025
### (Kaspersky Report)

---

## Introduction

- Supply chain attacks remain one of the most dangerous types of information security incidents.
- Their popularity among cybercriminals is not declining but continues to grow.
- This article covers the most unusual and attention-grabbing supply chain attacks of 2025 — not always the largest in damage, but definitely the most notable.

---

## January 2025: RAT in DogWifTools GitHub Repository

- Cybercriminals trojanized several versions of **DogWifTools** — a tool for launching and promoting Solana memecoins on Pump.fun.
- Attackers compromised the private GitHub repository, waited for developers to upload a new version, added a **RAT**, and replaced the legitimate program with their own version a couple of hours later.
- Windows versions **1.6.3 to 1.6.6** were trojanized.
- Attackers emptied victims' crypto wallets — over **$10 million** stolen (attackers denied the figure but didn't specify their actual haul).

---

## February 2025: Vubit Crypto Exchange Hack — $1.5 Billion

- The **largest crypto robbery in history**.
- Attackers compromised the **Safe(Wallet)** cold multi-signature wallet software used by the exchange.
- Employees signed a malicious smart contract that transferred all contents of a cold wallet to hundreds of attacker wallets.
- **400,000+ ETH and stETH** stolen — worth about **$1.5 billion**.

---

## March 2025: Coinbase Attack Attempt via GitHub Actions

- A complex attack using a **cascading compromise** of GitHub Actions.
- Attackers compromised the **tj-actions/changed-files** workflow and modified it to run a malicious Python script.
- The script searched for secrets: **AWS, Azure, Google Cloud keys, GitHub PAT and NPM tokens, database accounts, RSA private keys**, etc.
- All found data was written to **publicly accessible build logs** — anyone could access the leaked data.
- Initial target was a repository belonging to **Coinbase**.

---

## April 2025: Backdoor in 21 Magento Extensions

- A backdoor was found in **21 Magento modules** developed by three vendors: **Tigren, Meetanshi, and MGS**.
- These extensions were used by **several hundred e-commerce organizations**, including at least one multinational company.
- The backdoor was embedded back in **2019** but activated in **April 2025**.
- Attackers compromised websites and uploaded **web shells** via a function that ran arbitrary code from a license file.
- Ironically, infected modules included **MGS GDPR** and **Meetanshi Cookie** (security/privacy-related extensions).

---

## May 2025: Ransomware via Compromised MSP

- **DragonForce** ransomware group gained access to an unnamed **MSP's infrastructure**.
- Used it to steal client data and spread ransomware.
- Exploited several vulnerabilities (including one critical) in **SimpleHelp** remote monitoring tool.
- Vulnerabilities were discovered in **2024**, disclosed and fixed in **January 2025** — but the MSP **did not install updates in time**.

---

## June 2025: Backdoor in 17 Popular npm Packages

- Attackers hacked a **gluestack** library maintainer's account and used their token to add backdoors to **17 npm packages**.
- Most popular package: **@react-native-aria/interactions** — 125,000 weekly downloads.
- All compromised packages together: **over 1 million downloads**.
- After the incident, gluestack developers:
  - Restricted GitHub access for secondary contributors
  - Enabled **2FA** for publishing new versions
  - Promised secure development practices (pull request workflow, code review, audit logs)
- Before the incident, the project had none of these protections.

---

## July 2025: npm Packages Infected via Phishing

- Attackers targeted npm packages, including the popular **"is"** package — **2.7 million weekly downloads**.
- Successful **phishing attack** on a project owner using **typosquatting** (npmjs.com instead of npmjs.com) and a clone of the official npm site.
- Used the compromised account to publish malicious versions with a **backdoor**.
- Infection remained **unnoticed for 6 hours**.
- Same phishing attack was used on other developers; attackers may have saved some credentials for future attacks.

---

## August 2025: s1ngularity Attack — Secrets Leaked from Hundreds of Developers

- Attackers compromised **Nx** — a popular build system and CI/CD pipeline tool.
- Malicious code searched for: **crypto wallet keys, npm and GitHub tokens, SSH keys, API keys**, etc.
- Used **locally installed AI tools** (Claude Code, Gemini CLI, Amazon Q) to find secrets.
- All found data was published in public GitHub repositories named **s1ngularity-repository**, **s1ngularity-repository-0**, **s1ngularity-repository-1** — hence the attack name.
- Confidential data of hundreds of developers became accessible to **anyone**.

---

## September 2025: Crypto Stealer in npm Packages — 2.6 Billion Weekly Downloads

- New phishing campaign targeted JavaScript developers.
- Malicious code embedded in **a couple dozen popular projects**, including **chalk** and **debug**.
- Total infected packages: **2.6+ billion weekly downloads** at the time of compromise.
- Payload: **crypto stealer** — intercepted crypto transactions and redirected them to attackers' wallets.
- Attackers **botched the final stage** — only managed to steal **$925**.
- A week later: **first wave of Shai-Hulud** — self-propagating malware infected ~150 npm packages, including **Crowdstrike** projects.

---

## October 2025: GlassWorm Worm in Visual Studio Code

- **GlassWorm** — self-propagating malware infecting VS Code extensions in **Open VSX Registry** and **Microsoft Extension Marketplace**.
- Targets: **GitHub, Git, npm, Open VSX accounts**, and crypto wallet keys.
- Unusual C2 setup:
  - **Primary C2**: crypto wallet on **Solana blockchain**
  - **Backup channel**: **Google Calendar**
- Also downloaded a RAT called **Zombi** — full control over infected systems.

---

## November 2025: IndonesianFoods — 150,000 Spam Packages in npm

- Coordinated malicious campaign **IndonesianFoods** spammed npm with tens of thousands of useless packages.
- Goal: **inflate metrics and earn tokens** in the **tea.xyz** blockchain (rewards open-source developers).
- Created dependency structures with names like **"name + Indonesian dish"** (e.g., zul-tapai9-kyuki, andi-rendang23-breki).
- **No account compromise**; **no malicious payload** — except a script creating new packages every 7 seconds.
- Demonstrated npm's vulnerability to **large-scale spam campaigns**.

---

## December 2025: Shai-Hulud 2.0 — 400,000 Developer Secrets Leaked

- **Most important event of the year** in supply chain attacks (and likely all of infosec).
- **Shai-Hulud** (aka Sha1-Hulud) — self-propagating worm that:
  - Searches for secrets and publishes them in public GitHub repositories
  - **Self-propagates** by infecting projects controlled by already-infected developers
- **First wave**: September — several hundred npm packages infected.
- **Second wave (Shai-Hulud 2.0)**: added **wiper functionality** — if no valid npm or GitHub tokens found, it **erased user files**.
- **~400,000 secrets leaked** — all in public repositories accessible to anyone.
- **First confirmed attack using leaked secrets**: **Trust Wallet** — attackers uploaded a malicious Chrome extension with a **crypto drainer** on Christmas Eve, stealing **$8.5 million** from several thousand users.
- Consequences likely to be felt for a **long time**.

---

## How to Protect Against Supply Chain Attacks

- 2025 had **so many large-scale attacks** that not all fit in this review.
- 2026 promises to be **no less intense**.

**Key recommendations:**

1. **Carefully evaluate vendors** and check the code you use in your projects.
2. **Implement contractual security requirements.**
3. **Develop an incident response plan.**
4. **Monitor suspicious activity** in corporate infrastructure using **XDR** solutions.
5. **Use external threat hunting services** if internal infosec resources are insufficient.

---

## Key Themes Across 2025

| Theme | Details |
|-------|---------|
| **npm ecosystem** | Most targeted — DogWifTools, gluestack, "is", chalk, debug, Shai-Hulud, IndonesianFoods |
| **Crypto theft** | DogWifTools ($10M), Vubit ($1.5B), Trust Wallet ($8.5M) |
| **Self-propagating worms** | Shai-Hulud, Shai-Hulud 2.0, GlassWorm |
| **AI tools abused** | Claude Code, Gemini CLI, Amazon Q used to find secrets (s1ngularity) |
| **Unusual C2** | Solana blockchain + Google Calendar (GlassWorm) |
| **Public leaks** | s1ngularity and Shai-Hulud published secrets in public GitHub repos |
| **Delayed patching** | MSP ignored SimpleHelp vulnerabilities for months |
| **Spam campaigns** | IndonesianFoods — 150,000 packages |

---

## Final Takeaway

Supply chain attacks in 2025 were **relentless, creative, and devastating**. Attackers targeted every link in the chain — from GitHub repositories and npm packages to CI/CD tools and crypto wallets. The most dangerous trend was **self-propagating malware** (Shai-Hulud, GlassWorm) that spreads automatically using stolen credentials. Organizations must adopt **layered defenses** — vendor assessment, contractual security, incident response plans, XDR monitoring, and external threat hunting — because **no single measure is enough**.



======================================================

# Supply Chain Attacks — Summary in Tree Form
*(Based on the whiteboard photo)*

---

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  Retailer "Target" was compromised through the account of                   │
│  their air-conditioners supplier                                            │
└─────────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│              DEFENCE MEASURES AGAINST SUPPLY CHAIN ATTACKS                  │
└─────────────────────────────────────────────────────────────────────────────┘
                                    │
        ┌───────────────┬───────────┴───────────┬───────────────────┐
        │               │                       │                   │
        ▼               ▼                       ▼                   ▼
┌───────────────┐ ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────────┐
│  To Evaluate  │ │ Technological   │ │ To Implement    │ │ Develop an          │
│  Suppliers    │ │ Preventive      │ │ Contractual     │ │ Incident Response   │
│               │ │ Measures        │ │ Security        │ │ Plan                │
├───────────────┤ ├─────────────────┤ ├─────────────────┤ ├─────────────────────┤
│ → IS Policies │ │ → Least         │ │ → Audits        │ │ → Detection         │
│               │ │   Privileges    │ │                 │ │                     │
│ → Compliance  │ │                 │ │ → Incident      │ │ → Containment of    │
│               │ │ → Browser       │ │   Notification  │ │   attacks/incidents │
│               │ │   Isolation     │ │                 │ │                     │
│               │ │                 │ │ → Risk          │ │                     │
│               │ │ → Zero Trust    │ │   Management    │ │                     │
│               │ │                 │ │                 │ │                     │
│               │ │ → Build Mature  │ │                 │ │                     │
│               │ │   Account       │ │                 │ │                     │
│               │ │   Management    │ │                 │ │                     │
│               │ │                 │ │                 │ │                     │
│               │ │ → Malware       │ │                 │ │                     │
│               │ │   Prevention    │ │                 │ │                     │
│               │ │                 │ │                 │ │                     │
│               │ │ → Shadow IT     │ │                 │ │                     │
└───────────────┘ └─────────────────┘ └─────────────────┘ └─────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  Organize Monitoring                        Build Cooperation with          │
│                                             Security Suppliers              │
├─────────────────────────────────────────────┼───────────────────────────────┤
│ → XDR                                       │ → Work Closely                │
│                                             │                               │
│ → MDR                                       │ → Mutual Trust                │
│                                             │                               │
│                                             │ → Patch Management            │
└─────────────────────────────────────────────┴───────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  Organization                                                               │
├─────────────────────────────────────────────────────────────────────────────┤
│ → Training                                                                  │
│ → Finances (Reliability)                                                    │
│ → Access Control                                                            │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Simplified Tree (Text Version)

```
Supply Chain Attacks — Defence Measures
│
├── 1. Evaluate Suppliers
│   ├── IS Policies
│   └── Compliance
│
├── 2. Technological Preventive Measures
│   ├── Least Privileges
│   ├── Browser Isolation
│   ├── Zero Trust
│   ├── Build Mature Account Management
│   ├── Malware Prevention
│   └── Shadow IT
│
├── 3. Contractual Security
│   ├── Audits
│   ├── Incident Notification
│   └── Risk Management
│
├── 4. Incident Response Plan
│   ├── Detection
│   └── Containment of Attacks/Incidents
│
├── 5. Organize Monitoring
│   ├── XDR
│   └── MDR
│
├── 6. Build Cooperation with Security Suppliers
│   ├── Work Closely
│   ├── Mutual Trust
│   └── Patch Management
│
└── 7. Organization
    ├── Training
    ├── Finances (Reliability)
    └── Access Control
```

---

## Summary Table

| Branch | Key Measures |
|--------|-------------|
| **Evaluate Suppliers** | IS Policies, Compliance |
| **Technological Preventive Measures** | Least Privileges, Browser Isolation, Zero Trust, Mature Account Management, Malware Prevention, Shadow IT |
| **Contractual Security** | Audits, Incident Notification, Risk Management |
| **Incident Response Plan** | Detection, Containment |
| **Monitoring** | XDR, MDR |
| **Cooperation with Suppliers** | Work Closely, Mutual Trust, Patch Management |
| **Organization** | Training, Finances (Reliability), Access Control |

---

## Key Incident (From Whiteboard)

> **Retailer Target** was compromised through the account of their **air-conditioners supplier**.

This real-world example illustrates exactly why supply chain attacks are so dangerous — attackers don't need to breach the target directly; they just need to compromise **one trusted vendor** with access.




================================================================

# Supply chain across 2025 


# Supply Chain Attacks — Most Notable Incidents of 2025
### (Kaspersky Report) — Tree Form

---

## Root Incident


CHEETSHEEET to Learn Supply Chain  Attack 

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  SUPPLY CHAIN ATTACKS — 2025                                                │
│  (Most Notable Incidents)                                                   │
│  Source: Kaspersky                                                          │
└─────────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│  Supply chain attacks remain one of the most dangerous types of infosec     │
│  incidents. Their popularity among cybercriminals continues to grow.        │
└─────────────────────────────────────────────────────────────────────────────┘
                                    │
        ┌───────────────────────────┼───────────────────────────┐
        │                           │                           │
        ▼                           ▼                           ▼
   MONTHLY INCIDENTS           KEY THEMES                 DEFENSE MEASURES
   (Jan–Dec 2025)              (Across 2025)              (Recommendations)
```

---

## Monthly Incidents Tree

```
SUPPLY CHAIN ATTACKS — 2025
│
├── JANUARY 2025: RAT in DogWifTools GitHub Repository
│   ├── Tool: DogWifTools — launches/promotes Solana memecoins on Pump.fun
│   ├── Attack: Compromised private GitHub repo; waited for new version;
│   │         added RAT; replaced legitimate program
│   ├── Affected: Windows versions 1.6.3 to 1.6.6
│   └── Impact: $10M+ stolen from crypto wallets
│
├── FEBRUARY 2025: Vubit Crypto Exchange Hack — $1.5 Billion
│   ├── Largest crypto robbery in history
│   ├── Attack: Compromised Safe(Wallet) cold multi-signature wallet software
│   ├── Method: Employees signed malicious smart contract; transferred funds
│   └── Impact: 400,000+ ETH and stETH stolen — ~$1.5 billion
│
├── MARCH 2025: Coinbase Attack Attempt via GitHub Actions
│   ├── Attack: Cascading compromise of GitHub Actions
│   ├── Method: Compromised tj-actions/changed-files workflow;
│   │         ran malicious Python script searching for secrets
│   ├── Secrets targeted: AWS, Azure, Google Cloud keys,
│   │                     GitHub PAT, NPM tokens, DB accounts, RSA keys
│   ├── Leak: All data written to publicly accessible build logs
│   └── Target: Repository belonging to Coinbase
│
├── APRIL 2025: Backdoor in 21 Magento Extensions
│   ├── Vendors: Tigren, Meetanshi, MGS
│   ├── Affected: 21 Magento modules; several hundred e-commerce orgs
│   ├── Backdoor embedded: 2019 — activated: April 2025
│   ├── Method: Arbitrary code from license file → web shells
│   └── Ironic: Infected modules included MGS GDPR and Meetanshi Cookie
│
├── MAY 2025: Ransomware via Compromised MSP
│   ├── Group: DragonForce ransomware
│   ├── Attack: Gained access to unnamed MSP's infrastructure
│   ├── Method: Exploited vulnerabilities in SimpleHelp (RMM tool)
│   ├── Vulnerabilities: Discovered 2024; fixed Jan 2025
│   └── Problem: MSP did not install updates in time
│
├── JUNE 2025: Backdoor in 17 Popular npm Packages
│   ├── Attack: Hacked gluestack maintainer's account; used token
│   ├── Affected: 17 npm packages
│   ├── Most popular: @react-native-aria/interactions (125K weekly downloads)
│   ├── Total: Over 1 million downloads
│   └── Aftermath:
│       ├── Restricted GitHub access for secondary contributors
│       ├── Enabled 2FA for publishing new versions
│       └── Promised secure development practices
│
├── JULY 2025: npm Packages Infected via Phishing
│   ├── Target: Popular "is" package (2.7M weekly downloads)
│   ├── Method: Phishing via typosquatting + clone of npm site
│   ├── Result: Published malicious versions with backdoor
│   ├── Detection: Unnoticed for 6 hours
│   └── Note: Same attack on other developers; credentials saved for future
│
├── AUGUST 2025: s1ngularity Attack — Secrets Leaked from Hundreds of Developers
│   ├── Target: Nx — popular build system and CI/CD pipeline tool
│   ├── Malicious code searched for: crypto wallet keys, npm tokens,
│   │                                GitHub tokens, SSH keys, API keys
│   ├── AI tools abused: Claude Code, Gemini CLI, Amazon Q
│   ├── Leak: Public GitHub repos named s1ngularity-repository,
│   │         s1ngularity-repository-0, s1ngularity-repository-1
│   └── Impact: Confidential data of hundreds of developers accessible to anyone
│
├── SEPTEMBER 2025: Crypto Stealer in npm Packages — 2.6 Billion Weekly Downloads
│   ├── Attack: New phishing campaign targeting JavaScript developers
│   ├── Affected: Dozens of popular projects — chalk, debug
│   ├── Total: 2.6+ billion weekly downloads at time of compromise
│   ├── Payload: Crypto stealer — intercepted crypto transactions
│   ├── Result: Attackers botched final stage — only $925 stolen
│   └── Follow-up: First wave of Shai-Hulud (~150 npm packages,
│                  including Crowdstrike projects)
│
├── OCTOBER 2025: GlassWorm Worm in Visual Studio Code
│   ├── Type: Self-propagating malware
│   ├── Target: VS Code extensions in Open VSX Registry
│   │          and Microsoft Extension Marketplace
│   ├── Targets: GitHub, Git, npm, Open VSX accounts, crypto wallet keys
│   ├── Unusual C2:
│   │   ├── Primary: Crypto wallet on Solana blockchain
│   │   └── Backup: Google Calendar
│   └── Additional: Downloaded RAT called Zombi — full system control
│
├── NOVEMBER 2025: IndonesianFoods — 150,000 Spam Packages in npm
│   ├── Campaign: IndonesianFoods
│   ├── Method: Spammed npm with tens of thousands of useless packages
│   ├── Goal: Inflate metrics; earn tokens in tea.xyz blockchain
│   ├── Naming: "Name + Indonesian dish" (e.g., zul-tapai9-kyuki)
│   ├── Note: No account compromise; no malicious payload
│   │         (except script creating packages every 7 seconds)
│   └── Lesson: npm vulnerable to large-scale spam campaigns
│
└── DECEMBER 2025: Shai-Hulud 2.0 — 400,000 Developer Secrets Leaked
    ├── Most important event of the year in supply chain attacks
    ├── Shai-Hulud (aka Sha1-Hulud): Self-propagating worm
    │   ├── Searches for secrets; publishes in public GitHub repos
    │   └── Self-propagates by infecting projects of infected developers
    ├── First wave: September — several hundred npm packages infected
    ├── Second wave (Shai-Hulud 2.0):
    │   └── Added wiper functionality — erases user files if no tokens found
    ├── Leak: ~400,000 secrets in public repositories
    ├── First confirmed attack using leaked secrets:
    │   └── Trust Wallet — malicious Chrome extension with crypto drainer
    │       on Christmas Eve; $8.5 million stolen from thousands of users
    └── Consequences: Likely to be felt for a long time
```

---

## Key Themes Across 2025

```
KEY THEMES — 2025
│
├── npm Ecosystem
│   ├── Most targeted ecosystem
│   ├── DogWifTools, gluestack, "is", chalk, debug
│   ├── Shai-Hulud, IndonesianFoods
│   └── Why: Massive download counts; trusted by developers
│
├── Crypto Theft
│   ├── DogWifTools — $10M
│   ├── Vubit — $1.5B (largest crypto robbery ever)
│   └── Trust Wallet — $8.5M
│
├── Self-Propagating Worms
│   ├── Shai-Hulud — first wave September, second wave December
│   ├── Shai-Hulud 2.0 — added wiper functionality
│   └── GlassWorm — VS Code extensions; Solana + Google Calendar C2
│
├── AI Tools Abused
│   ├── s1ngularity attack used Claude Code, Gemini CLI, Amazon Q
│   └── Purpose: Find secrets in infected systems
│
├── Unusual C2 (Command & Control)
│   ├── GlassWorm: Solana blockchain (primary)
│   └── GlassWorm: Google Calendar (backup)
│
├── Public Leaks
│   ├── s1ngularity — public GitHub repos
│   ├── Shai-Hulud — public GitHub repos
│   └── Impact: Anyone can access leaked secrets
│
├── Delayed Patching
│   ├── MSP ignored SimpleHelp vulnerabilities
│   ├── Discovered 2024; fixed Jan 2025
│   └── Result: DragonForce ransomware attack in May
│
└── Spam Campaigns
    ├── IndonesianFoods — 150,000 packages
    └── Goal: tea.xyz blockchain tokens
```

---

## Defense Measures Tree

```
DEFENSE MEASURES AGAINST SUPPLY CHAIN ATTACKS
│
├── 1. Carefully Evaluate Vendors
│   ├── Check the code you use in your projects
│   └── Assess vendor security posture before cooperation
│
├── 2. Implement Contractual Security Requirements
│   ├── Security audits
│   ├── Incident notification protocols
│   └── Compliance with IS policies
│
├── 3. Develop an Incident Response Plan
│   ├── Detection procedures
│   └── Containment of attacks/incidents
│
├── 4. Monitor Suspicious Activity
│   ├── Use XDR (Extended Detection and Response)
│   └── Use MDR (Managed Detection and Response)
│
└── 5. Use External Threat Hunting Services
    └── If internal infosec resources are insufficient
```

---

## Final Takeaway

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  FINAL TAKEAWAY                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Supply chain attacks in 2025 were:                                         │
│  • RELENTLESS — month after month, new attacks                              │
│  • CREATIVE — AI tools abused, blockchain C2, wiper functionality           │
│  • DEVASTATING — billions stolen, 400,000 secrets leaked                    │
│                                                                             │
│  Attackers targeted every link in the chain:                                │
│  • GitHub repositories                                                      │
│  • npm packages                                                             │
│  • CI/CD tools                                                              │
│  • Crypto wallets                                                           │
│  • MSP infrastructure                                                       │
│  • VS Code extensions                                                       │
│                                                                             │
│  Most dangerous trend:                                                      │
│  • SELF-PROPAGATING MALWARE (Shai-Hulud, GlassWorm)                         │
│  • Spreads automatically using stolen credentials                           │
│                                                                             │
│  Organizations must adopt LAYERED DEFENSES:                                 │
│  • Vendor assessment                                                        │
│  • Contractual security                                                     │
│  • Incident response plans                                                  │
│  • XDR monitoring                                                           │
│  • External threat hunting                                                  │
│                                                                             │
│  Because NO SINGLE MEASURE IS ENOUGH.                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Full Summary Tree (One-Page View)

```
SUPPLY CHAIN ATTACKS 2025 (Kaspersky)
│
├── INCIDENTS BY MONTH
│   ├── Jan — DogWifTools RAT ($10M)
│   ├── Feb — Vubit Exchange ($1.5B)
│   ├── Mar — Coinbase GitHub Actions attempt
│   ├── Apr — Magento backdoor (21 extensions)
│   ├── May — DragonForce ransomware via MSP
│   ├── Jun — gluestack npm backdoor (17 packages)
│   ├── Jul — npm phishing ("is" package)
│   ├── Aug — s1ngularity (Nx compromise)
│   ├── Sep — Crypto stealer (2.6B downloads) + Shai-Hulud wave 1
│   ├── Oct — GlassWorm (VS Code)
│   ├── Nov — IndonesianFoods (150K spam packages)
│   └── Dec — Shai-Hulud 2.0 (400K secrets leaked)
│
├── KEY THEMES
│   ├── npm ecosystem most targeted
│   ├── Crypto theft ($1.5B+ total)
│   ├── Self-propagating worms (Shai-Hulud, GlassWorm)
│   ├── AI tools abused (Claude, Gemini, Amazon Q)
│   ├── Unusual C2 (Solana blockchain, Google Calendar)
│   ├── Public leaks (GitHub repos)
│   ├── Delayed patching (MSP ignored SimpleHelp)
│   └── Spam campaigns (IndonesianFoods)
│
└── DEFENSE MEASURES
    ├── Evaluate vendors
    ├── Contractual security
    ├── Incident response plan
    ├── XDR/MDR monitoring
    └── External threat hunting
```