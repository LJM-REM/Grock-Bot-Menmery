# 主张工坊 — 记忆快照（灾备）
- agent: 主张工坊
- agent_id: 986c6d76-1eb9-45c3-a22b-b0b9541d380f
- serverId (profile): 见 profile.json
- snapshot_at: 2026-09-16T19:39+08:00 (Asia/Shanghai)
- writer: self (via 记忆管家请求)
- 禁止明文密钥：本文件不含 token / API key / cookie；见「密钥占位」

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
- 明确不做：不写代码、不翻译全文、不代跑 Cursor 实验、不替用户锁定主张、不把工程交付写成方法贡献

## 2. 历史决策
- 2026-09-16：首次开场读 CONSTRAINTS + cards；cards 当时为空，按关键词地图给出候选 A/B/C，注明证据不足。
- 2026-09-16：用户采用主张 C（2D→合成 3D 表示迁移）；写入 `CLAIM.md`（已锁定）。
- 2026-09-16：写出本周实验清单 `weekly/2026-W38.md`（可贴进 Cursor 的固定标题格式）。
- 2026-09-16：创建 routine「周选题」folder `automation-1789552636609`；初为周日 12:00 paused → 改为每周一 11:00（`0 11 * * 1`）paused → 用户指示全部开放定时后 **enabled/resumed**。
- 2026-09-16：通知文献员按主张 C 补近邻文献；文献员回报已写入 5 篇 cards（HubRouter / REST / OAREST / MRA* / Wavestar）。
- CONSTRAINTS 演变（以磁盘文件为准，主张工坊跟文件不跟口头打架）：
  - 检索主词仍禁止：nuclear / 核岛 / 核电；仍禁甲方项目名当检索主词
  - 论文正文：已放开核电相关表述（2026-09-16 用户指示）
  - 实验场：公开二维 + 去身份合成三维
  - 注意：`CLAIM.md` 保密段仍写着对外禁止 nuclear 等，与 CONSTRAINTS「正文已放开」不完全一致——待用户确认是否改 CLAIM 表述（见待确认）

## 3. 现场快照
### 当前主张（CLAIM.md）
- 状态：已锁定（2026-09-16）主张 C
- 一句话：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。
- 基线对照：HubRouter / REST / NCO / OARSMT（或公开可复现同类）

### 本周实验（2026-W38）
路径：`/home/box/research/weekly/2026-W38.md`
必做 ≤3：
1. 配对数据集 ≥20 对 (2D,3D) + `pairs_manifest.csv`
2. 2D 连通基线：几何（OARSMT 类）+ 搜索（A* 类）
3. 零样本/轻量迁移摸底；写清 shared vs relearned layers
回传数字：`n_pairs`, `conn_2d_geom`, `conn_2d_search`, `len_ratio_2d`, `conn_3d_zeroshot`, `len_ratio_3d_vs_3d_baseline`, `shared_layers`, `relearned_layers`
截图名：`w38_pair_example_2d3d.png`, `w38_conn_bar.png`, `w38_len_scatter.png`
用户结果：尚未回传（截至快照时）

### 文献 cards（磁盘）
- `20260916-hubrouter.md`
- `20260916-rest.md`
- `20260916-oarest.md`
- `20260916-mra-star.md`
- `20260916-wavestar-hier3d.md`

### Routine
- 周选题 [enabled]：每周一 11:00 Asia/Shanghai；`automation-1789552636609`；截至快照 never run

### 硬约束摘要（跟 CONSTRAINTS.md）
- 半年一篇；贡献只能一句；不把工程功能清单当创新
- 公开问题改写需要处理；实验优先公开 2D / 去身份合成 3D
- 档次等文献员攒约 15 篇近邻 venue 后再定

## 4. 密钥占位
- 无本 bot 自持的外部 API token / OAuth cookie / 私有 git deploy key（若有，由记忆管家/平台侧托管）。
- 占位符约定（本文件永不填明文）：
  - `<GITHUB_TOKEN_OR_APP_AUTH>` — 若未来代表用户访问 GitHub
  - `<CURSOR_API_KEY>` — 若平台注入
  - `<MCP_*_TOKEN>` — 各连接器凭证
  - `<BOX_BROWSER_SESSION>` — 盒内浏览器登录态（非文本密钥）
- 科研仓库线索（公开 URL，非密钥）：用户侧相关仓库见队友「周会PPT」配置中的 `LJM-REM/3DPipRouter-V2`（主张工坊不直接改代码）。

## 待确认项
1. 是否把 `CLAIM.md`「保密」段与 CONSTRAINTS 对齐（正文可写核电相关 vs CLAIM 仍列禁止）？
2. W38 实验数字/截图用户何时回传？回传后只允许：更新主张强度 / 改下周清单 / 建议放弃。
3. 「周选题」首次自动跑在下周一 11:00；若 CLAIM 仍锁定 C，应产出新一周清单还是只复盘未回传实验？需用户偏好（当前默认：有锁定则写清单；无新结果则注明证据/进度不足）。
