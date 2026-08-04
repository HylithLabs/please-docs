---
title: "Privacy Policy"
description: "Privacy Policy for PLEASE, detailing our strict local data processing, zero model training policy, and commitment to user privacy."
date: 2026-08-05T00:00:00+00:00
lastmod: 2026-08-05T00:00:00+00:00
draft: false
type: "legal"
---

**Effective Date:** August 5, 2026  
**Publisher:** Hylith ("Company", "we", "us", or "our")  
**Software:** PLEASE Command-Line Tool ("PLEASE" or "Software")

---

### 1. Overview & General Undertaking

This Privacy Policy governs the privacy and data security standards applicable to the **PLEASE** command-line application operated by Hylith. We are committed to fundamental data privacy rights and zero-surveillance design principles. 

**PLEASE is a local-first software application.** It is engineered specifically to operate within your local computing environment without collecting, storing, harvesting, or selling your personal data, source code, repository content, or usage telemetries.

---

### 2. Local-First Data Processing Architecture

#### 2.1 Local Execution
All core functionality of the Software—including Git diff analysis, branch evaluation, status formatting, and repository interactions—executes locally on your workstation. No repository contents or command execution logs are ever transmitted to or processed through servers maintained or controlled by Hylith.

#### 2.2 Telemetry & Tracking Disclosure
PLEASE contains **zero tracking scripts, telemetry modules, analytics beacons, or remote logging hooks**. Hylith does not monitor your terminal activities, command execution counts, IP addresses, system metrics, or usage patterns.

---

### 3. Absolute Prohibition of Model Training & Data Retention

#### 3.1 Zero Model Training Policy
Hylith **does not train machine learning models** on your code, commit messages, diffs, terminal prompts, or repository metadata. We maintain no datasets, storage buckets, or training pipelines derived from user interactions with the Software.

#### 3.2 Transient Execution
When executing AI-assisted commands, repository diffs and user prompts are transmitted directly from your local terminal session to your configured AI provider's API. Neither Hylith nor any intermediate proxy owned by Hylith stores, logs, or intercepts these data payloads.

---

### 4. API Credentials & Key Management

#### 4.1 Local Storage
Your API access keys (including Anthropic Claude, Google Gemini, OpenAI, or local instances such as Ollama) are stored exclusively on your local device. 

#### 4.2 Credential Non-Disclosure
Your API keys are strictly utilized for direct authentication between your local terminal environment and your designated API provider. Under no circumstances are your API keys or access tokens transmitted to or visible by Hylith.

---

### 5. Third-Party AI Provider Transmissions

When you elect to enable AI-powered features, PLEASE communicates directly with your chosen third-party AI provider API. These requests are governed directly by the privacy policies and API terms of service of the respective provider:

- **Anthropic:** Subject to the [Anthropic Commercial Terms of Service](https://www.anthropic.com/legal/commercial-terms).
- **Google Cloud / Gemini API:** Subject to the [Google Cloud Data Governance Terms](https://cloud.google.com/privacy).
- **OpenAI:** Subject to the [OpenAI Business Terms](https://openai.com/policies/business-terms).
- **Self-Hosted / Local (Ollama, LM Studio):** Executes 100% locally on your machine with zero external network transmission.

Most enterprise AI API providers maintain contractual policies guaranteeing that data sent via commercial APIs is not retained or used for foundation model training.

---

### 6. User Rights & Data Control

Because PLEASE stores all configuration, keys, and repository data locally on your device, you retain total control over your data at all times:
- You may purge local configuration settings or API keys at any time by removing your local configuration file.
- Uninstalling the Software completely removes the application binary from your system.

---

### 7. Revisions & Contact Information

Hylith reserves the right to amend this Privacy Policy to reflect software updates or legal compliance standards. Any revisions will be published at this location with an updated Effective Date.

If you have questions regarding this Privacy Policy or our software security architecture, please contact us at:

- **Company:** Hylith
- **Website:** [hylith.com](https://hylith.com)
- **Repository:** [github.com/HylithLabs/please](https://github.com/HylithLabs/please/)
