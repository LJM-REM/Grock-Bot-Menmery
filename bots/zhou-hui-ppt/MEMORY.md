# 周会PPT 记忆快照（agent serverId 3513989）

备份时间：2026-09-16 19:39 Asia/Shanghai  
请求方：记忆管家（灾备）  
禁止内容：明文 token / 密钥 / cookie（仅占位）

---

## 1. 身份

- **名称**：周会PPT
- **serverId**：3513989
- **一句话职责**：每周四 12:00 根据本周 GitHub 更新生成中文周会工作 PPT。
- **用户**：REM（偏好中文回复）
- **时区**：Asia/Shanghai
- **目标仓库**：https://github.com/LJM-REM/3DPipRouter-V2.git（LJM-REM/3DPipRouter-V2），公开可 clone
- **对比窗口**：自「上周四 12:00 Asia/Shanghai」至今的 commits / merged PR / 显著文件变更（用户通常周三推代码）
- **数据手段**：gh / git log / diff 摘要；禁止编造提交；GitHub 未授权时如实报失败
- **交付目录**：/home/box/research/weekly-ppt/
- **样式参考**：/home/box/research/weekly-ppt/style-ref/sample-report.pptx 与 STYLE.md
- **例行任务**：周会PPT [enabled]，folder `ppt`，CRON_TZ=Asia/Shanghai `0 12 * * 4`（每周四 12:00）；截至备份时 never run
- **明确不做**：不改仓库、不 push、不发邮件、不做科研文献简报、不编造未提交的工作

---

## 2. 历史决策

1. **样式必须贴近用户样例**（2026-09-16，via dr eggbot / 人设更新）  
   - 图文并茂；每页顶栏日期标题 + 面包屑路径 + 水平阶段导航（当前节高亮）  
   - 不要做成纯文字条目列表  
   - 导航可用「总览 / 各改动主题 / 风险与下周」，或沿用样例阶段条（规则口径→几何底座→…→输出路径）并只展开本周有改动的节  
   - 生成前先读 STYLE.md

2. **文件命名硬性规则**（2026-09-16，用户 REM 亲口）  
   - 格式：`利进铭_x月xx日汇报.pptx`  
   - 日期取**当周周四**（周会日），不是生成当天  
   - 例：周四为 9 月 17 日 → `利进铭_9月17日汇报.pptx`  
   - 顶栏标题同步用「M月D日汇报」（周四日期）  
   - 已写入 STYLE.md「文件命名」节；已更新例行任务 prompt

3. **人设交付路径说明与命名并存**  
   - 旧人设写过 `YYYY-MM-DD-周会.pptx`；现行以用户命名规则为准（利进铭_周四日期）  
   - 首跑曾产出过 `2026-09-16-周会.pptx` 作过程稿；正式交付名为 `利进铭_9月17日汇报.pptx`

4. **授权策略**  
   - 仓库公开，可无 gh 登录直接 clone + git log  
   - GitHub MCP connector 需要 PAT，首跑未安装；`gh` 已装未登录  
   - 无权限或无提交时如实说明，禁止编造

5. **定时节奏**  
   - 先手动跑通，再依赖周四 12:00 cron（已创建且 enabled）  
   - 用户可说「生成本周 PPT」手动触发

6. **交互**  
   - 用户说话用中文回复，并显示「正在工作」  
   - 做完短报路径与页数，附件发对话

---

## 3. 现场快照

### 记忆（agent profile 级）
- 周会 PPT 必须贴近样例风格：style-ref/sample-report.pptx 与 STYLE.md；图文并茂，每页顶栏日期+面包屑+水平导航高亮，不要纯文字列表。
- 文件命名：`利进铭_x月xx日汇报.pptx`，日期取当周周四。

### 共享用户偏好
- 后续用中文回答（via 记忆管家 / 其他助手亦有记录）

### 本周首次手动生成（2026-09-16）
- 时间窗：2026-09-10 12:00 — 2026-09-16（Asia/Shanghai）
- **Commit 数：0**（如实写入 PPT，未编造）
- 窗口前最新提交对照：`411209a`（2026-09-08）Q0b refine/GF01
- 正式文件：`/home/box/research/weekly-ppt/利进铭_9月17日汇报.pptx`（3 页：总览 / 无显著更新 / 风险与下周）
- 过程稿仍在：`/home/box/research/weekly-ppt/2026-09-16-周会.pptx`
- 仓库本地 clone：`/workspace/3DPipRouter-V2`
- python-pptx：`/workspace/.venv-pptx`（系统 pip 受 PEP668 限制）

### 例行任务状态
- 周会PPT：enabled，never run（下次预期：周四 12:00）

### 队友协作要点
- dr eggbot：创建时要求建 cron + 样例风格  
- 记忆管家：本灾备快照

### 待改进（非阻塞）
- 样例母版观感可再贴近（首版已有顶栏+导航，图文可加强）
- 可选：登录 `gh` 以便统计 merged PR

---

## 4. 密钥占位

| 用途 | 状态 | 占位 |
|------|------|------|
| GitHub CLI (`gh auth`) | 未登录 | `<GH_TOKEN_OR_GH_AUTH_LOGIN>` |
| GitHub MCP Personal Access Token | 未安装 connector / 无 PAT | `<GITHUB_PERSONAL_ACCESS_TOKEN>` |
| Cursor SCM GitHub 集成 | 未确认 | `<CURSOR_SCM_GITHUB>` |
| 其他 API / cookie | 无 | `<N/A>` |

说明：本助手不持有、不备份任何明文凭证；恢复时由用户在对应界面重新授权。

---

## 备份元数据

- 输出路径：`/workspace/3513989-memory-backup.md`
- 覆盖主题：身份与职责、仓库与时间窗、样式规范、命名规则、例行任务、首跑结果（0 commit）、交付路径、授权现状、密钥占位
- 待确认项：
  1. 人设 JSON 里交付路径仍写 `YYYY-MM-DD-周会.pptx`，是否要用 update_state 改成命名规则描述（现行以记忆+routine+STYLE.md 为准）
  2. 是否需要清理过程稿 `2026-09-16-周会.pptx`
  3. 是否优先安排 `gh auth` 以便后续周报含 merged PR
