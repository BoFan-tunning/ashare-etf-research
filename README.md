# 🚀 A-share ETF Research Skill for Antigravity

[![Impact Poster](assets/poster.png)](assets/poster.png)

## 🌟 简介 (Introduction)

**Ashare-ETF-Research** 是一款专为 Antigravity 框架设计的 A 股个股及 ETF 深度研究与分析 Skill。它旨在将宏观经济的宏大叙事与微观的资金博弈相结合，通过 AI 引擎为用户提供科学、客观且具有实战参考价值的投资研报。

该项目不仅是一个功能性的研究工具，更是通过 **「算法综合 (Algorithmic Synthesis)」** 视觉哲学，将金融数据的精密性与投资建议的艺术性完美融合。

---

## 🔥 核心功能 (Core Features)

- **🔭 宏观深度扫描 (Macro Insight)**：自动抓取并分析 CPI、PPI、LPR、PMI 等核心宏观指标，判断大盘底色。
- **📊 资金实时博弈 (Capital Flow)**：监控主力资金动态、北向资金流入及融资融券余额，洞察筹码博弈。
- **📈 行业趋势领航 (Sector Scan)**：基于政策面与券商最新研报，识别当前市场最具爆发潜力的板块。
- **📝 结构化报告产出 (Auto Reporting)**：一键生成结构清晰、逻辑严密的 Markdown 格式投研报告。

---

## 🛠️ 安装与使用 (Setup & Usage)

### 1. 安装 (Installation)
将本仓库中的 `.agent/` 目录合并到你的 Antigravity 工作区根目录中：

```bash
# 结构预览
.agent/
├── workflows/
│   └── ashare-etf-research.md             # 场景逻辑
└── resources/
    └── ashare-etf-research/
        ├── assets/
        │   └── report_template.md         # [关键] 报告美化模板
        └── references/
            └── macro_guide.md             # [关键] 宏观研判逻辑指南
```

> **注意**：请确保整个 `.agent` 目录完整拷贝，缺失 `resources` 会导致无法生成格式化的研报。

### 2. 使用 (Usage)
在对话窗口中触发：
- **主动触发**：发送 `/ashare-etf-research` 启动工作流。
- **自然对话**：直接提问 *"帮我分析下 510300 近期的基本面"* 或 *"今天的大盘趋势怎么看？"*

---

## 🎨 视觉美学 (Aesthetics & Design)

本项目高度重视视觉表达。我们认为，卓越的工具应当拥有匹配其能力的审美。

- **设计哲学**：详见 [docs/design-philosophy.md](docs/design-philosophy.md)。
- **海报生成**：本项目包含一个自动化的海报生成工具 `scripts/generate_poster.py`，它通过 Python 代码将数据流与光影美学结合，生成的宣传海报直接位于 `assets/` 目录。

---

## ⚖️ 免责声明 (Disclaimer)

*本 Skill 生成的所有分析报告及结论仅供学术研究参考，不构成任何形式的投资建议。股市有风险，入市需谨慎。*

---

**Developed with ❤️ by Antigravity Intelligence**
