# WG Accuracy and Reliability 会议纪要

- **日期**: 2026-08-04
- **形式**: Zoom 线上会议（约 40 分钟）
- **主持**: Casper Nielsen（Jordan 8 月 3-21 日休假）

## 参会人

- Casper Nielsen（主持/Chair）
- Sanjeev Suresh
- Jessie Zhang（Autodesk）
- Nicolas Bonnet
- Robert Bischof
- Anup Shirgaonkar（JPMorganChase）

## 议题与结论

### 1. Survey（调研问卷）提案评审

> **一句话总结**：Sanjeev 完成了问卷初稿（4 个部分、15 题）并以 PR 形式提交评审，会上逐节讲解了设计思路，请全员在 PR 上评论反馈；Nicolas 建议增加"组织如何管理 accuracy 生命周期"的问题。

- Sanjeev 讲解问卷结构：全卷锚定受访者"最近 6 个月内达到正式试点或部署的一个具体 agent 系统",共 4 部分 15 题：
  1. **入口与受访者画像**：参与过哪些活动（设计/决策等）、部署广度（试点→大规模）、应用领域（客服、研究、编码、创意等）;
  2. **总体采用与阻碍**（核心问题之一）：过去 6 个月哪些因素阻碍系统扩展——不限于 accuracy/reliability,还包括成本、工具可及性、安全/隐私/合规等,用 Likert 量表（1-5 分 + NA）评估,以了解 accuracy/reliability 相对其他因素的重要程度;另问最严重后果（延迟扩展→彻底放弃）、需要多少人工核查、系统带来的最大实际收益;
  3. **Accuracy & Reliability 专项**（核心问题之二）：过去 6 个月各类问题（结果错误、依赖变更导致失败、相似条件下结果不一致、该转人工时未转人工等,源自本组 taxonomy）对系统有用性的影响,Likert 量表;问题多久被提前发现、最严重后果、判断结果可接受性的主要证据来源（正式评估测试集 vs 非正式人工 vibe check）;
  4. **优先级**：哪些 accuracy/reliability 问题最需要业界共同投入（定义可接受质量、依赖变更后的回归检测等,深受 charter 影响）、期望工作组产出何种形式（术语、可复用测试、最佳实践报告）;最后开放题。
- 反馈方式讨论：Sanjeev 倾向 PR 评论;Jessie/Nicolas 认为 Google Docs 更易看到他人评论与讨论线索（Jessie 团队试过 PR 后又搬回 wiki,现用"wiki 讨论 + 自动化生成 PR 镜像"模式）;Casper 指出 GitHub 是工作组公开内容的权威所在,鼓励尽量在 Git 上讨论,复杂话题可开 GitHub Discussion。
- Nicolas 建议增加组织维度问题：公司内是否有专门的组织/团队管理 accuracy 评估与修复的生命周期（问责常常是弥散的）;他将起草一个具体问题与 Sanjeev 讨论。
- Jessie 反馈问卷偏长（多选题多、阅读负担重）,建议合并部分问题、补充受访者行业/公司规模等分析维度,并增加分支逻辑（无相关系统者直接跳到结尾——Sanjeev 确认设计上就是如此）。
- 定位澄清（答 Anup）：当前重心已从 gap analysis 转向 survey（因缺乏真实世界 grounding）,评审请优先关注 survey;survey 结果可支撑一份报告（类似 Sanjeev 上周在 Discord 分享的报告）,也可单独发布为 PDF 产物,gap analysis 是其后的独立工作;白皮书尚未启动,survey 将作为其数据输入。

### 2. 历史会议录像是否公开

> **一句话总结**：Chairs 会议提出"工作组转公开前的历史录像是否公开"的问题,因涉及当时以私密条件参会的所有成员,本次会议不做决定,请大家两周内反思并在 Discord 讨论;折中方案是用 AI 总结历史 transcript、经全员确认后公开摘要。

