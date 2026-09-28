# 变更记录

## 2026-09-16

- 冷启动：仓 `LJM-REM/Grock-Bot-Menmery` 当时为空且已改为公开。
- 写入标准目录：README、RESTORE、CHANGELOG、registry、shared-user-memory、meta、bots/ji-yi-guan-jia。
- GitHub 写入凭据当时尚未登录，首次推送可能只完成本地 commit。

## 2026-09-16（纳入名单与节奏）

- 用户决定：除 dr eggbot 外全部纳入备份。
- 例行任务改为每周一 12:00（Asia/Shanghai）并启用。
- 向科研秘书、主张工坊、稿匠、文献员、周会PPT 发出首次备份请求。

## 2026-09-16（首次业务 BOT 全量）

- 归档科研秘书、主张工坊、稿匠、文献员、周会PPT 的首次 MEMORY。
- 密钥扫描：未发现明文 token。
- 主张工坊与文献员文件已写好，回执稍后或未单独发。

## 2026-09-21（周一例行全量）

- 例行灾备：纳入 6 BOT 全量刷新；dr eggbot 仍排除。
- SendToAgent 在本 harness 不可用：自 live profile.json + research 现场 + 2026-09-16 archive 重建快照，未向各 BOT 发请求/不等回执。
- 现场增量：主张 C 仍锁定；PathBench 入实验平台候选；FlexPath 写入方法叙事近邻；cards约20；daily 09-16/17/18/21；weekly W38+W39；library.bib约229 行。
- archive/2026-09-16.md 已存在，未重复归档旧 MEMORY；直接覆盖写新 MEMORY.md。
- 密钥扫描：仅命中占位符/说明行，无明文密钥入仓。
- Slack 频道 id 仍未配置。

## 2026-09-28（周一例行全量）

- 例行灾备：纳入 6 BOT 全量刷新；dr eggbot 仍排除。
- SendToAgent 在本 harness 不可用：自 live profile.json + /home/box/research/ 现场 + 既有 MEMORY/archive 重建快照，未向各 BOT 发请求/不等回执。
- 现场增量：主张 C 仍锁定；近邻新增 localheur/LoHA*（09-25）、CLEAR（09-28）、RUSH（09-23）；实验设计模板近邻 flowfield-3dpp（09-22）；PathBench、FlexPath 仍在；cards≈40；library.bib≈455 行；daily 新增 09-22/23/25/28；weekly 新增 W40；inbox 20260928（CLEAR/compplan/SMCFPP/grorder/hexcpp）。
- 各 slug 将旧 MEMORY 归档为 archive/2026-09-21.md，再覆盖写新 MEMORY.md；未改动 archive/2026-09-16.md。
- 周会PPT：weekly-ppt/ 仍仅 09-16、09-17；未见 09-25 新 PPT（记为缺口/待确认）。
- 密钥扫描：仅命中占位符/说明行，无明文密钥入仓。
- Slack 频道 id 仍未配置（补缺写入 registry 与 shared-user-memory）。
