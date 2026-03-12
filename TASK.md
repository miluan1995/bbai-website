# BBAI Official Website Task

Build a single-page official website for BBAI (Black Bear AI) token project.

## Design
- Cyberpunk/dark theme matching the existing dashboard (colors: #060816 bg, #58e0ff cyan, #ff4fd8 pink, #c9ff4f lime)
- Mobile responsive
- Smooth scroll animations
- Single `index.html` file with inline CSS/JS (no build tools)

## Sections (top to bottom)

### 1. Hero
- Large "BBAI" title with glow effect
- Tagline: "AI-Powered Buyback & Burn on BSC"
- "Black Bear AI" subtitle
- Two CTA buttons: "View Dashboard" → `/dashboard/` and "Join Community" → `https://t.me/+bj5r2b79s8RiYzQx`

### 2. About
- Brief description: BBAI is an AI-driven vault that uses Flap AI Oracle to make intelligent buyback & burn decisions on BSC
- 3 feature cards:
  - 🤖 AI Oracle — Powered by Flap AI Oracle for smart decision making
  - 🔥 Auto Burn — Automated buyback and burn mechanism
  - 🛡️ Transparent — Fully open-source, verified on BSCScan

### 3. How It Works
- Simple 3-step flow with icons:
  1. BNB flows into the vault
  2. AI Oracle analyzes market conditions
  3. Smart buyback & burn executes automatically

### 4. Live Stats
- Fetch live data from BSC RPC (read-only, no wallet needed):
  - Vault BNB Balance (cast equivalent via ethers.js or raw JSON-RPC)
  - Total AI Oracle Requests (call `totalReqs()` on vault)
  - Token contract address display
- Vault address: `0xdb192b58371ea8f79b79daba169bccb292fae65b`
- RPC: `https://bsc-dataseed1.binance.org`
- Use raw `fetch()` with JSON-RPC `eth_call` — no external libraries

### 5. Contract Addresses
- Table showing:
  - BBAI Token: `0xa89500641846D9De787D2C34647730DB49e67777`
  - V3 Vault: `0xdb192b58371ea8f79b79daba169bccb292fae65b`
  - FlapAIProvider: `0xaEe3a7Ca6fe6b53f6c32a3e8407eC5A9dF8B7E39`
- Each address links to BSCScan

### 6. Community & Links
- Twitter: https://x.com/miluan1995
- Telegram: https://t.me/+bj5r2b79s8RiYzQx
- GitHub: (leave as #)
- BSCScan Vault: https://bscscan.com/address/0xdb192b58371ea8f79b79daba169bccb292fae65b

### 7. Footer
- "Built by Black Bear AI 🐻 | Powered by Flap AI Oracle"
- "Part of the Flap $15K Developer Competition"

## Technical Requirements
- Pure HTML/CSS/JS, single file, no dependencies
- Use `fetch` for JSON-RPC calls to read vault data
- Responsive (mobile-first)
- Fast loading, no external fonts (use system fonts or embed minimal)
- Output: `index.html` in this directory
