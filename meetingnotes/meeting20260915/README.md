# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-09-15
- **形式**: Zoom 线上会议（约 40 分钟，出席人数较少）
- **主持**: Jordan Augé

## 参会人

- Jordan Augé（Cisco，Chair，主持；次日启程赴阿姆斯特丹 AgentCon）
- Sanjeev Suresh（D2 survey 负责人）
- Matthew Khouzam（Ericsson，本组在 Taxonomy & Landscape 工作流的代表）
- Brian Malone

缺席：Casper Nielsen、Jessie Zhang（休假中，9 月 5 日起两周）、Robert Bischof（休假中）。

## 议题与结论

### 1. 开场分享：Taxonomy 术语编辑工具 & AgentCon

> **一句话总结**：Matthew 演示了自制的 Taxonomy Browser 网页工具——可查看已合并的术语、提议/编辑定义（可选让 AI 填充初稿）并一键生成 PR，commit message 会自动标注"AI 生成文本未修改的百分比"以便评审把关；Jordan 认为该工具大幅降低参与门槛，是拉动 D1 贡献的好抓手。

- 工具地址：https://matthewkhouzam.github.io/taxonomy-browser/ 。列表反映的是 taxonomy 仓库中**已合并**的内容；大量术语状态为 "definition pending"（大家同意该术语应该存在，但尚未就定义达成一致，如 "skill"）。
- 操作流程：Propose/Edit Term → 输入术语（自动带出已有定义）→ 手工修改或让不同 AI 填充 → Prepare PR。Prepare PR 有两种方式：走 GitHub API，或生成 bash 脚本（Matthew 更推荐后者，保留 human-in-the-loop）。
- AI 标注机制很朴素：对比 AI 生成字符串被改动的字符比例；100% 未改会提示"需额外评审"，改动达 70% 左右可视为作者确实读过。Brian 提醒不要因此否定 AI 本身的贡献价值，Matthew 同意（他自己用 Grok 生成了 "AI slop" 的定义）。
- 注意：Ericsson 内网屏蔽了该页面的 JavaScript，可能需用家庭网络访问。
- **AgentCon**：阿姆斯特丹场（本周末，约 2000 人）Jordan 及 Ericsson 欧洲同事参加；圣何塞场（下月）Matthew、Sanjeev 参加。

### 2. D2 Gap Analysis：Survey 收尾与推广

> **一句话总结**：Sanjeev 已处理全部反馈并补充欢迎/致谢文案，会上无人反对，**决定合并 PR #9**（后续修改走新 PR），正式发布前归档测试数据、另起干净副本；推广方面将制作 1 页 slide（含链接 + QR code）与邮件草稿，请 Manick 反馈后借 AgentCon 与邮件列表扩散，并考虑 10 月底办一次虚拟峰会。

- **PR 合并**：Matthew 提出流程问题——PR 挂了很久、大家都认为"够好但不完美"，是否拖慢了进度，建议先合并再打补丁；Sanjeev 与 Jordan 同意。Jordan 确立机制：**以双周例会为节拍合并进行中的 PR**——会前几天冻结、会上确认合并、有修改再迭代，最终可投票认定是否完成。会上举手表决无异议。
- **Merge 权限**：Matthew 提醒目前仅 TC 成员有 merge 权限；Jordan 会看能否给 Sanjeev 授权，否则请 Christina 协助。
- **Survey 现状**：目前约 6 份测试应答；Matthew 会中反馈"早退出路径缺少致谢页"，Sanjeev 将补上。合并后 Sanjeev 会把表单编辑权限分享给 Jordan、Matthew 及其他有兴趣者。
- **重复填写**：Jordan 问同一人参与多个项目能否填多份，Sanjeev 认为无法也无需限制——免费问卷能让人认真填一次已属不易，多多益善。
- **推广**：
  - Jordan 已在 chair 群里询问是否需要审批、能否在 plenary 上用 1 页 slide 推广；计划先在 AgentCon 各场口头/slide 宣传，再发邮件（大范围触达），并请 Manick 把关。
  - 文案要点：几行说明 gap analysis 交付物是什么、这是把工作落到具体问题的机会、征集最大痛点、结果将直接决定交付物内容与优先级。
  - Sanjeev 提议 10 月底办一场虚拟峰会（2-3 位 speaker），并可承诺"填问卷者可受邀参加与 leads 的结果早期讨论"作为激励；Jessie 回来后再一起敲定。
  - Sanjeev 询问基金会是否有 slide 模板/风格指南，Jordan 去确认。
- **Gap analysis 文档不等 survey**：两人一致认为可并行推进——文档已有部分章节初稿、部分为空，欢迎补充 bullet；Sanjeev 提醒领域变化太快，需重新审视几个月前的草稿及其结构是否仍然成立。Jordan 提出一个方向：按 agentic 应用生命周期（研发 → 上生产 → 基准测试 → 产品化）梳理**现有工具（尤其开源）的 landscape**，看它们如何覆盖需求（如用户满意度、human-in-the-loop），预期会清晰暴露碎片化与协议缺失；Sanjeev 建议最终文档 = landscape 分析 + 千人级 survey 的实践者反馈两部分。

### 3. D1 Taxonomy：评审节奏与优先术语

