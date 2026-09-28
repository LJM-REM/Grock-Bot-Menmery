# 主张工坊 — 记忆快照（灾备）
- agent: 主张工坊
- agent_id: 986c6d76-1eb9-45c3-a22b-b0b9541d380f
- serverId: 3497408
- 备份时间：2026-09-21 12:10 Asia/Shanghai
- 请求方：记忆管家
- 文件：/workspace/3497408-memory-backup.md（覆盖写）
- 重建方式：SendToAgent 不可用；自 prior MEMORY + profile.json + research 现场重建
- 禁止明文密钥：本文件不含 credential；见「密钥占位」

## 1. 身份
- 名称：主张工坊
- 角色：贡献教练（非吹稿）。逼用户把项目改写成一句可投稿主张，并给出本周实验清单。
- 用户：REM；时区 Asia/Shanghai；偏好中文回复。
- 用户设定：第一篇论文；英文靠模型（稿匠）；实验用户自己在 Cursor 跑。
- 共享目录：`/home/box/research/`
- 队友（协作边界）：
  - 文献员：搜论文 → cards / library.bib / inbox；不发明创新点
  - 科研秘书：每日中文简报入口；不定主张本身
  - 稿匠：英文与 bib 编辑；无用户确认的中文主张不准扩写成论文贡献
  - 周会PPT / 记忆管家 / dr eggbot：基础设施与编排，不改科研主张内容
- Routine：周选题 folder `automation-1789552636609`；每周一 11:00（`0 11 * * 1`）
- 明确不做：不写代码、不翻译全文、不代跑 Cursor 实验、不替用户锁定主张、不把工程交付写成方法贡献

## 2. 历史决策
- 2026-09-16：首次开场读 CONSTRAINTS + cards；给出候选 A/B/C；用户采用主张 C；写入 CLAIM.md（已锁定）。
- 2026-09-16：写出本周实验清单 weekly/2026-W38.md；通知文献员按主张 C 补近邻。
- 2026-09-16：创建 routine「周选题」→ 改为每周一 11:00 → enabled。
- 2026-09-16..CONSTRAINTS：检索主词仍禁 nuclear/核岛/核电；论文正文已放开核电相关表述；实验场公开二维 + 去身份合成三维。
- 2026-09-18：科研秘书默认将 PathBench 列入实验平台候选（CLAIM 已反映）。
- 2026-09-21：写出 W39 清单；措辞校准——共享层≈连通/可行性先验，重学层≈目标偏好或细分辨率残差；对照 FlexPath 同维解耦，本文贡献仍是跨维量化。
- CLAIM「保密」段与 CONSTRAINTS「正文已放开」不完全一致——仍待用户确认是否改 CLAIM 表述。

## 3. 现场快照
### 当前主张（CLAIM.md）
- 状态：已锁定（2026-09-16）主张 C
- 一句话：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。
- 基线对照：HubRouter / REST / NCO / OARSMT（或公开可复现同类）
- 实验平台候选：PathBench（2026-09-18）
- 方法叙事近邻：FlexPath（2026-09-21）— 连通/可行性先验可共享，任务偏好须适配重学（二维；非跨维）

### 本周实验（2026-W39）
路径：`/home/box/research/weekly/2026-W39.md`
必做 ≤3：
1. 补齐/复核配对最小版（≥20 对 pairs_manifest.csv）
2. 钉死 2D 连通与线长两基线（几何 + 搜索）
3. 零样本迁移 + 显式 shared/relearned 分层记账
回传：n_pairs, conn_2d_*, len_ratio_2d, conn_3d_zeroshot, len_ratio_3d_vs_3d_baseline, shared_layers, relearned_layers
截图：w39_pair_example_2d3d.png, w39_conn_bar.png, w39_len_scatter.png,（可选）w39_share_ablation.png
用户结果：W38/W39 数字与截图均尚未回传（截至 2026-09-21）

### 文献与简报
- cards 约 20 张（含 OAREST、TransPath、PathBench、FlexPath、UPath、OctoPath 等）
- inbox 最新 20260921；daily 09-16/17/18/21
- OAREST 主题与主张 C「可共享 vs 须重学」仍一致（与科研秘书快照对齐）

### 硬约束摘要
- 半年一篇；贡献只能一句；不把工程功能清单当创新
- 公开问题改写需要处理；实验优先公开 2D / 去身份合成 3D
- 档次等文献员攒约 15 篇近邻 venue 后再定（cards 已约 20，venue 混预印本）

## 4. 密钥占位
- 无本 bot 自持的外部 API credential / OAuth session / 私有 git deploy key。
- 占位符约定（本文件永不填明文）：
  - `<GITHUB_CREDENTIAL_OR_APP_AUTH>` — 若未来代表用户访问 GitHub
  - `<CURSOR_API_CREDENTIAL>` — 若平台注入
  - `<MCP_*_CREDENTIAL>` — 各连接器凭证
  - `<BOX_BROWSER_SESSION>` — 盒内浏览器登录态（非文本密钥）
- 科研仓库线索（公开 URL）：LJM-REM/3DPipRouter-V2（主张工坊不直接改代码）。

## 待确认项
1. 是否把 CLAIM.md「保密」段与 CONSTRAINTS 对齐？
2. W38/W39 实验数字/截图用户何时回传？
3. FlexPath 近邻措辞是否需用户显式确认（当前为简报默认采用）？
