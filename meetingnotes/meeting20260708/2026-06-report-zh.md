# [报告] 准确性与可靠性工作组（ARWG）– 2026 年 6 月

> 译自 PR [#5](https://github.com/aaif/wg-accuracy-and-reliability/pull/5)（作者：Casper Nielsen），原文件 `reporting/2026-06-report.md`

**工作组：** WG Accuracy & Reliability（准确性与可靠性工作组）

**报告周期：** 2026 年 6 月

**主席：** Jordan Augé（Cisco）与 Casper Nielsen（Diagrid）

**提交日期：** 2026-06-29

---

## 摘要

- Charter 获批（5 月 15 日）后进入执行模式的第一个完整月份；GitHub 公开仓库已上线
- 三条并行工作线取得进展：
    - Taxonomy（术语）引导启动（词汇普查、分类、里程碑、跨工作组关系）
    - **D1**（准确性/可靠性词汇的架构性框架）
    - **D2**（基于企业角色与运营需求的应用型差距分析）
- **会议节奏：** 主全体会议每两周一次，与交付物工作会议（D2 优先）交替进行——不设独立的 Focus Group
- 已确定联络人候选：Taxonomy 工作组 3 人、Observability 工作组 1 人

## 目标进展

- **跨工作组 Taxonomy：** 跨工作组协作，共同贡献到单一 Google 文档
    - 内部工作跟踪仍保留在 running notes 中（见下文链接）
- **D1-ARWG-Taxonomy：** ARWG 首次交付涵盖：评估对象、准确性与可靠性、输出质量、可靠性维度、可观测性与归因、grounding（接地/事实依据）、症状、根因、评估生态、纠正机制
- **D1：** 结构化交付物，为术语提供架构性框架，梳理相关工作，并分析已确立的术语、以及存在矛盾、不精确和/或需要补齐的空白

### 差距分析与基准测试调研

- **负责人：** Sanjeev Suresh；首次交付物工作会议正在排期（与主全体会议隔周交替）
- 聚焦 B2B 企业场景；角色（persona）不限于开发者（还包括 PM、部署/运维、评估人员、数据科学家）
- 方法论遵循目录结构：角色 → 企业需求 → 基准测试全景 → 方案/工具差距 → 互操作性需求 → 差距综合 → D6 范围雏形
- 以生产系统中识别出的运营需求与差距为依据（grounding）
- 将驱动 D6 评估协议的范围界定
- 发布策略：
    - D1：宽泛/理论性的词汇框架
    - D2：应用型证据报告，回应 TC 对范围与实证依据（grounding）的关切

## 阻碍与风险

- **D2：** 实地证据——用例与角色需以社区真实需求为依据
    - 目前生产环境用例不足——数据覆盖面可能欠缺
- ARWG 范围较宽；用例种类繁多且需求差异很大。需在首批交付物中为成员创造最大价值

## 需要 TC 决策的事项

请确认 D2 的方法（聚焦 B2B 企业、多角色需求、与 D1 词汇挂钩的应用型差距分析、明确的工具/互操作差距、向 D6 交接）是否充分回应了 TC 对范围蔓延（scope creep）的关切——并确认将 D2 作为首批公开交付物发布是可接受的策略（D1 为理论框架，D2 为应用落地）。

## 下月重点

1. **D2（差距分析）：** 完成交付物的全部章节覆盖并指定各章节负责人；扩大活跃贡献者群体
1. **Taxonomy：** 向 Taxonomy 工作组的汇总文档贡献内容；确认联络人；定稿 D1 结构，随后跟踪术语演变
1. 基于交付物需求与术语开展跨工作组协作
1. **参与度：** 继续在每次同步会议上收集成员的个人目标；招募生产环境用例及工具/基准测试贡献者

## 指标 / 链接

- [Running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- 约 7-8 名活跃贡献者（且在增长）
- **D1（taxonomy）：** 完成 70%
    - **M1：** 41 个术语，其中 23 个仍需完善
    - [进展](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.hd16wsudjqjh#heading=h.3212hz242hul)
- **D2（差距分析）：** 完成 20%，目录已定稿
    - [进展](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.s0van0cuuukb)