> **一句话总结**：GitHub issue 中的评论建议改为 PR 方式贡献，D1 将按双周合并、迭代版本；优先从"Accuracy & Reliability 的不同维度"章节入手，先定义 accuracy、reliability 本身再逐步细化，Jordan 会在纪要中列出优先术语清单。

- 后续每个 sprint 双周合并一次 D1 PR，评审后迭代。
- 术语提议应同时给出在交付物中相应部分的 rationale（不同词之间的辨析）。
- 借 Matthew 的工具降低门槛，争取更多贡献者。

### 4. 与其他工作组的 Liaison

> **一句话总结**：Jordan 原打算先积累度量指标等材料再启动跨组 liaison（如与 Observability），Matthew 反驳"先去听别人说什么反而更快校正自己的需求"，并推荐 Govind 主持的跨组半小时会议 "Security Circleback"（周一美东下午）作为切入点；决定征集志愿者代表本组参加，并在 I1 liaison 文档中记录交流内容。

- Circleback 名字不达意（Matthew 请 Jordan 向 TC 提议改名），实质是各工作组代表碰头找 common ground。Matthew 已以 Observability 身份参加，可兼顾 A&R 视角，但希望有更多本组代表；Casper 周一无法参加。
- Jordan 将收集会议详情放入 action points，并在下周一的 chair 会议上提出（本周一的 chair 会议多数人缺席）。
- Matthew 建议大家对感兴趣的其他组会议"带着爆米花去旁听"，回来即可带着已知方向做交付物。

### 5. Taxonomy 工作流的 "AI slop" 贡献问题与贡献指南

> **一句话总结**：Matthew 通报 Taxonomy 工作流正被一位（疑似非英语母语、澳洲时区）热心贡献者的大量 AI 生成内容"轰炸"——语法正确但句子自指、明显未经通读，评审极其耗神，呼吁各组成员就自己领域的术语帮忙评审；Sanjeev 提议制定贡献指南（用 AI 生成文本须自己读过），Matthew 支持并认为其他工作组已在推进此类政策，但不应一刀切拒绝 AI 内容。

- 该贡献者几乎向所有工作组都有提交，Matthew 相信其出于善意，正尝试联系对方。
- Brian 猜测可能是母语写作后机翻导致，Matthew 认可这是最善意的解释。

### 6. 其他事项（AOB）

> **一句话总结**：Matthew 推介两项 Eclipse 技术——Eclipse Enclave（类似 nono.sh，但用完整 VM 而非 Docker 沙箱化 agent，隔离性更强）与 Eclipse Theia AI（内置 agentic harness 的 IDE）；下次会议将做两项交付物的状态检查并启动"合并当前版本—迭代"流程，期望 AgentCon 曝光能带来新成员。

- Jordan 鼓励对现有 D1/D2 之外的主题有兴趣者提出新方向。

## 后续 Action

| Action | 负责人 |
|---|---|
| 合并 Survey PR #9；补早退出路径的致谢页；归档测试数据、另起正式表单；分享表单编辑权限 | Sanjeev |
| 确认 Sanjeev 的 merge 权限（否则请 Christina 协助） | Jordan |
| 制作 1 页 survey 推广 slide（链接 + QR code）；确认基金会 slide 模板/风格指南 | Sanjeev（slide）/ Jordan（模板） |
| 起草 survey 推广邮件，连同 slide 提交 Manick 反馈 | Jordan + Sanjeev |
| 在 AgentCon 阿姆斯特丹 / 圣何塞场推广 survey | Jordan / Sanjeev / Matthew |
| 规划 10 月底虚拟峰会（Jessie 回来后敲定） | Sanjeev + Jessie |
| 不等 survey，先行推进 gap analysis 文档：审视现有草稿结构，启动开源工具 landscape 梳理 | 全体（Jordan / Sanjeev 牵头） |
| 在纪要中列出 D1 优先术语（从 A&R 维度章节起），并在下周一 chair 会议征集评审 | Jordan |
| 使用 Taxonomy Browser 工具贡献/评审 D1 术语；帮助评审 taxonomy 工作流中的 AI 生成内容 | 全体 |
| 收集 Security Circleback 会议详情并征集本组志愿者代表；向 TC 建议改名 | Jordan |
| 在 I1 liaison 文档中记录跨组交流 | 全体 |
| 起草贡献指南（AI 辅助文本须经作者通读等基本要求） | Sanjeev |
| 按双周节拍合并 D1 / D2 进行中的 PR，下次会议做状态检查 | Jordan |

## 参考链接

- [Meeting agenda / running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- [Survey PR #9](https://github.com/aaif/wg-accuracy-and-reliability/pull/9)
- [Survey Google Form](https://docs.google.com/forms/d/e/1FAIpQLSfrKDDrqocQRByBLLetN-F4rYmZEmCi6iIgSKzqsT-KerKBAg/viewform)
- [D1 Taxonomy PR #8](https://github.com/aaif/wg-accuracy-and-reliability/pull/8)
- [Taxonomy Browser（Matthew 的术语编辑工具）](https://matthewkhouzam.github.io/taxonomy-browser/)
- [Taxonomy & Landscape 仓库](https://github.com/aaif/ws-taxonomy-landscape)
