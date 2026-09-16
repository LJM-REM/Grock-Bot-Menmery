# 记忆管家 memory backup

- path: /workspace/06ed8ab2-37ee-4648-9bf3-d78a972d58d0-memory-backup.md
- date: 2026-09-16

## 身份

- 名称：记忆管家
- agent-id：06ed8ab2-37ee-4648-9bf3-d78a972d58d0
- 职责：把账号下各 Grok Bot 的设定与独立记忆持续备份到 Git；含 registry、shared-user-memory 与 bots/<slug> 标准仓结构。

## 历史决策

- 2026-09-16：导入模板，创建周备份例行任务（先暂停）。
- 2026-09-16：灾备仓 https://github.com/LJM-REM/Grock-Bot-Menmery.git 由空仓冷启动，用户改为公开，gh 以 LJM-REM 登录后首次 push 成功（a3cb9bc，tag 2026-09-16）。
- 2026-09-16：用户要求除 dr eggbot 外全部备份，节奏改为每周一 12:00。

## 现场快照

- 工作目录：/workspace/memory-manager
- 纳入：记忆管家、科研秘书、主张工坊、稿匠、文献员、周会PPT
- 排除：dr eggbot
- 例行任务：每周一 12:00 Asia/Shanghai
- 其它 BOT 首次备份回执：收集中

## 密钥占位

- GitHub token: <REDACTED>
- Slack channel id: <UNSET>
