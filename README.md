# 🦞 Clawders

**The community guide to running OpenClaw securely, affordably, and efficiently**

[![OpenClaw](https://img.shields.io/badge/OpenClaw-2026.1.30+-orange)](https://openclaw.ai)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/tomerb3/clawders/pulls)

![Clawders Banner](https://devopsite.top/github-pic1-openclaw.jpeg)

---

## 🎯 What is Clawders?

**Clawders** is an updated, community-maintained guide for installing and running [OpenClaw](https://openclaw.ai) in a way that is:

- 🔒 **Secure** — Minimize risk with proper isolation, burner accounts, and hardened configurations
- 👤 **User-Friendly** — Step-by-step instructions from basic to advanced, suitable for beginners
- 💰 **Token-Efficient** — Run on FREE models (NVIDIA NIM, Ollama) or optimize paid usage to avoid surprise bills

This guide was compiled from real-world community experience, official documentation, and security research — so you don't have to learn the hard way.

---

## ⚠️ Critical Security Warning

> **OpenClaw security vulnerabilities are by design.** The attack surface is every input. There is currently no way to fully secure its usage.

These guides help **minimize the blast radius** if something goes wrong. The golden rule:

> **Treat OpenClaw like an untrusted contractor with access to whatever you give it.**

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| [openclaw/OpenClaw_Installation_Guide.md](openclaw/OpenClaw_Installation_Guide.md) | **📘 Complete Installation Guide** — 9 sections covering prerequisites, security setup, 3 installation methods, 4 model providers, hardening, and troubleshooting |
| [openclaw/OpenClaw_Installation_Guide.pdf](openclaw/OpenClaw_Installation_Guide.pdf) | **📄 PDF Version** — Same comprehensive guide in printable format |
| [openclaw/openclaw-tips.txt](openclaw/openclaw-tips.txt) | **💡 Quick Tips** — Community-sourced tips and tricks |

---

## 🚀 Quick Start Options

### Option 1: One-Command Install (FREE - Easiest)

```bash
curl -fsSL skyler-agent.github.io/oclaw/i.sh | bash
```

This community installer (created with OpenClaw's founder @steipete):
- ✅ Automatically configures **MiniMax M2.1** (completely FREE model)
- ✅ One-click authentication — no manual API keys
- ✅ Includes optimized "7-day Coding Plan" presets
- ✅ Works out of the box

*Source: [@SkylerMiao7](https://x.com/SkylerMiao7/status/2017789329138212986) (73K+ views)*

### Option 2: Docker Install (Recommended for Security)

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
docker compose run --rm openclaw-cli onboard
docker compose up -d openclaw-gateway
```

Then harden with our [security guide](openclaw/OpenClaw_Installation_Guide.md#5-security-hardening).

### Option 3: VPS / Cloud Deployment

Use [DigitalOcean's 1-Click Deploy](https://www.digitalocean.com/community/tutorials/how-to-run-openclaw) for a pre-hardened cloud setup.

---

## 🔒 Essential Security Checklist

**Before you install, you MUST:**

| Step | Why It Matters |
|------|----------------|
| ✅ Use a **dedicated machine** | If compromised, only that machine is affected |
| ✅ Create **burner email** | Don't expose your real inbox |
| ✅ Create **new GitHub account** | Use Personal Access Tokens with limited scope |
| ✅ Use **burner phone/SIM** | For WhatsApp/Telegram integration |
| ❌ Never connect **primary email** | Full inbox access = full compromise |
| ❌ Never connect **banking/financial** | No exceptions, ever |
| ❌ Never connect **password managers** | Would expose all your credentials |

### The Freelancer Test™

> Before connecting ANY service, ask yourself:
> *"Would I give this access to a random freelancer I just hired online?"*
>
> **If the answer is NO → Don't give it to OpenClaw.**

---

## 💰 Free & Token-Efficient Model Options

One community member spent **$0.60 just saying "hi"** with default Anthropic settings. Don't be that person.

### Free Options

| Provider | Model | Setup |
|----------|-------|-------|
| **NVIDIA NIM** | MiniMax, Kimi K2.5 | [build.nvidia.com](https://build.nvidia.com) → Settings → API Keys |
| **Ollama** | qwen2.5, llama3, etc. | [ollama.com](https://ollama.com) — Runs 100% locally |
| **One-Command Installer** | MiniMax M2.1 | See Quick Start above |

### Critical: Limit Token Usage

```bash
openclaw config set agents.defaults.contextTokens 25000
```

---

## 🛡️ Security Tools & Resources

- **[openclaw-shield](https://github.com/knostic/openclaw-shield)** — Prevents leaking secrets, PII, and destructive commands
- **[awesome-openclaw](https://github.com/thewh1teagle/awesome-openclaw)** — Curated list of tools, guides, and integrations

---

## 🤝 Contributing

Found a tip that saved you hours? A security practice that should be shared?

**PRs are welcome!**

---

## 📜 Credits

This guide was compiled from community wisdom (Israeli tech WhatsApp group), official OpenClaw documentation, and security research from JFrog, Composio, DigitalOcean, and VentureBeat.

Special thanks to @steipete (OpenClaw), @SkylerMiao7 (one-command installer), and the Knostic team (openclaw-shield).

---

<p align="center">
  <b>Stay secure. Stay efficient. Stay clawed. 🦞</b>
</p>
