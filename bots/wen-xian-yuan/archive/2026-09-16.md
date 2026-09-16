# 文献员记忆快照

- 备份时间：2026-09-16 19:39 Asia/Shanghai
- 代理：文献员（原「找文献」，因唤醒故障重建改名）
- 文件：`/workspace/3502351-memory-backup.md`
- 共享目录：`/home/box/research/`
- 本快照不含明文 token / 密钥 / cookie

---

## 1. 身份

- 名称：文献员
- 角色：按当前主张搜论文，写成卡片和 bib；用户说话就正常回复。不是研究员。不定主张、不发明创新点、不写论文、不发邮件、不管 Cursor、不改其他 Bot。
- 用户：REM；时区 Asia/Shanghai；回复用中文。
- 交互硬规则：每条用户消息及时中文回复，并应出现「正在工作」；禁止装死、禁止只写文件不说话。搜完立刻短报篇数、路径、失败原因。
- 检索源优先级：arXiv、Semantic Scholar、DBLP；Google Scholar 补充。
- 领域锚点：neural combinatorial optimization, pointer network routing, obstacle-avoiding rectilinear Steiner, hub generation / neural Steiner, grid/voxel path planning, coarse-to-fine routing。
- 检索主词禁止（以 CONSTRAINTS.md 为准）：nuclear, 核岛, 核电, 甲方项目名。
- 论文正文：CONSTRAINTS 已放开核电 / 核岛 / nuclear 等相关表述；甲方项目名与未公开内部规则名仍须谨慎。检索与投稿改写是两回事；文献员只负责检索与卡片。
- 每次交付最多 5 篇。卡片字段（供科研秘书简报引用）：英文题名+链接、年份、会议/期刊、相关理由、对应主干词、方法与结果摘记、作者自称贡献、文中不足、与 CLAIM 关系、BibTeX。
- 落盘：`/home/box/research/cards/YYYYMMDD-短名.md`；追加 `library.bib`；覆盖 `inbox.md`。禁止编造。
- 节奏：工作日 10:30「日更文献」；周末不跑。可被科研秘书调用。
- 例行任务：`日更文献` folder `automation-1789553895778`，enabled，`CRON_TZ=Asia/Shanghai 30 10 * * 1-5`，截至本快照从未跑过（今日为手动搜）。

## 2. 历史决策

- 2026-09-16 创建本代理，替代哑掉的「找文献」。
- 同日创建 paused 例行「日更文献」`30 10 * * *`；后用户「全部开放定时」→ resume；再改「周末不用汇报」→ `30 10 * * 1-5`。
- CLAIM 由未锁定改为锁定主张 C（主张工坊通知）：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，量化连通率与线长退化，并指出哪一层表示该共享、哪一层必须重学。基线对照：HubRouter / REST / NCO / OARSMT。
- 检索禁词曾短暂允许 nuclear/核岛/核电，随后 CONSTRAINTS 再次禁止检索主词；同时论文正文放开核电相关表述。以最新 CONSTRAINTS.md 为准。
- 卡片字段加码：题名链接、相关理由、主干词、方法与结果摘记、作者贡献、文中不足。之后搜写按此字段。
- 今日（20260916）第一次交付 5 篇（二维+三维均覆盖），科研秘书已出简报（3 篇：HubRouter / OAREST / Wavestar），存 `daily/2026-09-16.md`。
- 检索失败记录：Semantic Scholar 持续 429；DBLP bot/429；HubRouter/REST/NeuralSteiner 无 arXiv 条目（改用 NeurIPS/DAC 官方 PDF）；独立 NCO 关键词命中偏杂，以 REST/OAREST 覆盖 NCO 风格 Steiner。
- 用户未回复「现在搜 5 篇吗」的 widget，按跳过处理；实际已因主张工坊/科研秘书调用完成检索。
- 明确不做：不定主张、不发邮件、不管 Cursor、不改其他 Bot。

## 3. 现场快照

### 主张 C（CLAIM.md）
同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。实验场：公开二维栅格 + 去身份合成三维体素，两条并行、先用配对实例测迁移落差。

注意：CLAIM.md「保密」段仍写「对外禁止 nuclear、核岛、核电…」，与已更新的 CONSTRAINTS.md（检索禁、正文放开）不一致，见待确认。

### 今日 inbox（20260916）5 篇
1. HubRouter — NeurIPS 2023 — 可作基线 — 二维 VLSI — `cards/20260916-hubrouter.md` — key `du2023hubrouter`
2. REST — DAC 2021 — 可作基线 — 二维 RSMT / NCO 风格 — `cards/20260916-rest.md` — key `liu2021rest`
3. OAREST / Train on Pins and Test on Obstacles — NeurIPS 2025 — 可作基线+支持 — OARSMT — `cards/20260916-oarest.md` — key `du2025oarest`
4. Multi-Resolution A* — SoCS 2020 — 支持 — 公开 2D+3D 多分辨率栅格 — `cards/20260916-mra-star.md` — key `du2020mra`
5. Hierarchical Any-Angle 3D Grids / Wavestar — RSS 2025 — 支持 — 3D 体素 coarse-to-fine — `cards/20260916-wavestar-hier3d.md` — key `reijgwart2025wavestar`

BibTeX 已在 `library.bib`（5 keys 如上）。今日卡片写于字段加码之前，可能尚未含「主干词 / 作者贡献 / 文中不足」全套，下次日更应按新字段补或重写。

### 协作
- 科研秘书：已收到 inbox 并出简报。
- 主张工坊：已通知 5 篇落盘。
- dr eggbot：约束/定时/周末规则均已执行。
- 记忆管家：本文件即其发起的灾备快照。

### 用户偏好
- 中文回复；不让用户搜词、管 bib、翻译。

## 4. 密钥占位

本代理不持有也不需要外部账号密钥。灾备占位如下（均为占位符，非真实值）：

- Semantic Scholar API key：`<SEMANTIC_SCHOLAR_API_KEY>`（当前未配置；曾遇 429）
- DBLP：公开 API，无密钥；曾遇 bot/429
- arXiv：公开 API，无密钥
- Google Scholar：无 connector / 无 cookie 备份；禁止写入浏览器 cookie
- GitHub / Origin token：`<GITHUB_TOKEN>` / `<ORIGIN_TOKEN>`（文献员不使用）
- 邮箱 / Slack / 其他 connector：`<CONNECTOR_TOKEN>`（未用）
- 甲方项目名：不写入本快照，不当检索主词

