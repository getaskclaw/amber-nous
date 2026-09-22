# amber-nous

用私有题库 **AMBER** 实测 Nous Portal（inference-api.nousresearch.com）在售模型，只公开结果，不公开题目。
English: [README.en.md](README.en.md)

## 这是什么

- 每期一篇 `results/YYYY-Www.md`：同题、同 harness，对目标模型跑全库；同名模型跨厂商并排。
- 一期固定报告：题集规模与哈希、每案 d2 分与通过/失败、终端终态、token 用量与成本（按量道实价）、时延、环境指纹、按证据纪律写的定性裁决。
- 题目、oracle、transcript、中间产物**永不公开**（见下「发布纪律」）。
- 姐妹仓：[amber-commandcode](https://github.com/getaskclaw/amber-commandcode)（CommandCode 道）、[amber-opencode](https://github.com/getaskclaw/amber-opencode)（OpenCode Go 道）、[amber-deepseek](https://github.com/getaskclaw/amber-deepseek)、[amber-gpt](https://github.com/getaskclaw/amber-gpt)、[amber-crof](https://github.com/getaskclaw/amber-crof)、[amber-ollama](https://github.com/getaskclaw/amber-ollama)、[amber-devin](https://github.com/getaskclaw/amber-devin)。本仓的对照轴是**同名模型跨厂商对决**——同一个模型名在 Nous Portal / CommandCode / xAI 官方道上可能是不同端点，跨仓引用一律带日期与档位声明。
- AMBER 是 agentic 实战题库（施工/运维/审查/视觉/需求漂移），规范与制题工具见 [getaskclaw/amber](https://github.com/getaskclaw/amber)；考题本体私有。

## 发布纪律（红线）

1. 只发：分数与聚合、token 用量与成本、速度、定性裁决。
2. 永不发：题目内容、oracle/判分器、transcript、考生工作区、任何能复原题面的中间产物。
3. 每期必钉：模型 ID、effort 档、日期（UTC）、harness 版本、每案内容哈希（bundle_sha）。哈希用于对照 [amber](https://github.com/getaskclaw/amber) 的公开哈希清单，自证题集未变。
4. 案号与题目结构属私有面：公开结果里案例只用稳定别名（A-xxxxxxxx，哈希派生）+ bundle 哈希作句柄；内部案号、变体名、题目描述永不出现。
5. 基调：这是社区实测，不是对厂商的攻击。数据说话，措辞克制。
