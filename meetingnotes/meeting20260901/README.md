# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-09-01
- **形式**: Zoom 线上会议（约 58 分钟）
- **主持**: Jordan Augé（休假归来）

## 参会人

- Jordan Augé（Cisco，Chair，主持）
- Casper Nielsen（Diagrid，Chair）
- Sanjeev Suresh（D2 survey 负责人，9:40 PT 提前离会）
- Jessie Zhang（Autodesk）
- Nicolas Bonnet（Autodesk）
- Matthew Khouzam（Ericsson，本组在 Taxonomy & Landscape 工作流的代表）
- Brian Malone

## 议题与结论

### 1. 开场分享：AgentCon / MCPCon 参会情况

> **一句话总结**：摸底工作组成员的 AgentCon 参会计划——Jordan 及 Cisco 同事去 9 月阿姆斯特丹场，Sanjeev、Matthew、Jessie 去 10 月 22 日圣何塞场；Matthew 将请 Discord 管理员为两场会议各建一个频道，方便线下碰面，Jordan 也会在频道里 ping 一下。

- Jordan 去阿姆斯特丹（9 月），Sanjeev 与 Matthew 去圣何塞（10 月 22 日），Jessie 原本报了 10 月的另一场 "The AI Conference"（Pier 48），也会尽量去圣何塞场。
- Sanjeev 建议：若要办 Accuracy & Reliability 的推广活动，可考虑作为 AgentCon 的 side event（见议题 2）。
- Matthew 会请 Discord 管理员为两场会议分别建频道，方便成员互相知道谁去哪场。

### 2. D2 Gap Analysis：Survey 现场试做与反馈

> **一句话总结**：会上现场试做 Google Form 版问卷收集实时反馈，确认本周内完成组内评审后合并 PR #9，随后在组内先跑一轮采样再迭代；目标回收 >1000 份（预留低质量应答的剔除空间）；发放渠道包括 TC（Jordan 已在 7 月报告中提出）、Security WG 的 "Checklist" 机制（Govind）、基金会 newsletter、以及自办 meetup / 虚拟峰会等。

- **现状与时间表**：Sanjeev 已把 survey 做成 Google Form 原型（链接贴在聊天区），邀请大家会中花 10 分钟实际填一遍，重点看"难不难、能否拿到想要的信号"——Sanjeev 自评复杂度偏高，免费问卷要求 10 分钟专注作答有风险。本周内完成组内评审，周末停止收集评论并合并 PR；Jessie 已获 form 编辑权限，可直接做小幅措辞/顺序调整。原型表单收到的测试数据（含 Matthew 的多次测试）作废，正式发布时另起新表单。
- **跨组评审**：Sanjeev 提出不清楚 survey 需不需要在 leads / 跨工作组层面评审。Matthew 建议借助 Security WG 由 Govind 推动的 "Checklist" 机制（防止各组重复造轮子），Govind 是把 survey 快速推给所有人的最佳盟友。Jordan 计划在下周一的 WG chair 会议上分享（Matthew 提醒周一是北美 Labor Day，可能延期）。
- **目标样本量与发放渠道**：
  - Sanjeev 提出 500，Jessie 认为应更大（约 1000+），因为会有 10-20% 的人快速乱填需剔除；Matthew 补充 20 题量表用标准差等基础统计即可轻松识别乱填的应答。
  - Jordan 昨日向 TC 提交了 7 月报告，其中请 TC 协助发放 survey（TC 联系人 David Suryapara），预计本周内有回复，结果会同步到 Discord。
  - Sanjeev 与 Bay Area 的 AAIF 组织者相熟（过去两月协助办了 2 场 MCP meetup），可协助找场地办小型 meetup；Jessie 正在联系 OpenAI / Anthropic 的朋友作为 speaker。
  - 基金会 newsletter 也是渠道，但 Sanjeev 担心问卷过重、真正填完的人不多。
