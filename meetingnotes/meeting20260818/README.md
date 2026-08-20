# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-08-18
- **形式**: Zoom 线上会议（正会约 20 分钟，会后留在线上继续讨论 survey 约 15 分钟）
- **主持**: Casper Nielsen（Jordan 8 月 3-21 日休假）

## 参会人

- Casper Nielsen（主持/Chair）
- Sanjeev Suresh
- Jessie Zhang（Autodesk）
- Matthew Khouzam（本组在 Taxonomy & Landscape 工作流的代表，兼任 Security and Trust Best Practices Guide 的 lead）
- Nicolas Bonnet
- Robert Bischof

## 议题与结论

### 1. Phase 2 交付物（D3 / D4）征集负责人

> **一句话总结**：正式启动 D3（Reliability-by-Design 最佳实践指南）与 D4（Agent Output Quality 标准）的志愿者征集，Sanjeev 愿意参与 D3（暂不牵头），Casper 将在 Discord 和邮件列表再次公开征集；Matthew 提出各工作组的 Best Practices Guide 最终应统一格式避免各自为政，Casper 将带到下次 Chair Sync 讨论。

- Casper 说明 gap analysis（Sanjeev 主导）之后的两项 Phase 2 交付物需要启动：
  - **D3. Reliability-by-Design Best Practices Guide（报告）**：将吸收 gap analysis 的输入；
  - **D4. Agent Output Quality Standard（规范）**：预计需要与 Observability & Traceability 工作组协作对齐。
- 征集方式宽松：举手、Discord、Slack 或邮件线程均可；中途发现精力不够可以随时退出（"不会被钉在钩子上"）。
- Sanjeev 表示愿意**参与** D3，但在 survey 工作收尾前暂不牵头；Matthew 以观察者身份加入 D3。
- Matthew（Security & Trust BP Guide 的 lead）提问：各组的最佳实践指南是否应尽早汇合？Casper 认为早期"厨子太多"会拖慢节奏，但后期必须收敛（至少统一文档结构/格式），将在下次 Co-chair & Chair Sync 上提出。
- Casper 将在 Discord 与邮件列表发出 D3/D4 的征集帖，欢迎更多 participants 和 leads。

### 2. Survey PR 状态与收敛计划

> **一句话总结**：Survey PR 已公示两周多，确定收敛时间表——Jessie 与 Sanjeev 本周四（8/20）11:00-12:00 PST 单独过评论，下周二例会同一时间做最后开放讨论，之后合并 PR 并推进发布；会上收集到问卷长度/UX、组织成熟度、发放渠道与激励等多方面反馈。

- **时间表**：Casper 推动收敛——给大家再一周时间完成评审；Sanjeev 与 Jessie 约定周四 11:00-12:00 PST 专门过 Jessie 的评论（她已提交一大批评论，涉及受访者背景信息缺失等）；下周二（与例会同时段）做一次开放的收尾讨论后合并。
- **Jessie 的反馈**：问卷缺少受访者画像信息（行业、公司/组织形态等）；策略上先把想问的都列全，再从 UX 角度裁剪、合并或改为注册时采集；坦言问题偏多、阅读量大。
- **Matthew 的反馈**（UX 角度）：信息量过载，要做减法；受访者可能刚被 observability/security/workflow 等多个组的 survey 轮番轰炸，存在**问卷疲劳**；建议考虑**随机化问卷**（每人随机抽 5 题的短问卷，靠样本量扩散拼出全貌）；此前建议的 Likert 量表 Sanjeev 已落实（两道大题已改造）。
- **Nicolas 的反馈**（组织成熟度，延续上次会议）：希望问卷能回答"公司组织上如何应对质量问题"——是否有**专门团队负责 accuracy/quality 生命周期管理**，还是问责分散；以及**谁是质量问题的决策者**（谁判定"这是质量问题、必须修"并排优先级）。Sanjeev 请他起草成具体问题，并提醒**问题预算有限**，新增需考虑替换掉哪题；Robert 建议这类问题可放入开头的 General 部分。
- **Robert 的反馈**：建议增加"活跃用户数"一类问题（5 个用户与 500 个用户的系统差异巨大），以反映公司与 agentic 方案的成熟度。
- **发放与激励**：大概率是免费问卷（无报酬），Jessie 提醒无激励时问卷必须短；渠道上计划请基金会 newsletter 收录（Sanjeev 认识运营者 Alex）、各工作组成员自填并转发、结合线下活动推广（如"参与问卷送下次活动门票"之类的激励）；Jessie 会去问 Autodesk 能否主办活动，也建议问问 Linux Foundation 有无小激励预算。

