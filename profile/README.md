<div align="center">

# 🧭 SecuardenAI

**Building open-source tools for product security intelligence**

[![Website](https://img.shields.io/badge/Website-secuarden.com-00d4ff?style=for-the-badge)](https://secuarden.com)
[![Twitter Follow](https://img.shields.io/twitter/follow/secuarden?style=for-the-badge&logo=twitter&color=00d4ff)](https://twitter.com/secuarden)
[![GitHub Org's stars](https://img.shields.io/github/stars/SecuardenAI?style=for-the-badge&color=7CC243)](https://github.com/SecuardenAI)

</div>

---

## 🚀 Our Projects

<table>
<tr>

### 💻 [Secuarden CLI](https://github.com/secuardenai/secuarden-cli)

[![Stars](https://img.shields.io/github/stars/SecuardenAI/secuarden-cli?style=social)](https://github.com/SecuardenAI/secuarden-cli)

A passive capture agent for AI coding sessions. Hooks into Claude Code (Cursor, Copilot coming) and records every file read, shell command, and tool call into a local SQLite ledger — secrets scrubbed before anything hits disk.

The problem it solves: AI coding agents take 50+ actions per session. Git shows what changed; it doesn't show the agent read your .env, ran 47 commands, and rewrote 12 files in 90 seconds. When SOC 2 auditors ask "who authorized this AI change?" you need more than a commit log.

### How it works:

- secuarden init installs hooks and creates the database in under a second
- Every action gets a structured event: timestamp, action type, file paths, developer identity, session context
- Two-layer privacy: sensitive file detection suppresses content; pattern-based redaction scrubs API keys, tokens, JWTs, and credentials from commands and output
- All data stays local by default (add SecuardenAI SaaS `--api-key`) to enable SaaS sync and get per-session risk feedback printed to your terminal the moment a session ends
- Built for: security and GRC teams that need an evidence trail for AI-assisted development, platform teams rolling out AI tools across engineering, and individual developers who want to know exactly what the agent did.

Open source (Apache 2.0). The capture agent is free. The compliance intelligence platform is [secuarden.ai](https://secuarde.ai).
<td>
</tr>
<tr>
<td width="50%" valign="top">

### 🧭 [ComplianceCompass](https://github.com/SecuardenAI/compliance-compass)

The missing layer between AppSec findings and SOC2 / ISO / PCI evidence.

**Interactive tool** to map security requirements across OWASP, ISO27001, and NIST SSDF

[![Stars](https://img.shields.io/github/stars/SecuardenAI/compliance-compass?style=social)](https://github.com/SecuardenAI/compliance-compass)
[![Live Demo](https://img.shields.io/badge/Live-Demo-00d4ff)](https://secuardenai.github.io/compliance-compass)

**Key Features:**
- 🔍 Search across 3+ standards
- 🗺️ Cross-framework mappings
- 📥 Export for audits
- 💡 Implementation guidance

</td>
<td width="50%" valign="top">

### 🧭 [Context Confidence Rating Calculator](https://github.com/secuardenai/context-confidence-rating)

Why CVSS fails modern apps — and how CCR fixes it.

***Lightweight Python library*** that prioritizes vulnerabilities based on actual exploitability in your codebase

[![Stars](https://img.shields.io/github/stars/SecuardenAI/context-confidence-rating?style=social)](https://github.com/SecuardenAI/context-confidence-rating)


**Key Features:**
- 🎯 0-100 confidence scoring
- 🔍 Framework & dependency detection
- ⚡ Zero dependencies, pure Python
- 🤖 CI/CD ready with JSON output

```python
pip install context-confidence-rating
ccr analyze /path/to/repo
```
</td>
</tr>
<tr>
<td width="50%" valign="top"> 

### 🧐 [Secuarden Headers](https://github.com/SecuardenAI/secuarden-headers)
Modern HTTP security headers scanner for catching misconfigurations before they become vulnerabilities.  
Professional-grade CLI tool for analyzing security headers across your web applications with instant scoring and actionable insights.

[![CI](https://github.com/SecuardenAI/secuarden-headers/workflows/CI/badge.svg)](https://github.com/SecuardenAI/secuarden-headers/actions)
[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Code Style: Black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

**Key Features:**
* 🚀 **Async Scanning** - Concurrent analysis of multiple URLs with configurable limits
* 🎯 **Modern Headers** - Checks COOP, COEP, CORP, Permissions-Policy, CSP, HSTS, and more
* 📊 **Security Scoring** - Instant 0-100 rating with detailed breakdowns
* 🎨 **Rich CLI** - Beautiful terminal output with colors, tables, and progress indicators
* 📄 **Export Options** - JSON/CSV output for integration with CI/CD and reporting
* 🐳 **Docker Ready** - Pre-built container for seamless deployment
* ⚡ **Developer First** - Python 3.10+ with type hints, async/await, comprehensive tests
```bash
# Quick Start
pip install secuarden-headers
secuarden-headers https://yourapp.com -o results.json
```

**Perfect for:** DevSecOps teams, security audits, CI/CD integration, compliance validation
</td>
<td width="50%" valign="top">

### 🔮 Coming Soon

**More open-source security tools** in development:

- 📊 Security Metrics Dashboard
- 🤖 AI-Powered Risk Scoring
- 📝 Audit Template Generator
- 🔐 SBOM Generator & Analyzer

**Watch this space!** ⭐

</td>
</tr>
</table>

---

## 💡 Our Mission

We believe **security compliance shouldn't be a mystery**. We're building open-source infrastructure for context-aware application security.

### What We're Solving

| Problem | Our Solution |
|---------|--------------|
| 😵 Compliance frameworks use different terminology | 🗺️ Clear cross-framework mappings |
| 📚 Dense, hard-to-parse standards documents | 🔍 Interactive, searchable tools |
| ⏰ Manual audit preparation takes weeks | ⚡ Automated evidence generation |
| 🤔 Unclear what to implement | 💡 Actionable recommendations |

---

## 🤝 Get Involved

<div align="center">

| 💡 Have an Idea? | 🐛 Found a Bug? | 🛠️ Want to Contribute? | 💬 Questions? |
|:---:|:---:|:---:|:---:|
| [Request Feature](https://github.com/SecuardenAI/compliance-compass/issues/new?template=feature_request.yml) | [Report Bug](https://github.com/SecuardenAI/compliance-compass/issues/new?template=bug_report.yml) | [Contributing Guide](https://github.com/SecuardenAI/compliance-compass/blob/main/CONTRIBUTING.md) | [Discussions](https://github.com/orgs/SecuardenAI/discussions) |

</div>

### 🌟 Ways to Contribute

- ⭐ **Star our repos** - Show your support!
- 🐛 **Report issues** - Help us improve
- 📝 **Improve docs** - Make it clearer
- 💻 **Submit PRs** - Add features or fixes
- 🗺️ **Add standards** - Expand coverage (PCI-DSS, SOC 2, HIPAA)
- 📢 **Spread the word** - Share with your network

---

## 🏗️ Tech Stack

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

---

## 📊 Impact

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/SecuardenAI?style=for-the-badge&color=7CC243)
![GitHub forks](https://img.shields.io/github/forks/SecuardenAI/compliance-compass?style=for-the-badge&color=00d4ff)
![GitHub contributors](https://img.shields.io/github/contributors/SecuardenAI/compliance-compass?style=for-the-badge&color=7CC243)

</div>

---

## 🌟 Built By

<div align="center">

### [Secuarden](https://secuarden.ai)

**Product Security Intelligence That Auditors Actually Accept**

Secuarden transforms how organizations approach application security by bridging the gap between security tools and business requirements. We analyze application security at scale and deliver context-aware intelligence that helps teams prioritize what actually matters.

**What We Do:**
- 🎯 **Context-Aware Risk Assessment** - Our Context Confidence Rating (CCR™) evaluates security findings within your specific business context, application architecture, and threat landscape
- 🤖 **AI-Powered Security Intelligence** - Leverage LLM-powered analysis to understand vulnerability impact, recommend remediation strategies, and auto-generate audit evidence
- 📊 **Compliance Automation** - Map security controls to multiple frameworks (OWASP, ISO27001, NIST, SOC 2, PCI-DSS) and generate audit-ready documentation
- ⚡ **Actionable Insights** - Cut through the noise with prioritized findings that combine technical severity with business impact

**Why Teams Choose Secuarden:**
Traditional security tools overwhelm teams with alerts lacking business context. Secuarden delivers intelligence that auditors accept and developers trust, helping you ship secure products faster without drowning in false positives.

---

**Why we build in the open:**  
We were frustrated by the complexity of security compliance.  
We built tools to help ourselves.  
We're sharing them to help everyone.

---

<sub>Built with ❤️ for the security community</sub>

[![Website](https://img.shields.io/badge/🌐_Website-secuarden.ai-00d4ff)](https://secuarden.ai)
[![Twitter](https://img.shields.io/badge/🐦_Twitter-@secuarden-00d4ff)](https://twitter.com/secuarden)
[![Email](https://img.shields.io/badge/📧_Email-support@secuarden.ai-7CC243)](mailto:support@secuarden.ai)

</div>