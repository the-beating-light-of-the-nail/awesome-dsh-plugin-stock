# Awesome DSH Stock & Finance Plugins [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

English | [中文](README.zh.md)

> A curated vertical list of **stock / finance / quant** plugins for [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) (`dsh`).
>
> 🌐 Browse all verified stock/quant plugins with screenshots on [DSH Meme Hub — Stocks & Quant](https://dsh-meme-hub.cdqyfdbymn.me/plugins/stock).

DeepSeek Harness is DeepSeek's open-source agent harness — everything is a plugin, and the community has been shipping a lot of them. General directories list *everything*; this list only tracks plugins for **trading, market data, quant research, investment analysis, and broker access** — so you don't have to dig through hundreds of UI tweaks to find the finance stuff.

Every entry has been verified against its README (function, install method, data sources, trading capability). Plugins are grouped by what they actually do, not by what they're called.

> [!WARNING]
> Installing a plugin runs third-party code on your machine with your own permissions. Being listed here is **not** a security review — check the source before you install. Plugins that touch real brokerage accounts or credentials are marked explicitly below.

## Contents

- [📊 Market Data & Watchlists](#-market-data--watchlists)
- [🎨 Trading Terminals & Skins](#-trading-terminals--skins)
- [🔬 Quant Research](#-quant-research)
- [💼 Investment & Financial Research](#-investment--financial-research)
- [🏦 Broker & Account Access](#-broker--account-access)
- [🎮 Fun & Simulation](#-fun--simulation)
- [🧰 Related](#-related)
- [Platform & Data-source Matrix](#platform--data-source-matrix)
- [Safety Notes](#safety-notes)
- [Contributing](#contributing)
- [Disclaimer](#disclaimer)

## 📊 Market Data & Watchlists

- [Awu12277/dsh-stock-watch](https://github.com/Awu12277/dsh-stock-watch) - A-share real-time watchlist panel (collapsible popup in the DSH Web UI): grouped watchlists, minute/daily/weekly K-lines, buy/sell target-price alerts. ★50 · Tencent Finance · MIT
- [3930a/dsh-stock-watch](https://github.com/3930a/dsh-stock-watch) - Always-on A-share ticker strip under the input box (3s refresh, red-up/green-down, editable watchlist, `/stock/*` data routes, two-way sync with a local watchlist.json). ★2 · Eastmoney · MIT
- [Bob-Bo1/dsh-stock-watch](https://github.com/Bob-Bo1/dsh-stock-watch) - A-share holdings/watchlist observer in the sidebar: reads a local holdings.json, shows live quotes and P&L. Explicitly does **not** place orders. ★1 · Tencent Quotes · MIT
- [Realyujie/dsh-us-stocks](https://github.com/Realyujie/dsh-us-stocks) - US-stock data toolkit exposing six structured tools to the agent: quote / history / financials / analyst views / news / ownership, with browser-side candlestick rendering. ★5 · yahoo-finance2 · MIT
- [omdsh-dev/dsh-fun-ticker](https://github.com/omdsh-dev/dsh-fun-ticker) - Persistent marquee ticker at the bottom of the session: crypto, FX, A-share, index and HK/US quotes in any combination, keyless data sources. ★4 · Binance / CoinGecko / Eastmoney / Sina / Frankfurter
- [Hermit503/dsh-trading-terminal](https://github.com/Hermit503/dsh-trading-terminal) - A-share + domestic futures watch terminal: watchlist, top gainers, limit-up/down pools, hot searches, sector rankings, 31 futures main-contract K-lines plus AI-driven fundamental/technical analysis. Watch-only, no order placement. ★1 · Tencent / Sina / Eastmoney · MIT
- [helibeiqi/dsh-quant-data-mcp](https://github.com/helibeiqi/dsh-quant-data-mcp) - Zero-dependency MCP stdio server template with an A-share data example: daily OHLCV, real-time snapshots, financials, northbound capital, sector data (6 tools). ★0 · Eastmoney / Tencent · MIT

## 🎨 Trading Terminals & Skins

- [linhut/dsh-stock-terminal](https://github.com/linhut/dsh-stock-terminal) - Global trading-terminal visual skin plus a live quotes panel: watchlist marquee, pinyin fuzzy search, holdings P&L, index snapshots, K-line popups. Covers A-shares, HK, US, crypto and FX. ★2 · Apache-2.0 (per README; metadata NOASSERTION)
- [renat3u/tonghuashun-webui](https://github.com/renat3u/tonghuashun-webui) - Tonghuashun-style terminal skin for DSH Web. ⚠️ The "K-lines" visualize **token usage and code changes** — local mock data, not real quotes. ★10
- [AdamPlatin123/dsh-tonghuashun](https://github.com/AdamPlatin123/dsh-tonghuashun) - Tonghuashun terminal skin (`ui-skin-ths`) + code-volume K-line panel (`ui-market`). ⚠️ K-lines show code-change volume, not real market data. ★2 · MIT

## 🔬 Quant Research

- [pengpengyi92/dsh-quant](https://github.com/pengpengyi92/dsh-quant) - Native dsh quant toolkit (npm package, 46 `quant_*` tools across 6 domains): end-to-end PDAT→PET research pipeline from data → indicators → factors → backtest → risk → execution simulation, with UI/CLI. ★12 · Crypto/A-share/US · Binance / OKX / Bybit / Yahoo / Sina / Tencent + a 15-channel knowledge base (Tushare, AkShare) · MIT
- [maddogfinance/dsh-trading](https://github.com/maddogfinance/dsh-trading) - Trading research workbench (5 npm packages): typed market-data seam, CSV provider template, deterministic indicator library, interactive K-line cards, and a `risk-guard` pre-execution gate. Hard boundary: research only, never places orders. ★6 · US/Crypto · BYO data (ClickHouse/CCXT/broker APIs) · MIT
- [dmsobtl/dsh-quant-workbench](https://github.com/dmsobtl/dsh-quant-workbench) - Quant research workbench as an installable profile: combines market-data/backtest/vision-router/session-analyst plugins plus 3 preset skills (momentum scan, strategy backtest, crypto analysis). ★1 · A-share/US/Crypto · Sina / Eastmoney / Yahoo / Binance
- [linxichen/dsh-rigorquant](https://github.com/linxichen/dsh-rigorquant) - Empirical/computational finance research framework (agent preset + skills + role-routing plugin): context-isolated multi-agent research lab for portfolio construction, optimization, simulation and econ-fin math, with an evidence meta-validator. ★2 · sympy/cvxpy (no market-data feeds) · MIT
- [kentleenot/dsh-trading-toolkit](https://github.com/kentleenot/dsh-trading-toolkit) - A-share + US stock toolkit: quotes, K-lines, ADX three-state signals, simple long/short backtest preview. Author's live strategy is open read-only for teaching; never places orders. ★0 · Eastmoney · MIT
- [AllenCX/dsh-quant-workspace](https://github.com/AllenCX/dsh-quant-workspace) - Self-contained quant research workspace: built-in Python engine pulls Yahoo daily bars, single-symbol signal cards, rule backtests, health re-checks, interactive HTML charts, strategy registry. Read-only design. ★0 · Yahoo Finance · MIT

## 💼 Investment & Financial Research

- [eclipti/dsh-invest-research](https://github.com/eclipti/dsh-invest-research) - A-share full-chain investment research: one command runs quote snapshot → Buffett seven-dimension value score → risk scan → analyst consensus → conservative DCF valuation, outputting a structured research report. ★0 · Eastmoney (Tencent fallback) · MIT
- [hancao97/hanai-investment-dsh](https://github.com/hancao97/hanai-investment-dsh) - Local-first A-share value research workbench (standalone profile with a full React product): market dashboard, watchlist, 4 investor-persona agents, versioned reports, follow-up Q&A. ★3 · Eastmoney / Tencent / GuruFocus · MIT
- [v587d/capital-generation](https://github.com/v587d/capital-generation) - AI investment agent aimed at Chinese retail investors (Python + MCP, installed as a dsh bundle). BYOK: Wind, Tonghuashun and AkShare as free fallback. ★? · Apache-2.0
- [zhang787jun/dsh-finance](https://github.com/zhang787jun/dsh-finance) - Finance & accounting workflow plugin (DSH adaptation of Anthropic Finance): 8 skills covering journal entries, reconciliation, financial statements, variance analysis, period close, SOX testing, audit, plus 5 validation tools. Does not keep books or make investment decisions for you. ★4 · MIT (parts derived from Apache-2.0)
- [hanjixin/dsh-finance-plugins](https://github.com/hanjixin/dsh-finance-plugins) - A suite of 19 finance plugins (`@hanjixin/dsh-tool-*`): A-share/US quotes, FX, quant indicators, risk control, portfolio analysis, crypto, fund NAV, macro data, plus a DSH Market showcase frontend. Optional Tushare/Wind/Choice/JoinQuant. ★1 · Sina / Tencent / TTFund / CoinGecko / ECB / World Bank
- [coder-wu/dsh-finance-data](https://github.com/coder-wu/dsh-finance-data) - Incremental financial data collection tools. ★1 · MIT

## 🏦 Broker & Account Access

> ⚠️ These plugins touch real accounts or credentials. Review code carefully before installing.

- [omdsh-dev/dsh-longbridge](https://github.com/omdsh-dev/dsh-longbridge) - Longbridge HK/US market integration: quotes, K-lines, indices, watchlists **plus account funds/positions and order placement/cancellation** — trading tools are forced through the DSH approval channel, and App Key/Secret/Access Token live only in the DSH credential vault. ★4 · Longbridge OpenAPI · BSD-3-Clause
- [PM25000/dsh-ths-holdings](https://github.com/PM25000/dsh-ths-holdings) - Tonghuashun holdings P&L floating card: reads your real holdings to show today's P&L, SSE index and intraday chart (20s polling, read-only). Requires pasting a Tonghuashun login cookie into `ctx.credentials`. ★1 · tzzb.10jqka.com.cn · MIT
- [dyc-code/fundpilot-dsh](https://github.com/dyc-code/fundpilot-dsh) - Personal OTC fund portfolio read-only analysis: CSV holdings import → auditable ledger → official NAV → deterministic returns → end-of-day confirmation reports, with DSH tools and a Web UI. Explicitly executes **no** subscriptions/redemptions/trades. ★0 · Tushare (primary) / Eastmoney / Tencent

## 🎮 Fun & Simulation

- [AnacondaKC/dsh-stock-market](https://github.com/AnacondaKC/dsh-stock-market) - A simulated stock market inside DSH — per the README, "effectively fixes the bug where your account can't lose money while you're writing code." Mock trading, zero real money. ★15

## 🧰 Related

- [taxueseek/argo](https://github.com/taxueseek/argo) - Agent search tool with multilingual coverage across finance, news, academic, code, shopping and more. Not stock-specific, but a handy general research companion. ★98

## Platform & Data-source Matrix

| Plugin | Markets | Data source / Platform | Trading | Credentials |
|---|---|---|---|---|
| dsh-longbridge | HK / US | Longbridge OpenAPI | ✅ (DSH approval gate) | Credential vault |
| dsh-ths-holdings | A-share | Tonghuashun ledger | ✗ (read-only) | Cookie → `ctx.credentials` |
| Awu12277/dsh-stock-watch | A-share | Tencent Finance | ✗ | — |
| 3930a/dsh-stock-watch | A-share | Eastmoney | ✗ | — |
| Bob-Bo1/dsh-stock-watch | A-share | Tencent Quotes | ✗ | — |
| Realyujie/dsh-us-stocks | US | yahoo-finance2 | ✗ | — |
| dsh-fun-ticker | Crypto/FX/A/HK/US | Binance/CoinGecko/Eastmoney/Sina/Frankfurter | ✗ | — |
| dsh-trading-terminal | A-share/Futures | Tencent/Sina/Eastmoney | ✗ | — |
| dsh-quant-data-mcp | A-share | Eastmoney/Tencent | ✗ | — |
| dsh-quant | Crypto/A/US | Binance/OKX/Bybit/Yahoo/Sina/Tencent/Tushare/AkShare | ✗ (simulation) | BYOK |
| dsh-trading (maddog) | US/Crypto | BYO CSV (ClickHouse/CCXT/brokers) | ✗ (risk-guard) | — |
| dsh-quant-workbench | A/US/Crypto | Sina/Eastmoney/Yahoo/Binance | ✗ | — |
| dsh-rigorquant | — | sympy/cvxpy (no feeds) | ✗ | — |
| dsh-trading-toolkit | A/US | Eastmoney | ✗ | — |
| dsh-quant-workspace | US | Yahoo Finance | ✗ | — |
| dsh-invest-research | A/HK/US | Eastmoney/Tencent | ✗ | — |
| hanai-investment-dsh | A-share | Eastmoney/Tencent/GuruFocus | ✗ | — |
| capital-generation | A-share | Wind/Tonghuashun/AkShare | ? | BYOK |
| dsh-finance (zhang787jun) | Accounting | — | ✗ | — |
| dsh-finance-plugins | Multi | Sina/Tencent/TTFund/CoinGecko/ECB/World Bank | ✗ | BYOK |
| dsh-finance-data | Multi | — | ✗ | — |
| fundpilot-dsh | OTC funds | Tushare/Eastmoney/Tencent | ✗ | BYOK |
| dsh-stock-market | Mock | Simulation | ✗ | — |
| argo | Web search | Multi-engine | ✗ | — |

## Safety Notes

- **Only 2 entries touch real accounts**: `dsh-longbridge` (order placement, gated by the DSH approval channel, keys in the credential vault) and `dsh-ths-holdings` (a login cookie in `ctx.credentials`). Everything else is read-only research or keyless public data.
- Most data-driven plugins are BYOK (bring your own key) — keys are stored via DSH credentials, never in the plugin repo.
- This list is a community index, **not** a security review. Audit the source before installing anything that touches money.

## Contributing

PRs welcome. Keep the format consistent:

```markdown
- [owner/repo](https://github.com/owner/repo) - One-line description of what it actually does (data source, markets, trading capability). ★stars · License
```

Requirements:

- Must be installable as a dsh plugin (`dsh plugin add` / `dsh.bundle` manifest) or an installable dsh profile/bundle — presets and skill packs are accepted but must be labeled as such.
- Must be finance/stock/quant related; skins must state whether they show real quotes or mock data.
- Include license, stars, and the data sources you verified. Don't guess — if you haven't verified a repo, don't list it.
- Suggestions welcome as issues.

## Disclaimer

Community-maintained index. Plugins belong to their authors; listing is not an endorsement and no safety, quality or maintenance guarantees are made. Installing a plugin runs third-party code on your machine — review the source and install at your own risk. Nothing here is financial advice. This project is not affiliated with DeepSeek.
