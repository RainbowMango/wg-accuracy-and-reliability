# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-05-26
- **形式**: Zoom 线上会议

## 参会人

- Jordan Augé（主持/Chair）
- Matthew Khouzam（Ericsson）
- Sanjeev Suresh
- Jessie Zhang（Autodesk）
- Daniel King
- Vellaichamy, Sivapriya
- Pradyumna Singh

## 议题与结论

### 1. Charter 获批，进入执行阶段
- 工作组 Charter 已于 5 月 15 日由 TC（技术委员会）批准，工作组正式进入执行模式。
- Charter 及历次修订、评论、投票记录均在 GitHub 仓库中，GitHub 将作为最新资料的权威来源；日常工作可先用 running notes，成熟后迁移到 GitHub 以 PR 方式协作。

### 2. 工作流/交付物组织模式（Focus Group 讨论）
- Matthew 提出担忧：Focus Group 过多可能导致过度碎片化（Discord 频道已激增，超过 20 个频道后大家会失去关注）。
- 现场投票后达成共识：不再拆分过多子会议/频道，采用混合模式——共用一个 Discord 频道 + 按需组织临时(ad hoc)会议，主例会作为进展同步中心。
- 各工作流负责人可自行决定具体协作方式，Chair（Jordan/Casper）负责协调。

### 3. Gap Analysis（差距分析与准确性基准调研，D3 类交付物）
- Sanjeev 展示了周末起草的初稿：核心是一个覆盖矩阵（coverage matrix），按维度（准确性标准、上下文正确性、动作正确性与副作用等）评估 component 级、agent 级（单/多 agent）、operational 级证据的覆盖情况及未验证部分，并附基准测试目录（benchmark catalog）。
- 结论：方向获得认可，Sanjeev 将文档合并到主运行文档中，并由 Sanjeev 牵头该工作流。
- 目标：在夏休（7-8 月）前完成第一版，9 月恢复工作后推进最终版。

### 4. Taxonomy 与 Landscape（术语与全景图）
- 新的 Taxonomy & Landscape 工作组已成立（Chair：Junjie 和 Gala），每两周周一开会，通过 GitHub 上的 YAML 文件管理术语并自动生成浏览门户。
- 这是当前最紧迫的交付物；各工作组以小批量（batch）方式贡献：内部讨论 → 会议评审 → 向该工作组提交 PR。
- Matthew 自荐担任所有工作组的 taxonomy 联络人（liaison），重点避免术语重复与冲突（防止"巴别塔"）；Casper 继续牵头 D1 术语文档。

### 5. Agentic 系统中的准确性与可靠性（D4）
- 确认 Gap Analysis 是 D4 的前置条件，但不妨碍先收集想法与笔记。
- 计划下次会议开始收集 D4 相关的想法。

## 后续 Action

| Action | 负责人 |
|---|---|
| 在 Discord 建 thread，协调 Gap Analysis 贡献者，未来两周推进初稿 | Sanjeev（牵头），Jessie、Matthew、Sivapriya 参与 |
| 将 Gap Analysis 草稿合并到主运行文档并共享链接 | Sanjeev |
| 担任跨工作组 taxonomy liaison，协调术语贡献、避免重复冲突 | Matthew |
| 牵头 D1 术语文档，与 taxonomy 工作组对接 | Casper |
| 更新 Charter/文档中的负责人名单，协调会议安排（经 AAF） | Jordan |
| 阅读 Taxonomy & Landscape 工作组的 GitHub 仓库与贡献指南 | 全体 |
| 评审 Sanjeev 的 Gap Analysis 草稿并提供反馈（评论需署名） | 全体 |
| 确认可进一步认领的贡献项 | Jessie |
