# 记忆管家 memory backup

- 备份时间：2026-09-21 12:10 Asia/Shanghai
- 请求方：记忆管家（周一例行灾备）
- path: /workspace/06ed8ab2-37ee-4648-9bf3-d78a972d58d0-memory-backup.md
- 覆盖写：是
- 重建方式：SendToAgent 不可用；自 live profile + 既有 MEMORY/archive + 本管家 durable facts 重建

## 1. 身份

- 名称：记忆管家
- uuid / agent-id：06ed8ab2-37ee-4648-9bf3-d78a972d58d0
- serverId（profile.json）：3517469
- 职责：把账号下各 Grok Bot 的设定与独立记忆持续备份到 Git；含 registry、shared-user-memory 与 bots/<slug> 标准仓结构；支持冷启动/恢复/接入舰队与定时查漏补缺。
- 时区：Asia/Shanghai
- 工作目录：/workspace/memory-manager
- Remote：https://github.com/LJM-REM/Grock-Bot-Menmery.git
- 用户：REM；偏好中文回复
- 队友（纳入）：科研秘书、主张工坊、稿匠、文献员、周会PPT
- 排除：dr eggbot（serverId 3469760 / uuid 0195067d-8589-4394-8b32-cc2b51ff55ca）— 永不纳入
- 节奏：每周一 12:00 Asia/Shanghai；手动口令「存档」
- Slack channel id：未配置（<UNSET>）

## 2. 历史决策

- 2026-09-16：导入模板，创建周备份例行任务（先暂停）。
- 2026-09-16：灾备仓由空仓冷启动；用户改为公开；gh 以 LJM-REM 登录后首次 push 成功（commit a3cb9bc，tag 2026-09-16）。
- 2026-09-16：用户要求除 dr eggbot 外全部备份；节奏改为每周一 12:00；registry 更新（f68bea3）；五业务 BOT 首次全量归档（c6505cb）。
- 2026-09-16：纳入名单固定——记忆管家、科研秘书、主张工坊、稿匠、文献员、周会PPT；排除 dr eggbot。
- 2026-09-21：周一例行全量；本 harness 无 SendToAgent，改为从磁盘 live 源 + 先验 archive 重建快照（不向各 BOT 发备份请求、不等回执）。

## 3. 现场快照

- 工作树：/workspace/memory-manager（branch main，此前与 origin/main 同步）
- 已有 tag：2026-09-16；待写 tag：2026-09-21
- 纳入 6 BOT；排除 dr eggbot 仍为「否」
- 科研侧自 09-16 以来进展（供查漏）：主张 C 仍锁定；PathBench 入实验平台候选；FlexPath 写入方法叙事近邻；cards 增至约 20 张；daily 有 09-16/17/18/21；weekly 有 W38+W39；library.bib 约 229 行
- 周会PPT 侧：已有 利进铭_9月17日汇报.pptx 与 2026-09-17-周会.pptx
- 本轮动作：覆盖写 6 份 workspace backup → 刷新 bots/*/MEMORY.md、agent-spec、profile → shared-user-memory → meta → registry → CHANGELOG → secret scan → commit + tag + push

## 4. 密钥占位

- GitHub credential / gh auth：<REDACTED>（平台侧已登录 LJM-REM，不写入明文）
- Slack channel id：<UNSET>
- 其它 API / session：<NONE_IN_THIS_FILE>
- 禁止项确认：本文件无明文密钥或会话凭证

