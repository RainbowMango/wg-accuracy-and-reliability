# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-07-07
- **形式**: Zoom 线上会议

## 参会人

- Jordan Augé（主持/Chair）
- Sanjeev Suresh
- Matthew Khouzam（Ericsson）
- Jessie Zhang（Autodesk）
- Nicolas Bonnet（Autodesk）
- Brian Malone
- Jeff Borek
- Vellaichamy, Sivapriya
- Jeffin Varghese
- Pradyumna Singh / David（列席）

## 议题与结论

### 1. 一般性更新
- 已完成对 TC（技术委员会）的首次月度报告（PR 模板方式，每月最后一天提交，TC 有 sponsor 负责评审指导）。
- 夏休（PTO）安排：Jordan 与 Casper 错开休假，例会暑期继续，视出席情况调整。
- Jordan 起草了内部交付物初稿"与其他工作组的 Liaison/依赖地图"，列出可能交互的工作组及输入/输出，欢迎离线评论。

### 2. Taxonomy（术语）进展
- Jordan 已向跨工作组文档提交术语 PR，并按三个 Milestone 对术语分类，M1（加粗）为需优先评审的基础术语，每两周迭代一个版本，目标夏休前后完成 M1。
- Matthew 将术语从 150+ 条精简至约 30 条，整理为跨工作组共享的 Excel 表（含 observability、security 等各组 sheet 及 universal 通用术语），作为向 taxonomy 网站提交 Markdown PR 前的 triage 中间步骤。
- Brian 提出可维护性担忧（260+ 术语持续变动），建议尽早确定 taxonomy 管理流程（定期 PR + 变更评审、保留定义出处）；最终由 markdown/静态网站（Junjie @ Google 维护）承载。
- 讨论明确：本工作组不评估模型本身的准确性/可靠性（模型评估超出范围），但 agent、agentic 等基础术语仍需定义。

### 3. Gap Analysis（D3）与调研问卷
- 上周小组会议后认识到 Gap Analysis 需更贴近真实企业场景，Casper 建议通过 survey（问卷调研）收集实践者的用例与痛点作为 grounding。
- Sanjeev 分享了 AI Engineering Report 2026（Amplify 等出品，1000 名从业者调研）：模型选型考量中 accuracy/quality 第一，cost 进入前三且排在 reliability 之前；并展示了自拟的问卷草稿（15-20 题：画像、构建的 agent 系统、投产障碍、故障模式、评估监控方式等）。
- 结论：问卷方向获认可，倾向面向跨工作组甚至更广范围发放；挑战是控制题量并说明数据用途。决策机制按 AAIF 建议——限期评论后由会议中活跃成员表决，不追求全员共识。
- Matthew 建议双问卷方案：对外发布的 5 题轻量随机版（广泛传播）+ 内部完整版。
- Nicolas 强调 accuracy/reliability 必须结合用例（"教我做" vs "替我做"）与风险等级分析，建议问卷采用该用例分类框架。
- Matthew 指出 AAIF 各工作组均未覆盖 safety，本组最接近，需向上反馈；Jeff Borek 补充"价值（value）证明"是第三大关注点。
- D3 暂不设硬性截止时间：Jordan 表示需先有足够的参与和内容贡献，才能为各章节指定负责人并设定期限；夏休前目标是完善目录与已有内容。
- Jessie 对方向多变、责任不清表示困惑；明确当前优先级：taxonomy 第一，其次 survey，然后 gap analysis。

### 4. 外部动态
- 湾区 AAIF MCP launch party 将于 28 日举行（与 MCP 大版本发布同期），链接后续在 Discord 分享（Sanjeev）。
- Matthew 提议每次例会末尾固定加入"外部世界动态"环节（如 MCP attestations 等），获认可。

## 后续 Action

| Action | 负责人 |
|---|---|
| 评审 taxonomy Excel 表：查看 M1 优先术语，挑选词条评论/点赞（同意也请标注），可建议删词 | 全体 |
| 在会议纪要中分享新的 taxonomy Excel 表链接 | Jordan |
| 评审 survey 问卷草稿并补充问题；下周二左右组织一次离线讨论并在 Discord 协调 | Sanjeev + 全体 |
| 与 AAIF 确认对外（跨工作组/公开）发放问卷的方式 | Jordan / Casper（Chairs） |
| 评审 Liaison/依赖地图初稿并补充意见 | 全体 |
| 在 Discord 分享各自加入工作组想解决的核心问题/期望产出 | 全体 |
| MCP launch party 链接发布后在 Discord 分享 | Sanjeev |
| 向 AAIF 反馈 safety 议题无工作组覆盖的问题 | Matthew / Chairs |
| 贡献用户侧 accuracy/reliability 用例视角的内容 | Jessie |
