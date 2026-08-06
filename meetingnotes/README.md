# 会议纪要（Meeting Notes）

本目录存放 AAIF **Accuracy & Reliability 工作组**双周例会的中文会议纪要,由 AI agent（GitHub Copilot CLI）根据会议 transcript 与 agenda 自动整理生成。

## 目录结构

```
meetingnotes/
└── meetingYYYYMMDD/
    ├── README.md                                  # 中文会议纪要
    ├── GMTYYYYMMDD-HHMMSS_Recording.transcript.vtt  # 会议原始 transcript
    └── (可选) 会议中分享的报告、图片等附属材料
```

## 生成方法

完整工作流与 prompt 维护在私有仓库 **`RainbowMango/agent-ops`** 的
`projects/wg-accuracy-and-reliability.md` 中,概要如下:

1. **获取 agenda**:从工作组 running notes Google Doc 导出纯文本,
   搜索对应日期的章节:
   ```bash
   curl -sL "https://docs.google.com/document/d/13HPunOtlGkU0eBH8LRAEzaioVnrYXDd7-ylkOjPGI6Y/export?format=txt"
   ```
2. **获取 transcript**:用 `agent-ops/scripts/lfx_transcript.py` 自动登录
   LFX（openprofile.dev）下载会议 VTT:
   ```bash
   OP_EMAIL=<邮箱> OP_PWD=<密码> python3 lfx_transcript.py 2026-08-04 "Accuracy" out.vtt
   ```
   （凭据用后即焚,不落盘、不提交。）
3. **生成纪要**:AI 通读 transcript 并对照 agenda,按固定格式撰写中文纪要。
4. **提交**:放入 `meetingnotes/meetingYYYYMMDD/`,push 到本 fork 的
   `meetingnotes` 分支。

## 纪要格式约定

1. 标题 + 日期 + 形式（Zoom 线上会议,标注时长/主持人）
2. **参会人**:从 transcript 发言人提取,标注公司/角色
3. **议题与结论**:按 agenda 分节,每节开头一句话总结
   （`> **一句话总结**：讨论了xxx，决定了xxx`,便于向上汇报）
4. **后续 Action 表**（Action | 负责人）
5. **参考链接**

## 注意事项

- transcript 是口语稿,人名可能拼错或乱码,需与 agenda 交叉核对。
- 会议中注明"请勿外传"的内容,纪要中保留保密提醒。
- 生成后建议人工复核一遍再引用。