- **问卷设计反馈**：
  - Jessie：AI 成熟度不能只看公司规模，可从其他题推断；量表方向（most→least 还是 least→most）不统一导致找答案费时，需重排选项；正式发布前先在组内跑一轮拿样本数据做分析，看数据能否用、缺什么，再迭代。
  - Nicolas（以问卷设计者视角）：应先想清楚"拿到答案后要做什么"，部分选项彼此过于接近、无法区分；前半部分与 Accuracy & Reliability 关联感弱，建议题目措辞中反复锚定 "accuracy / reliability" 术语。Sanjeev 解释结构：前 4-5 题受访者背景，接着 3-4 题问最大痛点（A&R 是其中之二），**第 9 题起**才是 A&R 专题；第 1 题是唯一的退出题（仅二手经验或只做过 demo 的受访者直接退出）。
  - 反馈渠道：结构化反馈统一留在 PR #9（提新题请给出题目+选项，并说明替换掉哪题以控制题量），发散性讨论可到 Discord；Matthew 提议的 GitHub issue 方式未被采纳。
- **匿名性**：为回应 Matthew "受访者会说谎"的担忧，Jessie 与 Jordan 确认问卷应明确承诺匿名，如需分析组织类型则在结果中脱敏。

### 3. 讨论：用户维度（user dimension）与 Accuracy & Reliability

> **一句话总结**：Nicolas 分享 Autodesk 内部用户行为分析——面对同样不完美的系统，"韧性"用户会持续尝试、另一部分用户直接放弃，提出 reliability 不应只看系统属性、也要看用户交互维度；Casper（世代差异）、Jordan（"效用 utility" 概念，类比网络领域的告警疲劳）均表示认同，一致同意纳入 D2 白皮书及后续交付物。

- Nicolas 的观察：同一系统同一属性下，不同用户对不准确/不可靠的反应差异巨大，agent 需要具备"感知用户希望如何交互"的能力；因为 AI 系统可以把用户上下文回填到 prompt 中，这在确定性系统里做不到。
- Casper：Gen Z 与他这一代对 AI 的预期截然不同，系统是输入驱动的，用户人群会深刻影响系统行为，值得纳入但尚不知如何编码。
- Jordan：以内部 CI/CD 网络变更评审 agent 为例，即使不完全准确、能提前告警仍有"效用"，但误报过多会造成告警疲劳——不需要 100% 准确也能有用，建议用 utility 把系统指标映射到用户价值，并在多个交付物中考虑并度量。
- Jessie：taxonomy 中已有情感/行为分析相关定义，白皮书中可进一步展开。
- Sanjeev 顺带分享他将担任欧洲 "Who Verifies the Agent" workshop 的 PC 成员审稿。

### 4. 讨论：性能与成本维度

> **一句话总结**：Jessie 提出成本与性能（延迟）是企业落地 AI 的重大约束，建议纳入考量；Matthew 建议同时参与 Observability & Traceability WG（他正推动"为什么测、测性能与成本"）；Sanjeev 预期 survey 中成本会是排名最高的因素，未来工作可定义为"在成本约束下的 A&R"；Matthew 提醒问卷中涉及成本的措辞要避免让受访者"为面子说谎"，Nicolas 建议改问"公司有哪些成本控制手段"。

- Jessie：Autodesk 在 AI 与模型上开支巨大，因安全合规需经过代理路由，推理延迟也偏高；不知有无工作组在看性能与成本。
- Matthew：建议加入 Observability WG；成本会成为大话题。
- Nicolas：算力成本应与问题复杂度匹配（简单问题用开源权重模型即可）；Sanjeev 补充可推荐 smart routing 类标准，Discord 上近日也有人提及。
- Jessie 还提到正在给 agent 加 harness、缓存、语义检索等基础手段以降低成本与延迟，询问是否有工作组在做 harness 标准；Sanjeev 提到基金会内的开源 harness 是 Goose（支持本地推理）。

### 5. D1 Taxonomy 进展与评审机制

> **一句话总结**：D1 以 PR #8 为最新版本，Jordan 提议"1-2 周一个评审周期、每次会议合并当前版本再开新一轮"的迭代机制，首轮先评目录（ToC）再聚焦术语；但鉴于反馈量低，决定 survey 收尾后再向大家征集 D1 反馈，先聚焦约 15 个优先术语贡献给 Taxonomy & Landscape 工作流。