- 背景：工作组现已完全公开,新成员涌入,有其他工作组问及历史录像（录制于私密阶段）是否应公开;Chairs 会议未能达成一刀切结论,要求各组内部讨论。
- 需权衡公开收益与工作量;需要历史会议全体参会者的认可,而非简单多数。
- 折中选项：将历史 transcript 交给大模型生成浓缩摘要,经与会成员确认后公开摘要而非录像;也会参考其他工作组的做法,避免成为例外。
- 两周后的例会跟进,期间在 Discord 收集意见。

### 3. 其他事项

> **一句话总结**：提醒评审包括 Jordan D1 在内的共 3 个 open PR（Robert 发现 D1 文档章节与文件编号错位,Casper 将修正）;确定在 GitHub 建立公开的会议纪要 + to-do 流程（Jessie 认领自动化）;推进湾区线下 meetup 的筹备。

- **Open PRs**：仓库当前有 3 个 open PR（含 Jordan 休假前提交的 D1 文档 PR）,请大家评审。Robert 指出 D1 PR 中"第 4 章内容在第 3 个文件、反之亦然"的错位问题,评论易造成混淆;Casper 将与其在 Discord/Slack 对齐后修正。
- **会议纪要与 to-do 公开化**（Jessie 提议）：长期缺席后难以追赶进展,建议用 AI 汇总历史录像/transcript 生成摘要与带负责人的 to-do 清单;Casper 强烈支持——工作组已公开,本就需要发布公开会议摘要,计划在仓库建 meetings/summaries 目录,transcript 可从 LFX（app.lfx.dev）获取,摘要以 PR 提交,to-do 转为 GitHub issue 并用 GitHub handle 指派以保持问责;Jessie 认领（有现成自动化工具与云预算）。
- **湾区线下 meetup**：Casper 已向 AAIF（Monique）确认官方乐意协助推广（newsletter、征集讲者等）,需要成员提供场地;Sanjeev 已参与湾区本地组织者社区（曾协助上月 MCP party）,有场地人脉并与 MLOps 社区（Demetrios）相连,可负责场地与宣传,但需要帮忙找相关讲者;Jessie（Autodesk,旧金山 One Market 办公室）表示公司有预算,需明确 agenda 与受众价值即可申请场地;三人会后异步推进。
- **Observability WG liaison**：Jessie 此前报名担任联络人但找不到会议邀请;Casper 告知该组周三开会（太平洋时间上午 10 点）,可在 LFX 上报名;但页面仍显示"仅限邀请",与工作组已公开的认知矛盾,Casper 将跟进确认（临时方案：联系 Christy/AAIF support 获得邀请）。

## 后续 Action

| Action | 负责人 |
|---|---|
| 评审 survey PR 并留下评论（优先于 gap analysis） | 全体 |
| 起草"组织如何管理 accuracy 生命周期"的问题并与 Sanjeev 讨论 | Nicolas |
| 就问卷长度、问题合并、分支逻辑、分析维度提出具体修改意见 | Jessie |
| 反思"历史录像是否公开",在 Discord 讨论,两周后例会跟进 | 全体 |
| 评审其余 open PR（含 Jordan 的 D1 文档 PR） | 全体 |
| 修正 D1 PR 中章节与文件编号错位问题（与 Robert 在 Discord/Slack 对齐） | Casper |
| 用 AI 汇总历史会议 transcript,生成公开摘要与 to-do,以 PR 提交、issue 指派 | Jessie（Casper/Sanjeev 支持） |
| 跟进 LFX 上工作组"仅限邀请"状态问题;帮 Jessie 加入 Observability WG 例会 | Casper |
| 湾区 meetup：对接 Monique/AAIF,协调场地（Sanjeev/Autodesk）、讲者与宣传 | Casper + Sanjeev + Jessie |

## 参考链接

- [Meeting agenda / running notes](https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/edit?tab=t.0)
- [Survey proposal 讨论（Discord）](https://discord.com/channels/1461090924791595243/1463637013474578608/1534020941988892753)
