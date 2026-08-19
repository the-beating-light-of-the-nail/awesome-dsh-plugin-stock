# Awesome DSH 股票与金融插件精选 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English](README.md) | 中文

> 一个专注于 **股票 / 金融 / 量化** 的 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）插件垂直精选列表。

DeepSeek Harness 是 DeepSeek 开源的 agent harness，一切皆插件，社区产出极快。通用目录收录"大而全"——找股票插件要跨分类翻半天；这份列表只收录**交易、行情数据、量化研究、投研分析、券商接入**相关插件，一站式直达。

每条目都对照 README 实际验证过（功能、安装方式、数据源、是否触及实盘交易），按真实功能分层，不按名字归类。

> [!WARNING]
> 安装插件等于在你自己机器上以你的权限运行第三方代码。出现在本列表**不是**安全背书——安装前请审代码。触及真实券商账户或凭据的插件已显式标注。

## 目录

- [📊 行情数据与盯盘](#-行情数据与盯盘)
- [🎨 交易终端与看盘皮肤](#-交易终端与看盘皮肤)
- [🔬 量化研究](#-量化研究)
- [💼 投研与财务分析](#-投研与财务分析)
- [🏦 券商接入与账户](#-券商接入与账户)
- [🎮 整活与模拟](#-整活与模拟)
- [🧰 相关工具](#-相关工具)
- [平台与数据源矩阵](#平台与数据源矩阵)
- [安全提示](#安全提示)
- [收录标准](#收录标准)
- [免责声明](#免责声明)

## 📊 行情数据与盯盘

- [Awu12277/dsh-stock-watch](https://github.com/Awu12277/dsh-stock-watch) - A股自选股实时行情盯盘插件：DSH Web 右上角可折叠弹窗，分组自选、分时/日/周/月 K 线、买卖目标价提醒。★50 · 腾讯财经 · MIT
- [3930a/dsh-stock-watch](https://github.com/3930a/dsh-stock-watch) - A股常驻行情带：输入框下方随读带（3 秒刷新、涨红跌绿、自选股增删）+ `/stock/*` 数据路由，与本地 watchlist.json 双向同步。★2 · 东方财富 · MIT
- [Bob-Bo1/dsh-stock-watch](https://github.com/Bob-Bo1/dsh-stock-watch) - A股持仓/自选观察：侧边栏底部入口，读取本地 holdings.json 显示实时行情与持仓盈亏。README 明确不执行买卖操作。★1 · 腾讯行情 · MIT
- [Realyujie/dsh-us-stocks](https://github.com/Realyujie/dsh-us-stocks) - 美股数据工具插件：为 agent 提供 quote/history/financials/analyst/news/ownership 六个结构化工具（含浏览器端蜡烛图渲染）。★5 · yahoo-finance2 · MIT
- [omdsh-dev/dsh-fun-ticker](https://github.com/omdsh-dev/dsh-fun-ticker) - 行情跑马灯插件：会话底部常驻横向跑马灯，加密/汇率/A股/指数/港美股任意组合，免 key 数据源。★4 · Binance/CoinGecko/东方财富/新浪/Frankfurter
- [Hermit503/dsh-trading-terminal](https://github.com/Hermit503/dsh-trading-terminal) - A股+国内期货盯盘终端：自选/涨跌幅榜/涨跌停池/热搜/板块排行/31 个期货主力合约 K 线 + AI 基本面技术面分析。纯看盘无实盘下单。★1 · 腾讯/新浪/东方财富 · MIT
- [helibeiqi/dsh-quant-data-mcp](https://github.com/helibeiqi/dsh-quant-data-mcp) - A股数据 MCP：零依赖 stdio server 模板 + 开箱示例，日线 OHLCV/实时快照/财务指标/北向资金/板块 6 个工具。★0 · 东方财富/腾讯 · MIT

## 🎨 交易终端与看盘皮肤

- [linhut/dsh-stock-terminal](https://github.com/linhut/dsh-stock-terminal) - 股市行情皮肤+功能插件：全局交易终端视觉 + 实时行情面板（自选跑马灯、拼音模糊搜索、持仓盈亏、指数快照、K线弹窗），覆盖 A股/港股/美股/加密/外汇。★2 · Apache-2.0（README 声明，元数据 NOASSERTION）
- [renat3u/tonghuashun-webui](https://github.com/renat3u/tonghuashun-webui) - 同花顺风格 DSH 终端式皮肤。⚠️ "K线"画的是 **Token 消耗量与代码变更**——本地模拟数据，非真实行情。★10
- [AdamPlatin123/dsh-tonghuashun](https://github.com/AdamPlatin123/dsh-tonghuashun) - 同花顺行情终端皮肤（ui-skin-ths）+ 代码量 K 线面板（ui-market）。⚠️ K 线展示代码变更量，非真实行情。★2 · MIT

## 🔬 量化研究

- [pengpengyi92/dsh-quant](https://github.com/pengpengyi92/dsh-quant) - dsh 原生量化工具包（npm 包，46 个 `quant_*` 工具/6 域）：数据→指标→因子→回测→风险→执行模拟的端到端 PDAT→PET 研究管线，另有 UI/CLI。★12 · 加密/A股/美股 · Binance/OKX/Bybit/Yahoo/新浪/腾讯 + 15 通道知识库（含 Tushare/AkShare）· MIT
- [maddogfinance/dsh-trading](https://github.com/maddogfinance/dsh-trading) - 交易研究工作台插件集（5 个 npm 包）：类型化行情数据接缝、CSV provider 模板、确定性指标库、交互式 K 线卡片 + `risk-guard` 预执行门禁。硬边界：只研究不下单。★6 · 美股/加密 · 自带 CSV（可接 ClickHouse/CCXT/券商 API）· MIT
- [dmsobtl/dsh-quant-workbench](https://github.com/dmsobtl/dsh-quant-workbench) - 量化研究工作台 profile 包：组合 market-data/backtest/vision-router/session-analyst 四插件 + 3 个预置 skill（动量扫描/策略回测/加密分析）。★1 · A股/美股/加密 · 新浪/东方财富/Yahoo/Binance
- [linxichen/dsh-rigorquant](https://github.com/linxichen/dsh-rigorquant) - 实证/计算金融数学研究框架（agent preset + skills + 角色路由）：上下文隔离的多 agent 研究实验室，组合构建/优化、仿真、经济金融计算，含证据元验证器。★2 · sympy/cvxpy 计算环境（无行情源）· MIT
- [kentleenot/dsh-trading-toolkit](https://github.com/kentleenot/dsh-trading-toolkit) - A股+美股行情/K线/ADX 三状态信号/简易多空回测工具包；作者实盘策略以只读教学形式开放，永不下单。★0 · 东方财富 · MIT
- [AllenCX/dsh-quant-workspace](https://github.com/AllenCX/dsh-quant-workspace) - 自包含量化研究工作区：内置 Python 引擎拉 Yahoo 日线、单标的信号卡/规则回测/健康复查、交互式 HTML 图表、策略注册表，只读设计。★0 · Yahoo Finance · MIT

## 💼 投研与财务分析

- [eclipti/dsh-invest-research](https://github.com/eclipti/dsh-invest-research) - A股全链路投研：一条命令跑完行情快照→巴菲特七维价值评分→风险扫描→机构共识→保守 DCF 估值五层，输出结构化研报。★0 · 东方财富（腾讯备用）· MIT
- [hancao97/hanai-investment-dsh](https://github.com/hancao97/hanai-investment-dsh) - 本地优先 A股价值研究工作台（独立 profile，React 全屏产品 + DSH runtime）：市场仪表盘/自选/4 个投资人 agent 大师研判/版本化报告/报告后追问。★3 · 东方财富/腾讯/GuruFocus · MIT
- [v587d/capital-generation](https://github.com/v587d/capital-generation) - 面向中国股市小散户的金融投资智能体（Python + MCP，dsh bundle 安装）。BYOK：Wind/同花顺免费 Key + AKShare 兜底。· Apache-2.0
- [zhang787jun/dsh-finance](https://github.com/zhang787jun/dsh-finance) - 财务与会计工作流插件（Anthropic Finance 的 DSH 改编）：8 个技能覆盖日记账/对账/财务报表/差异分析/关账/SOX 测试/审计 + 5 个校验工具。不代记账、不代做投资决策。★4 · MIT（含 Apache-2.0 派生部分）
- [hanjixin/dsh-finance-plugins](https://github.com/hanjixin/dsh-finance-plugins) - 19 个金融插件套件（`@hanjixin/dsh-tool-*`）：A股/美股行情、外汇、量化指标、风控、组合分析、加密货币、基金净值、宏观等数据工具 + DSH Market 展示前端；可选 Tushare/Wind/Choice/聚宽。★1 · 新浪/腾讯/天天基金/CoinGecko/欧央行/世界银行
- [coder-wu/dsh-finance-data](https://github.com/coder-wu/dsh-finance-data) - 增量收集金融数据工具。★1 · MIT

## 🏦 券商接入与账户

> ⚠️ 这两个插件触及真实账户或凭据，安装前务必审代码。

- [omdsh-dev/dsh-longbridge](https://github.com/omdsh-dev/dsh-longbridge) - 长桥 Longbridge 港美股接入：行情快照/K线/指数/自选 **+ 账户资金/持仓 + 下单撤单**——交易工具强制走 DSH 审批通道，App Key/Secret/Access Token 只存 DSH 凭据保险箱。★4 · 长桥 OpenAPI · BSD-3-Clause
- [PM25000/dsh-ths-holdings](https://github.com/PM25000/dsh-ths-holdings) - 同花顺持仓盈亏悬浮卡片：读取真实持仓自动显示今日盈亏/上证指数/分时图，20 秒轮询（只读展示，无交易）；需粘贴同花顺登录 Cookie 存于 `ctx.credentials`。★1 · 同花顺投资账本 · MIT
- [dyc-code/fundpilot-dsh](https://github.com/dyc-code/fundpilot-dsh) - 个人场外基金组合只读分析：CSV 持仓导入→可审计账本→正式净值→确定性收益计算→日终确认报告，DSH 工具 + Web UI；明确不执行任何申购/赎回/交易。★0 · Tushare 主/东方财富/腾讯证券

## 🎮 整活与模拟

- [AnacondaKC/dsh-stock-market](https://github.com/AnacondaKC/dsh-stock-market) - DSH 里的模拟股票市场——按 README 原话："有效解决了写代码的时候账户不能同时亏钱的 BUG"。模拟交易，不碰真钱。★15

## 🧰 相关工具

- [taxueseek/argo](https://github.com/taxueseek/argo) - agent 搜索工具：多语言覆盖金融/新闻/学术/代码/购物等 8 个领域。非股票专属，但做研究时的趁手搭档。★98

## 平台与数据源矩阵

| 插件 | 市场 | 数据源/平台 | 实盘交易 | 凭据 |
|---|---|---|---|---|
| dsh-longbridge | 港/美股 | 长桥 OpenAPI | ✅（DSH 审批门禁） | 凭据保险箱 |
| dsh-ths-holdings | A股 | 同花顺投资账本 | ✗（只读） | Cookie→ctx.credentials |
| Awu12277/dsh-stock-watch | A股 | 腾讯财经 | ✗ | 无 |
| 3930a/dsh-stock-watch | A股 | 东方财富 | ✗ | 无 |
| Bob-Bo1/dsh-stock-watch | A股 | 腾讯行情 | ✗ | 无 |
| Realyujie/dsh-us-stocks | 美股 | yahoo-finance2 | ✗ | 无 |
| dsh-fun-ticker | 加密/汇/A/港/美 | Binance/CoinGecko/东方财富/新浪/Frankfurter | ✗ | 无 |
| dsh-trading-terminal | A股/期货 | 腾讯/新浪/东方财富 | ✗ | 无 |
| dsh-quant-data-mcp | A股 | 东方财富/腾讯 | ✗ | 无 |
| dsh-quant | 加密/A股/美股 | Binance/OKX/Bybit/Yahoo/新浪/腾讯/Tushare/AkShare | ✗（模拟） | BYOK |
| dsh-trading（maddog） | 美股/加密 | 自带 CSV（ClickHouse/CCXT/券商） | ✗（risk-guard 门禁） | 无 |
| dsh-quant-workbench | A/美/加密 | 新浪/东方财富/Yahoo/Binance | ✗ | 无 |
| dsh-rigorquant | — | sympy/cvxpy（无行情源） | ✗ | 无 |
| dsh-trading-toolkit | A/美 | 东方财富 | ✗ | 无 |
| dsh-quant-workspace | 美股 | Yahoo Finance | ✗ | 无 |
| dsh-invest-research | A/港/美 | 东方财富/腾讯 | ✗ | 无 |
| hanai-investment-dsh | A股 | 东方财富/腾讯/GuruFocus | ✗ | 无 |
| capital-generation | A股 | Wind/同花顺/AKShare | ? | BYOK |
| dsh-finance（zhang787jun） | 财务 | — | ✗ | 无 |
| dsh-finance-plugins | 多市场 | 新浪/腾讯/天天基金/CoinGecko/欧央行/世界银行 | ✗ | BYOK |
| dsh-finance-data | 多市场 | — | ✗ | 无 |
| fundpilot-dsh | 场外基金 | Tushare/东方财富/腾讯 | ✗ | BYOK |
| dsh-stock-market | 模拟 | 模拟盘 | ✗ | 无 |
| argo | 全网搜索 | 多引擎 | ✗ | 无 |

## 安全提示

- **只有 2 个条目触及真实账户**：`dsh-longbridge`（可下单，强制走 DSH 审批通道，密钥在凭据保险箱）与 `dsh-ths-holdings`（登录 Cookie 存于 ctx.credentials）。其余全部是只读研究或免 key 公共数据。
- 多数数据型插件是 BYOK（自带 Key），Key 存 DSH credentials，不入插件仓库。
- 本列表是社区索引，**不是**安全审查。凡是碰钱的插件，装之前先审计源码。

## 收录标准

欢迎 PR。保持条目格式一致：

```markdown
- [owner/repo](https://github.com/owner/repo) - 一句话真实功能（数据源、市场、是否交易）。★stars · License
```

要求：

- 可用 `dsh plugin add` / `dsh.bundle` manifest 安装，或是可安装的 dsh profile/bundle；preset 与 skill 包可收录但必须如实标注。
- 必须金融/股票/量化相关；皮肤类必须注明是真实行情还是模拟数据。
- 附 license、star 数和经你验证的数据源。没验证过的仓库不要列，别猜。
- 建议也可以直接开 issue。

## 免责声明

社区维护索引。插件归各自作者所有；收录不等于背书，不对任何插件的安全性、质量或维护性做保证。安装插件会在你的机器上运行第三方代码——请自行审阅源码并自负风险。本列表不构成任何投资建议。本项目与 DeepSeek 无关。
