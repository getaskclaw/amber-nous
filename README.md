[English](README.en.md) · 简体中文

# amber-nous

> ⚠️ **更正（2026-10-02，另一项）**：防御轴的一案 A-d511f9e8 在所有车道上改记 NA（考场判的不是考生交付的文件，判分还要求了题面没写的事）。分母不变，**过案数不变**，每条道的总分都带 `'`。本仓各期成绩表里这一格请按 NA 读，其余内容保留原样，以[更正声明](https://github.com/getaskclaw/amber/blob/main/docs/corrections-2026-10-02-a-d511f9e8.md)为准。

> ⚠️ **更正（2026-10-02）**：以下考卷在作答时越出考卷、接触了判分材料，不计胜负。grok-4.7 @ Nous Portal 有 2 张卷（A-be92627f、A-a5608487）改记 NA，成绩 13/24 → **11'/24**；grok-4.7 @ CommandCode（未完赛，不定级）的 A-be92627f、A-a5608487 两格由 ✓ 改记 NA。原因是考场隔离缺陷，责任在我们。本页其余内容保留原样，以[更正声明](https://github.com/getaskclaw/amber/blob/main/docs/corrections-2026-10-02.md)为准。

用私有题库 **AMBER** 实测 Nous Portal（inference-api.nousresearch.com）在售模型，只公开结果，不公开题目。

> **一句话**：我们给 AI 模型出「真实工作考卷」——修 bug、查事故原因、看系统截图挑毛病、真上手运维——这个仓放 **Nous Portal 商店里模型**的成绩单。最新一期：Claude Haiku 5.5 考 24 案过 16 案（案 = 一道题），账单不到五美元，施工运维面接近满钉，但深度分析三案无一过线。

## 成绩一览

<!-- scoreboard:start -->

![amber-nous 成绩一览：claude-haiku-5.5、laguna-s-2.1 (Nous Portal) 逐轴过案数](results/assets/scoreboard.zh.png?v=20261009)

| 大类 | 轴 | 考什么 | claude-haiku-5.5 · [W41](results/2026-W41.md) | laguna-s-2.1 (Nous Portal) · [W41](results/2026-W41.md) |
|---|---|---|:-:|:-:|
| 施工面 | 编码 | 照着需求把功能写对 | 5/6 | 4/6 · 1 NA |
|  | 交付 | 做完还得交得出东西 | 3/3 | 3/3 |
|  | 运维 | 照规程干脏活 | 5/6 · 1 NA | 6/6 |
|  | 需求 | 客户要 A 不要 B | 0/1 | 1/1 |
|  | 收敛 | 真干完，不绕圈装忙 | 1/1 | 1/1 |
| 判断面 | UI | 照设计稿做页面 | 0/1 | 0/1 |
|  | 视觉 | 给真截图挑毛病 | 0/1 | 0/1 |
|  | 防御 | 堵死校验器的漏网口 | 0/2 · 1 NA | 0/2 · 2 NA |
|  | 归因 | 毛病对到正确根因 | 0/1 | 0/1 · 1 NA |
|  | 审查 | 给别人的交付物挑错 | 2/2 | 1/2 · 1 NA |
|  | **合计** |  | **16'/24** | **16'/24** |

- **都拿满**：交付、收敛。
- **都没过**：UI、视觉、防御、归因（一道都没过；NA 不算没过）。
- **有差别**（数字依次对应上表各列）：编码 5/6 对 4/6 · 1 NA、运维 5/6 · 1 NA 对 6/6、需求 0/1 对 1/1、审查 2/2 对 1/2 · 1 NA。

每格 = 过了几案/该轴共几案（案 = 一道计分题）。NA = 这一案作废或暂停计分，不算过也不算没过；总分带 `'` 表示其中有 NA。多数轴只有 1–2 案，差一案读数就变，所以别把小差距当结论。各列考试周次相同（W41），具体日期可能不同，数字是当期快照。

<!-- scoreboard:end -->

## 这是什么

- 每期一篇 `results/YYYY-Www.md`：同一套题、同一套考试程序（harness，自动让模型做题并记分的工具），对目标模型跑全库；同名模型跨厂商并排。
- 一期固定报告：题集规模与哈希（hash=防偷换题目的指纹）、每题（案）的 d2 分（我们的打分，算法不公开）与通过/失败、终端终态、token 用量与成本（按量计费的渠道如实报价）、时延、环境指纹、按证据纪律写的定性裁决。
- 题目、oracle（判分器）、transcript（答题全过程记录）、中间产物**永不公开**（见下「发布纪律」）。
- AMBER 是 agentic 实战题库（施工/运维/审查/视觉/需求漂移——题中要求中途变化），规范与制题工具见 [getaskclaw/amber](https://github.com/getaskclaw/amber)；考题本体私有。
- 「道」= 同一个模型名在不同家的卖场/接口（如 CommandCode 道、Nous Portal 道）；「effort 档」= 给模型设置的思考力度档位。跨仓比较时，同名模型在不同「道」上可能是不同端点，引用一律带日期与档位声明。

## 姐妹仓

[amber-commandcode](https://github.com/getaskclaw/amber-commandcode) · [amber-opencode](https://github.com/getaskclaw/amber-opencode) · [amber-deepseek](https://github.com/getaskclaw/amber-deepseek) · [amber-gpt](https://github.com/getaskclaw/amber-gpt) · [amber-crof](https://github.com/getaskclaw/amber-crof) · [amber-ollama](https://github.com/getaskclaw/amber-ollama) · [amber-devin](https://github.com/getaskclaw/amber-devin)

## 最新成绩

- **2026-W41** — anthropic/claude-haiku-5.5 全库首考 16'/24：[正刊](results/2026-W41.md)（[English](results/2026-W41.en.md)）
- **2026-W39** — x-ai/grok-4.7 全库首考 13/24（2026-10-02 裁定两卷作废，更正为 11'/24，见页首更正条）：[正刊](results/2026-W39.md)（[English](results/2026-W39.en.md)）· [图解版](docs/explainers/2026-W39-g47-plain.md)（[English](docs/explainers/2026-W39-g47-plain.en.md)）

![榜单构成](results/assets/2026-W41-composition.zh.png?v=20261009)

## 发布纪律（红线）

1. 只发：分数与聚合、token 用量与成本、速度、定性裁决。
2. 永不发：题目内容、oracle/判分器、transcript、考生工作区、任何能复原题面的中间产物。
3. 每期必钉：模型 ID、effort 档、日期（UTC）、harness 版本、每案内容哈希（bundle_sha）。哈希用于对照 [amber](https://github.com/getaskclaw/amber) 的公开哈希清单，自证题集未变。
4. 案号与题目结构属私有面：公开结果里案例只用稳定别名（A-xxxxxxxx，哈希派生）+ bundle 哈希作句柄；内部案号、变体名、题目描述永不出现。
5. 基调：这是社区实测，不是对厂商的攻击。数据说话，措辞克制。
