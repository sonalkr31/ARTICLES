# ARTICLES
ARTICLES like attacks, tech, etc
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

You can see Cheetsheet and Tree from in SupplyChain.md File .

thank you