### 3. Taxonomy & Landscape 参与提醒

> **一句话总结**：Matthew 代表本组参加 Taxonomy & Landscape 工作流，昨日首轮评审"杀伐甚重"——本组提交的定义仅 4 条过关（每组第一轮上限 10 条）；工作底稿是 Google Sheets（链接在 Discord 的 ws-taxonomy-landscape 频道），请大家抽空补充高质量术语内容，Jessie 将对照其内部分类添加评论。

- Casper 提醒：taxonomy & landscape 工作流对所有人开放，尤其欢迎对术语命名提供输入。
- Matthew 通报：他曾把文档转成 150 条定义的 Excel 被"打回"（每组第一轮最多 10 条）；昨日评审后本组仅 4 条定义通过，但这只是 version 1，不必过虑。
- 目前工作在 Google Sheets 上进行（进 GitHub 前先在表格中打磨数据），链接在 Discord 的 ws-taxonomy-landscape 频道（Nicolas 会上贴出了链接）。
- Jessie 的内部分类近期有调整（大类从 7-8 个收敛为 4 个、其下挂更多细分定义），与工作组现稿有偏差，她将去术语章节补充评论，必要时与 Matthew 单独约会议（Matthew 因时区与日程原因倾向 Discord/Slack 异步沟通）。
- 本组在该工作流目前只有 Matthew 一名代表，欢迎更多人支援。

### 4. 其他事项

> **一句话总结**：会议纪要进 GitHub 的机制（上次会议 Jessie 提议）正在筹备中；各工作组普遍感到项目开始提速；Robert 8 月 21 日起休假 3 周，休假前会再完成一轮 taxonomy 文档评审。

- **会议纪要进 GitHub**：Casper 通报上次会议讨论的"将会议纪要转写并发布到 GitHub"事项正在推进中（in the making），虽未在 agenda 中显式跟踪，但在平行进行。
- **整体进展**：Casper 分享各工作组普遍反馈 traction 正在提升，首批交付物落地后有望进一步加速。
- **PTO**：Robert 8 月 21 日（周五）起休假 3 周，休假前将完成一轮 taxonomy 文档评审；Casper 请他把休假时间登记到 agenda 文档顶部的 PTO 清单（原 "Summer PTO" 改名为 "PTO"）。
- 正会约 20 分钟结束；Jessie、Sanjeev、Matthew、Nicolas、Robert 留在线上继续讨论 survey（Casper 提醒录制仍在进行，讨论内容见议题 2）。

## 后续 Action

| Action | 负责人 |
|---|---|
| 在 Discord 与邮件列表发布 D3/D4 志愿者征集 | Casper |
| 在下次 Chair Sync 提出"各组 Best Practices Guide 统一格式/协同"问题 | Casper |
| 参与 D3 的编写（gap analysis 收尾后） | Sanjeev（Matthew 为观察者） |
| 周四（8/20）11:00-12:00 PST 单独会议过 survey 评论；会前提交全部评论 | Sanjeev + Jessie |
| 下周二例会同一时段做 survey 最后开放讨论，之后合并 PR | 全体（Sanjeev 牵头） |
| 起草"组织是否有专门质量团队/谁决策质量问题"的具体问卷问题（注意问题预算） | Nicolas |
| 联系基金会 newsletter（Alex）收录 survey；探索活动等推广渠道 | Sanjeev |
| 询问 Autodesk 能否主办活动；了解 LF 有无问卷激励可能 | Jessie |
| 在 taxonomy Google Sheets 上按内部新分类补充术语评论 | Jessie |
| 休假前（8/21 前）完成一轮 taxonomy 文档评审；PTO 登记到 agenda | Robert |
| 抽空为 taxonomy & landscape 术语表补充内容 | 全体 |

## 参考链接

- [Meeting agenda / running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- [Survey PR #9](https://github.com/aaif/wg-accuracy-and-reliability/pull/9)
- [Taxonomy & Landscape 仓库](https://github.com/aaif/ws-taxonomy-landscape)
