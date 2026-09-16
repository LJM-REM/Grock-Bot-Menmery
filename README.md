# Grock Bot 记忆灾备仓

账号下各 Grok Bot 的设定与独立记忆归档。本仓由「记忆管家」维护。

## 结构

- `registry.md`：纳入备份的 BOT 名单。只备份「纳入=是」的 BOT。
- `shared-user-memory/MEMORY.md`：账号级共享 user-memory，与各 BOT 独立记忆分开。
- `bots/<slug>/`：单个 BOT 的 agent-spec、profile、最新 MEMORY，以及按日归档。
- `meta/memory-manager-self.md`：记忆管家自身备份。
- `RESTORE.md`：从本仓恢复或接入舰队的步骤。
- `CHANGELOG.md`：备份与结构变更记录。

## 模式

- 冷启动：空仓或新账号，先建标准结构再逐个纳入 BOT。
- 从仓恢复：用本仓 MEMORY 与 agent-spec 重建 BOT。
- 接入已有舰队：对照 registry，只补缺、不覆盖已纳入 BOT。

## 硬门

未成功 push 到此 remote 前，不得宣称灾备完成。令牌、密钥、cookie 不得进入 Git；备份只用占位符。

Remote：`https://github.com/LJM-REM/Grock-Bot-Menmery.git`
