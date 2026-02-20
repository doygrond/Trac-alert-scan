# TracAlert — P2P Price Alert Agent

> A fork of [Trac-Systems/intercom](https://github.com/Trac-Systems/intercom) that adds a decentralized crypto price alert agent powered by the Intercom P2P sidechain network.

[![Live Demo](https://img.shields.io/badge/Demo-Live-00e5ff?style=flat-square)](https://YOUR_GITHUB_USERNAME.github.io/intercom)
[![Fork of Intercom](https://img.shields.io/badge/Fork-Trac--Systems%2Fintercom-1a3040?style=flat-square)](https://github.com/Trac-Systems/intercom)

---

## What is TracAlert?

TracAlert is a **peer-to-peer price alert broadcasting agent** built on top of the Intercom network stack. Instead of relying on centralized alert servers, your alerts are broadcast directly to peers via Intercom sidechannels.

### Features

- **Set price alerts** for BTC, ETH, SOL, BNB, XRP — above or below a target price
- **P2P broadcast** — alerts are shared across Intercom peers in real time
- **Live price feed** — simulated live prices with 2-second refresh
- **Agent activity log** — see what peers are doing across the network
- **Real-time notifications** — popup when your alert triggers
- **Zero backend** — runs entirely in the browser, P2P via Intercom

### How It Works

1. User sets a price alert (e.g. "BTC above $100,000")
2. Alert is broadcast to Intercom P2P sidechannel peers
3. Each agent monitors prices and fires the alert when condition is met
4. Triggered alerts are broadcast back to all connected peers

---

## Trac Reward Address

```
trac15ks5z8a9sfp6x44f0hycttpwdz73dqhrmvkaankhws4s3330pnesatkyj7
```

> Replace this with your actual Trac address to receive 500 TNK payout.

---

## Screenshots

> Add screenshots or screen recording of `index.html` running in browser here.

---

## Quick Start

```bash
# Clone this fork
git clone https://github.com/YOUR_USERNAME/intercom
cd intercom

# Open the app
open index.html
# or serve locally:
npx serve .
```

No build step needed — it's a single HTML file.

---

## Skill File

See [`SKILL.md`](./SKILL.md) for agent instructions.

---

## Contributing

Built on top of [Trac-Systems/intercom](https://github.com/Trac-Systems/intercom).  
PR to [awesome-intercom](https://github.com/Trac-Systems/awesome-intercom) pending.
