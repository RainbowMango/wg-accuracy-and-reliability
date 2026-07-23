# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-07-21
- **形式**: Zoom 线上会议（约 47 分钟）

## 参会人

- Jordan Augé（主持/Chair，Cisco）
- Sanjeev Suresh
- Matthew Khouzam（Ericsson）
- Brian Malone
- Jeff Borek
- Vellaichamy, Sivapriya
- Pavan Sudheendra（Observability 工作组）

## 议题与结论

### 1. 一般性更新
- 夏休（PTO）提醒：Jordan 与 Casper 交替休假，例会暑期继续（前提是有足够人参加）；昨日 Chairs 会议出席人数已明显减少。
- Jordan 在 Chairs 会议上确认：AAIF 支持工作组开展 survey（问卷调研），后续可联系 Kristina 协调对外传播；是否有官方问卷工具尚待确认。
- Matthew 提醒 Discord 上有 AAIF Technical Excellence Awards 的项目提名流程（该轮提名截止日已过——上周五）；Jordan 补充当日收到的 Pulse 调查中也包含项目提名相关问题，后续可能还有其他轮次。

### 2. D3（Gap Analysis）与调研问卷
- Sanjeev 回顾背景：最初的 agent/benchmark gap analysis 因缺乏真实企业问题的 grounding 而转向先做 survey，目标是了解业界 agent 采用现状、并识别 accuracy/reliability 方面的优先差距，以支撑后续交付物。现有草稿已获 Robert 反馈，希望更多成员参与评审。
- 关于协作方式：Chairs 会议反馈各工作组普遍存在工具问题（GitHub、Google Doc 均有人不适应），有问题请及时向 Chairs 反馈；各子组可自行选择合适的协作方式。
- Matthew 建议：给评审设定 deadline、并在文档中加入"What's in it for me"（评审对评审者的价值）以提升参与度——大家都在以低优先级碎片时间评审。
- Sivapriya 建议先定一个"锚点"（最终目标）：例如以白皮书/会议论文/AAIF 博客报告为产出目标反推时间计划；Jordan 说明 survey 的定位是为交付物提供真实用例与使用情况的输入，结果预计落入交付物的章节。
- Brian 分享问卷设计经验：与其罗列问题，不如**陈述期望的成果（outcomes）**（如"更准确的 agentic 工作流""更详细的错误信息"等），让受访者评估"对组织的重要性"与"当前解决程度"，两者的差距（gap）加上简单的数学处理即可揭示应优先关注的成果，并可据此产出白皮书。
- Matthew 提出问卷 UX 改进：避免单题 10+ 选项，改用 Likert 量表并拆分为更小的问题；会上他现场展示了将现有问卷重排为 Likert 矩阵格式的新版本（已发 Discord），可自动导入 Google Forms，统一答案顺序与矩阵形态以降低受访者认知负担，也便于后续用 Excel 分析。Sanjeev 认可，并表示还要进一步精简待评分条目。
- 问卷范围：倾向先锚定本工作组（跨工作组问卷难以兼顾各组需求，Observability 是最接近的），完成后再放到更大范围评审。
- 发放工具：Pulse 使用外部工具，LFX 中有 survey 功能但非所有人可访问；若要面向更广受众（如通过 newsletter/邮件征集），Google Forms 更合适。Jordan 将向 Kristina 确认工具与许可问题。
- Jordan 提出一个待思考的问题：假设拿到问卷答案，聚合结果对 AAIF 成员的价值有多大、能否真正解决交付物目前的困境（如用例分组：autonomous agents vs copilots、受访者所处的采用/部署阶段等），需要提前设想清楚。
- **结论（deadline）**：问卷内部评审期约一个月——下次例会迭代一版，再下次例会（第二次会议）前定稿，为休假成员留出参与时间。

### 3. Taxonomy（术语）与 D1 进展
- 两条并行工作线：① 向 Taxonomy & Landscape 工作组维护的跨组 Excel 表贡献术语（Matthew 从本组提取的定义已录入）；② 本组自己的术语优先级（Jordan 已在文档中建议了优先定义的核心概念）。
- 评审方式：在 Excel 表中新增以自己名字命名的列填写意见；即使同意也请标注"agree"，以留下评审与共识的痕迹。
- 跨组 taxonomy 现状（Matthew）：每组最多贡献约 10 条术语（总上限 70 条）；他在积极推动将本组核心术语（如 hallucination）升级为 universal 通用术语以争取更多名额。当前进展缓慢（约每周达成一条定义共识），目前正在辩论"什么是 agent"（甚至衍生到"如何定义狗不算 AI agent"）。
- Taxonomy 工作组例会：每周一 11:30-12:30（美东时间）；希望每个工作组有约 3 名参与者，目前本组主要是 Matthew（Casper 因时区冲突退出）；Sivapriya 有意加入，Jordan 会后联系 Junji 安排邀请。
- 分工共识：通用术语交由跨组共同定义避免重复劳动；Accuracy/Reliability 维度等本组特有术语由本组负责定义并贡献到主文档。
- D1 交付物：Jordan 将把长期放在 Google Docs 的 work-in-progress 交付物转为 GitHub PR 方式迭代，会后分享 PR 链接。
- Liaison（与 Observability 工作组）：Jordan 上周起草了工作组间 liaison 文档的初始问题清单；Pavan（Observability 组）表示会审阅，指出双方在 metrics 定义、agent 失败识别/评估等方面与其组正在开发的更广泛 agent 评估模型高度重叠，后续协调合作。

### 4. 其他分享
- Matthew 分享了他近几周开发的一个开源项目：以"极致可观测性"评估本地开源模型的观测准确性（observed accuracy），桥接 accuracy 与 observability；链接已发会议聊天区，请勿在其正式公布结果前对外传播。
- Matthew 还提到可以用 Gemini 从 Markdown 自动生成 Google Forms 表单，他将尝试用该方式生成问卷表单，避免手工录入。

## 后续 Action

| Action | 负责人 |
|---|---|
| 确定 survey 截止时间：约 1 个月（下下次例会前定稿） | Chairs |
| 确认 survey 发放工具（LFX/外部工具/Google Forms）及许可 | Jordan（联系 Kristina） |
| 将 survey 整理为 PR 提交；在此之前继续在 Google Doc/Discord 收集评论 | Sanjeev |
| 按 Brian 的 outcome-gap 框架与 Matthew 的 Likert 格式修改问卷、精简条目 | Sanjeev + Matthew |
| 用 Markdown 自动生成 Google Forms 问卷表单 | Matthew |
| 分享 D1 交付物的 GitHub PR 链接 | Jordan |
| 离线评审 taxonomy Excel 表（优先 M1/核心术语，加自己名字列评论，同意也标注） | 全体 |
| 联系 Junji 为 Sivapriya 安排加入 Taxonomy 工作组例会 | Jordan |
| 评审 Observability liaison 文档并补充问题 | Pavan + 全体 |
| 夏休前目标：完成 Accuracy/Reliability 最重要的约 10 条术语定义 | 全体 |

## 参考链接

- [Meeting agenda / running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- [跨工作组 Taxonomy Excel 表](https://docs.google.com/spreadsheets/d/1Oa-x7nBISIOuqaC-BnsQ1R-iPdwZ6Otk3dpWlqpI_z4/edit?gid=0#gid=0)
- [google-form-from-markdown-file](https://github.com/sverch/google-form-from-markdown-file/)（Markdown 生成 Google Forms 工具）
