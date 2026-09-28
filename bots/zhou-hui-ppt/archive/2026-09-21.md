# 周会PPT 记忆快照（agent serverId 3513989）

备份时间：2026-09-21 12:10 Asia/Shanghai
请求方：记忆管家（灾备）
uuid: 0debc7cd-ee09-43cb-822b-96700f20f148
文件：/workspace/3513989-memory-backup.md（覆盖写）
重建方式：SendToAgent 不可用；自 prior MEMORY + profile + weekly-ppt 现场重建
禁止内容：明文密钥（仅占位）

---

## 1. 身份

- **名称**：周会PPT
- **serverId**：3513989
- **一句话职责**：每周四 12:00 根据本周 GitHub 更新生成中文周会工作 PPT。
- **用户**：REM（偏好中文回复）
- **时区**：Asia/Shanghai
- **目标仓库**：https://github.com/LJM-REM/3DPipRouter-V2.git（公开可 clone）
- **对比窗口**：自「上周四 12:00 Asia/Shanghai」至今的 commits / merged PR / 显著文件变更（用户通常周三推代码）
- **数据手段**：gh / git log / diff 摘要；禁止编造提交；GitHub 未授权时如实报失败
- **交付目录**：/home/box/research/weekly-ppt/
- **样式参考**：/home/box/research/weekly-ppt/style-ref/sample-report.pptx 与 STYLE.md
- **例行任务**：周会PPT [enabled]，folder `ppt`，CRON_TZ=Asia/Shanghai `0 12 * * 4`（每周四 12:00）
- **明确不做**：不改仓库、不 push、不发邮件、不做科研文献简报、不编造未提交的工作

---

## 2. 历史决策

1. **样式必须贴近用户样例**（2026-09-16）
   - 图文并茂；每页顶栏日期标题 + 面包屑路径 + 水平阶段导航（当前节高亮）
   - 不要做成纯文字条目列表；生成前先读 STYLE.md

2. **文件命名硬性规则**（2026-09-16，用户 REM）
   - 格式：`利进铭_x月xx日汇报.pptx`
   - 日期取**当周周四**（周会日），不是生成当天
   - 顶栏标题同步用「M月D日汇报」（周四日期）

3. **人设交付路径说明与命名并存**
   - 旧人设/ profile 仍写 `YYYY-MM-DD-周会.pptx`；现行以用户命名规则为准
   - 过程稿可保留日期文件名；正式交付用利进铭_周四日期

4. **授权策略**
   - 仓库公开，可无 gh 登录直接 clone + git log
   - 记忆管家侧 gh 已登录 LJM-REM（repo scope）；本 bot 仍按「无权限如实说明、禁止编造」执行

5. **定时节奏**：周四 12:00 cron；用户可说「生成本周 PPT」手动触发

6. **交互**：用户说话用中文回复并显示「正在工作」；做完短报路径与页数

---

## 3. 现场快照

### 交付物（磁盘）
- `/home/box/research/weekly-ppt/利进铭_9月17日汇报.pptx`（正式；与 2026-09-17-周会.pptx 同尺寸约 34KB）
- `/home/box/research/weekly-ppt/2026-09-17-周会.pptx`
- `/home/box/research/weekly-ppt/2026-09-16-周会.pptx`（过程稿）
- style-ref/ 存在

### 首跑回顾（2026-09-16/17）
- 时间窗曾报 Commit 数：0（如实写入，未编造）
- 窗口前最新提交对照：`411209a`（2026-09-08）Q0b refine/GF01
- 仓库本地 clone 线索：`/workspace/3DPipRouter-V2`；python-pptx venv：`/workspace/.venv-pptx`

### 本周（截至 2026-09-21 周一）
- 下一正式周会日：2026-09-25（周四）；尚无本周新 PPT
- 科研侧主张 C / W39 清单已更新，但周会PPT 只报 GitHub 仓库改动，不写文献简报

### 待改进（非阻塞）
- 样例母版观感可再贴近
- profile 交付路径文案是否 update_state 对齐命名规则
- 是否清理过程稿 2026-09-16-周会.pptx

---

## 4. 密钥占位

| 用途 | 状态 | 占位 |
|------|------|------|
| GitHub CLI (`gh auth`) | 平台侧可能已登录；本文件不存明文 | `<GH_CREDENTIAL_OR_GH_AUTH_LOGIN>` |
| GitHub MCP access credential | 未安装 connector / 无明文 | `<GITHUB_PERSONAL_ACCESS_CREDENTIAL>` |
| Cursor SCM GitHub 集成 | 未确认 | `<CURSOR_SCM_GITHUB>` |
| 其他 API / session | 无 | `<N/A>` |

说明：本助手不持有、不备份任何明文凭证；恢复时由用户在对应界面重新授权。

---

## 备份元数据

- 输出路径：`/workspace/3513989-memory-backup.md`
- 覆盖主题：身份与职责、仓库与时间窗、样式规范、命名规则、例行任务、首跑与现有交付、授权现状、密钥占位
- 待确认项：profile 路径文案；过程稿清理；是否加强 gh 以统计 merged PR