- Jordan：希望 survey 结束后的一周征集 D1 反馈，优先挑约 15 个术语做小范围评审并贡献到工作流，完整交付物作第二轮评审。
- 评审流程：PR 是最新版本，在 PR 上评论；每 1-2 周合并一次、清理评论、开新一轮。
- D2 gap analysis 文档在 survey 期间可暂缓或等待贡献；同时继续征集 D3 / D4 志愿者（延续上次会议）。
- Jessie 提议 survey 之后应开始规划白皮书大纲，她休假归来后启动。

### 6. 其他事项（AOB）

> **一句话总结**：Matthew 提议每次会议固定加一个 "AI 业界新闻对 A&R 的影响" 环节（如 OpenAI 与 Cursor 分道、模型随意变更），引发关于"基准测试移动目标"（Nicolas）、harness 版本不可控（Jordan）、开源/蒸馏模型与数据主权（Jessie、Matthew）的讨论；Matthew 将分享其 CC-BY-SA 的 AI 全景 slide deck。

- Nicolas：底层模型版本频繁变化使基准测试成为"追移动目标"，一侧进步一侧回归，规划极难，对终端用户影响巨大。
- Jordan：Claude Code 之类 harness 也一样，用户对版本更新无感知、无控制；Observability WG 目前仍在"基础原语"阶段（Matthew）。
- Jessie：关注可蒸馏的开源模型（本地/自托管），既省钱又便于控制；Matthew 提到瑞典新建数据中心大量采购 GPU，说明业界在转向开源模型以获得数据主权。
- Jordan 鼓励把讨论延续到 Discord 保持频道活跃，会后发布纪要与 action points；考虑下周加一次临时会议同步 survey。
- **PTO**：Jessie 自 9 月 5 日（周五）起休假两周。

## 后续 Action

| Action | 负责人 |
|---|---|
| 本周内在 PR #9 完成 survey 评审（建议实际填一遍 Google Form 再评论），周末合并 | 全体（Sanjeev 牵头） |
| 合并后在组内先跑一轮 survey 采样，分析数据可用性后迭代；正式发布另起新表单 | Sanjeev + Jessie |
| 周四上午 Sanjeev 与 Jessie 单独同步 survey（Jessie 休假前） | Sanjeev + Jessie |
| 对 survey 做一遍通读 + 逐题结构化反馈，提交到 PR #9；措辞上锚定 A&R 术语 | Nicolas |
| 跟进 TC（David Suryapara）关于协助发放 survey 的回复，同步到 Discord | Jordan |
| 在下周一 WG chair 会议分享 survey（注意北美 Labor Day 可能延期） | Jordan |
| 联系 Govind，借 Security WG 的 Checklist 机制跨组推广 survey | Sanjeev / Matthew |
| 探索 Bay Area meetup / AgentCon side event 作为 survey 推广渠道 | Sanjeev + Jessie |
| 请 Discord 管理员为 AgentCon 阿姆斯特丹 / 圣何塞两场各建频道 | Matthew |
| 分享 AI 全景 slide deck（CC-BY-SA） | Matthew |
| survey 收尾后征集 D1 反馈，挑约 15 个优先术语做首轮评审 | Jordan |
| 休假归来后启动白皮书大纲 | Jessie |
| 将"用户维度/效用"与"成本约束"纳入 D2 及后续交付物考量 | 全体 |
| 会后发布纪要与 action points；评估下周是否加临时会议 | Jordan |

## 参考链接

- [Meeting agenda / running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- [Survey PR #9](https://github.com/aaif/wg-accuracy-and-reliability/pull/9)
- [Survey Google Form（原型）](https://docs.google.com/forms/d/e/1FAIpQLSfrKDDrqocQRByBLLetN-F4rYmZEmCi6iIgSKzqsT-KerKBAg/viewform)
- [D1 Taxonomy PR #8](https://github.com/aaif/wg-accuracy-and-reliability/pull/8)
