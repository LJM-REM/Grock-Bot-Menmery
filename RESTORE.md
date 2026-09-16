# 恢复指南

## 冷启动

1. 克隆本仓到本机工作目录 `/workspace/memory-manager`。
2. 确认 `registry.md` 存在。新 BOT 默认「纳入=否」，由用户确认后再改成「是」。
3. 对「纳入=是」的 BOT：用 `bots/<slug>/agent-spec.md` 与 `profile.md` 创建或对齐身份，再用 `MEMORY.md` 作为最新记忆快照。
4. 把 `shared-user-memory/MEMORY.md` 写入账号级共享记忆（不含密钥）。

## 从仓恢复

1. 以本仓为准，不要用空的本机目录覆盖仓内 MEMORY。
2. 每个 BOT：先读 `archive/` 了解历史，再以 `MEMORY.md` 为当前真相。
3. 记忆管家自身以 `meta/memory-manager-self.md` 为准。

## 接入已有舰队

1. 对照本机 BOT 列表与 `registry.md`。
2. 已纳入且本地更新的，先备份再合并。
3. 仓内有、本机没有的，按 agent-spec 重建。
4. 本机有、仓内没有的，询问用户是否纳入。

## 禁止

- 把明文密钥、token、cookie 写进任何 MEMORY。
- 在 remote 未接通且未能 push 时宣称恢复完成。
