# 🛡️ MiMoRug

### Rugpull Risk Predictor — Powered by Xiaomi MiMo V2.5

Paste any Ethereum token contract. Get a 0–100 rug probability score with 12-signal forensic breakdown — explained in plain English by Xiaomi MiMo V2.5.

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=for-the-badge&logo=github)](https://gyoomei.github.io/mimorug/)
[![Try Now](https://img.shields.io/badge/Audit-Now-ef4444?style=for-the-badge&logo=googlechrome)](https://gyoomei.github.io/mimorug/)
[![AI](https://img.shields.io/badge/AI-Xiaomi%20MiMo%20V2.5-f97316?style=for-the-badge)](https://huggingface.co/XiaomiMiMo)
[![Data](https://img.shields.io/badge/Data-GoPlus%20%2B%20Blockscout-22c55e?style=for-the-badge)](https://gopluslabs.io)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 📖 The Problem

Every week, thousands of new tokens deploy on Ethereum. Most are scams. Existing tools like TokenSniffer flag known patterns but don't reason about combined signals — and most charge for premium features.

**MiMoRug closes the gap.** Paste a contract, get an actionable verdict.

The audit engine pulls 40+ security fields from GoPlus, scores 12 weighted risk signals, and lets MiMo V2.5 compose a plain-English verdict. Result: a 0–100 rug score backed by traceable reasoning, free for everyone.

---

## ✨ Core Features

### 🎯 12 Risk Signals

| Signal | Weight | What It Catches |
|--------|--------|-----------------|
| Honeypot | 30 | Cannot sell after buying — pure scam |
| Mintable Supply | 20 | Owner can dilute holders infinitely |
| Hidden Owner | 20 | Control obscured — likely rug prep |
| Sell Tax >20% | 20 | Extraction tax disguised as fee |
| Take-back Ownership | 15 | Renounce reversible — fake decentralization |
| Blacklist Function | 15 | Owner can freeze any wallet |
| Closed Source | 15 | Can't audit — black box |
| Holder Concentration | 15 | Top 10 wallets dominate supply |
| Trading Pausable | 10 | Owner can halt trading anytime |
| Buy/Sell Tax 5–10% | 10 | Moderate extraction risk |
| LP Risk | 10 | Few/unlocked LPs — soft rug enabler |
| DEX Listing | 5 | No liquidity available |
| Self-destruct | +25 | Contract can erase itself |
| Upgradeable Proxy | +8 | Logic can change without warning |

### 📊 Verdict Tiers

| Score | Tier | Action |
|-------|------|--------|
| 0–14 | ✅ LOOKS SAFE | Standard DeFi caution applies |
| 15–39 | 🟡 PROCEED WITH CAUTION | Verify each warning |
| 40–69 | 🟠 HIGH RISK | Avoid unless experienced |
| 70–100 | 🚨 RUG ALERT | Do NOT interact |

### 🌐 Other

- 🌍 Bilingual EN / ID full translation
- 🌓 Dark / Light theme (WCAG-AA contrast)
- 📱 Mobile-first responsive (clamp 320px → 1440px)
- 🔗 Shareable URL (hash-based deep link)
- 🚀 Single zero-dependency HTML on GitHub Pages

---

## 🏗️ Architecture

```
INPUT: Token contract (0x...)
    ↓
GoPlus Security API → 40-field audit (no API key)
    ↓
12-Signal Risk Analyzer → weighted score 0-100
    ↓
MiMo V2.5 Narrative Engine → plain-English verdict
    ↓
SVG Risk Gauge + Signal Grid + Stats
```

Three free APIs power the audit:
- **GoPlus Security** — honeypot/owner/tax/holder analysis
- **Blockscout** — contract verification, creation tx history
- **CoinGecko** — market data when available

---

## 🚀 Quick Start

```bash
git clone https://github.com/gyoomei/mimorug.git
cd mimorug
python3 -m http.server 8080
# Open http://localhost:8080
```

Or just visit the [live demo](https://gyoomei.github.io/mimorug/).

---

## 📁 Project Structure

```
mimorug/
├── index.html       # UI + CSS (15 KB)
├── app.js           # Audit engine + i18n + render (28 KB)
└── README.md
```

Total: ~45 KB. Zero npm dependencies. Loads in <1s.

---

## 🎨 Risk Tier Examples

| Token | Score | Verdict |
|-------|-------|---------|
| USDC | ~18 | 🟡 CAUTION (proxy upgradeable) |
| PEPE | ~15 | 🟡 CAUTION (memecoin standards) |
| SHIB | ~12 | 🟡 CAUTION (older contract) |
| Honeypot scam | 70+ | 🚨 RUG ALERT |

---

## 🛣️ Roadmap

- [x] 12-signal weighted scoring
- [x] GoPlus integration (40 fields)
- [x] MiMo V2.5 plain-English verdict
- [x] SVG risk gauge
- [x] Bilingual EN / ID
- [x] Dark / Light theme
- [x] Mobile responsive
- [ ] Multi-chain (Base, Arbitrum, BSC)
- [ ] Dev wallet history scoring (multi-token rug pattern)
- [ ] Comparison against known rug DB
- [ ] Telegram bot integration

---

## 📸 Screenshots

[See screenshots in this repo](./screenshots/) or live demo.

---

## 📜 License

MIT © 2026 — built with 🧠 by Xiaomi MiMo V2.5

---

## 🔗 Links

- **Live:** https://gyoomei.github.io/mimorug/
- **GoPlus Security:** https://gopluslabs.io
- **Blockscout:** https://eth.blockscout.com
- **Xiaomi MiMo:** https://huggingface.co/XiaomiMiMo

---

*Built for users who got rugged once and never want to again.*
