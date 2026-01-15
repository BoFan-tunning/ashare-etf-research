---
name: ashare-etf-research
description: A-share stock and ETF research and analysis skill. Use this to analyze specific stocks/ETFs or the general A-share market based on macro data and news.
---

# A-share 股票与 ETF 研究分析指南

本工作流旨在通过网络搜索和宏观数据分析，为用户提供 A 股个股、ETF 或整体市场的投资分析结论（看空/看平/看涨）。

## 使用步骤

### 第一步：识别搜索目标
判断用户请求中是否包含明确的个股（如：贵州茅台、600519）或 ETF（如：沪深300ETF、510300）。

- **如果包含个股/ETF**：跳转至 **[场景 A：特定标的研究]**。
- **如果不包含明确标的**：跳转至 **[场景 B：整体市场分析]**。

---

### 场景 A：特定标的研究
针对指定的个股或 ETF 进行深度扫描。

1. **信息收集**：
   使用 `search_web` 工具搜索以下关键词：
   - `[个股/ETF名称] 近期行业政策`
   - `[个股/ETF名称] 资金流向` (关注北向资金、主力资金、融资融券)
   - `[个股/ETF名称] 最新资讯/研报`

2. **内容分析**：
   - **政策面**：是否有行业利好（如产业补贴）或利空（如监管收紧）。
   - **资金面**：近期是持续流入还是大量净流出。
   - **消息面**：是否有关键财报发布、重组、定增或突发新闻。

3. **输出报告**：
   参考 `g:\stock\ptrade策略\.agent\resources\ashare-etf-research\assets\report_template.md` 的结构，生成一份详尽的 Markdown 格式分析报告。
   **关键要求**：
   - 使用 `write_to_file` 工具将报告保存至工作区根目录，文件名为 `{标的代码/名称}_分析报告_{YYYYMMDD}.md`。
   - 使用 Markdown 语法增强可读性，加粗核心结论。
   - 在聊天窗口中简要告知用户文件已生成并提供文件路径。

---

### 场景 B：整体市场分析
当用户未提供具体标的时，基于宏观经济数据判断大盘趋势。

1. **宏观数据收集**：
   参考 `g:\stock\ptrade策略\.agent\resources\ashare-etf-research\references\macro_guide.md`，使用 `search_web` 搜索最新数据：
   - `中国 贷款市场报价利率 LPR 变化`
   - `中国 CPI PPI 最新通胀数据`
   - `全社会用电量 最新统计`
   - `中国 GDP 增长率/PMI 数据`
   - `中国 外贸出口及社会消费品零售总额`

2. **趋势判断**：
   基于上述数据进行综合研判：
   - 如果 LPR 下行、用电量和消费增长，通常偏向**看涨**。
   - 如果 PPI 持续低迷、通胀受阻或出口受挫，通常偏向**看空或看平**。

3. **输出报告**：
   参考 `g:\stock\ptrade策略\.agent\resources\ashare-etf-research\assets\report_template.md` 的结构，生成一份宏观趋势报告。
   **关键要求**：
   - 使用 `write_to_file` 工具将报告保存至工作区根目录，文件名为 `A股市场整体趋势报告_{YYYYMMDD}.md`。
   - 详细覆盖利率、通胀、用电量、GDP/PMI、外贸消费等核心指标。
   - 在聊天窗口中简要告知用户文件已生成并提供文件路径。

---

## 报告规范
- **格式**：必须输出为结构化的 Markdown 文档。
- **语气**：专业、客观、基于事实。
- **时效性**：必须优先参考当月或最近一个季度的最新数据。
- **美观性**：适当使用引用块 (blockquote) 和列表 (bullets) 来组织信息，使其看起来像一份专业的投研报告。
- **风险提示**：在结论末尾附带：*“本分析仅供参考，不构成投资建议。股市有风险，入市需谨慎。”*
