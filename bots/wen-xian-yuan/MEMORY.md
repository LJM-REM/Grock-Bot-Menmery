# 文献员记忆快照

- 备份时间：2026-09-21 12:10 Asia/Shanghai
- 请求方：记忆管家
- 代理：文献员（原「找文献」，因唤醒故障重建改名）
- uuid: 2be3fa28-5969-4ea0-abad-7eb14dd76ac1
- serverId: 3502351
- 文件：`/workspace/3502351-memory-backup.md`（覆盖写）
- 共享目录：`/home/box/research/`
- 重建方式：SendToAgent 不可用；自 prior MEMORY + profile + research 现场重建
- 本快照不含明文密钥

---

## 1. 身份

- 名称：文献员
- 角色：按当前主张搜论文，写成卡片和 bib；用户说话就正常回复。不是研究员。不定主张、不发明创新点、不写论文、不发邮件、不管 Cursor、不改其他 Bot。
- 用户：REM；时区 Asia/Shanghai；回复用中文。
- 交互硬规则：每条用户消息及时中文回复，并应出现「正在工作」；禁止装死、禁止只写文件不说话。搜完立刻短报篇数、路径、失败原因。
- 检索源优先级：arXiv、Semantic Scholar、DBLP；Google Scholar 补充。
- 领域锚点：neural combinatorial optimization, pointer network routing, obstacle-avoiding rectilinear Steiner, hub generation / neural Steiner, grid/voxel path planning, coarse-to-fine routing。
- 检索主词禁止（以 CONSTRAINTS.md 为准）：nuclear, 核岛, 核电, 甲方项目名。
- 论文正文：CONSTRAINTS 已放开核电相关表述；检索与投稿改写是两回事；文献员只负责检索与卡片。
- 每次交付最多 5 篇。卡片字段：英文题名+链接、年份、会议/期刊、相关理由、对应主干词、方法与结果摘记、作者自称贡献、文中不足、与 CLAIM 关系、BibTeX。
- 落盘：`/home/box/research/cards/YYYYMMDD-短名.md`；追加 `library.bib`；覆盖 `inbox.md`。禁止编造。
- 节奏：工作日 10:30「日更文献」；周末不跑。可被科研秘书调用。
- 例行任务：`日更文献` folder `automation-1789553895778`，enabled，`CRON_TZ=Asia/Shanghai 30 10 * * 1-5`。

## 2. 历史决策

- 2026-09-16 创建本代理，替代哑掉的「找文献」。
- 同日创建例行「日更文献」→ resume → 改为工作日 only `30 10 * * 1-5`。
- CLAIM 锁定主张 C；基线对照 HubRouter / REST / NCO / OARSMT。
- 检索禁词：CONSTRAINTS 禁检索主词 nuclear/核岛/核电；论文正文放开。
- 卡片字段加码后按新字段搜写。
- 2026-09-16 首次交付 5 篇（HubRouter/REST/OAREST/MRA*/Wavestar）。
- 2026-09-17 交付：TransPath / NeuralSteiner / NeuroSteiner / NN-Steiner / MazeNet（简报置顶 TransPath）。
- 2026-09-18 交付：PathBench / Neural-A* / OARSMT-flow / GAT-Steiner / Attention-NCO（PathBench 入平台候选）。
- 2026-09-21 交付：FlexPath / UPath / AMRA* / OctoPath / DRL-global-routing（FlexPath 写入主张方法叙事近邻）。
- 检索失败常态：Semantic Scholar 常 429；DBLP 偶发 bot/429；保密主词未用于检索。

## 3. 现场快照

### 主张 C（CLAIM.md）
同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。实验平台候选 PathBench；方法叙事近邻 FlexPath。

### 最新 inbox（20260921）5 篇
1. FlexPath — arXiv 2026 — 支持 — 二维；连通先验可共享/偏好须适配 — `cards/20260921-flexpath.md` — kim2026flexpath
2. UPath — arXiv 2026 — 支持 — 公开二维学习启发式；拓扑异分布 — `cards/20260921-upath.md` — ananikian2026upath
3. AMRA* — ICRA 2022 — 可作基线 — 多分辨率 anytime — `cards/20260921-amra-star.md` — saxena2022amra
4. OctoPath — Sensors 2021 — 支持 — 三维 OcTree/体素层次 — `cards/20260921-octopath.md` — trasnea2021octopath
5. DRL-global-routing — J. Mech. Des. 2020 — 可作基线 — NCO/DRL 全局布线 — `cards/20260921-drl-global-routing.md` — liao2020drlgr

### 库存
- cards/：约 20 张（09-16..21）
- library.bib：约 229 行
- daily 简报已引用多日 inbox；显式「二维→三维」同一表示迁移量化文献仍稀薄

### 协作
- 科研秘书：持续消费 inbox 出简报
- 主张工坊：W39 已吸收 FlexPath 措辞
- 记忆管家：本文件即灾备快照（无 SendToAgent 回执）

## 4. 密钥占位

本代理不持有也不需要外部账号密钥。灾备占位如下（均为占位符，非真实值）：

- Semantic Scholar API key：`<SEMANTIC_SCHOLAR_API_KEY>`（当前未配置；曾遇 429）
- DBLP：公开 API，无密钥；曾遇 bot/429
- arXiv：公开 API，无密钥
- Google Scholar：无 connector；禁止写入浏览器 session
- GitHub / Origin：`<GITHUB_CREDENTIAL>` / `<ORIGIN_CREDENTIAL>`（文献员不使用）
- 邮箱 / Slack / 其他 connector：`<CONNECTOR_CREDENTIAL>`（未用）
- 甲方项目名：不写入本快照，不当检索主词
