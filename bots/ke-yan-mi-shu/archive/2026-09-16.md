# 科研秘书 — 记忆备份快照

- 备份时间：2026-09-16 19:39 Asia/Shanghai
- 请求方：记忆管家（灾备）
- Agent：科研秘书 / id 可见于 agent-data 路径 4793a740-0795-427c-90e5-ecd25c1388a8
- 文件：/workspace/3496483-memory-backup.md（覆盖写）

---

## 1. 身份

- 名称：科研秘书
- 一句话职责：每天（工作日）11:00 给用户一页中文简报，并问一个决定。
- 角色边界：用户每周 10–16 小时只做「定主张」；不代搜词、不管 bib、不翻译、不定主张本身（主张工坊）、不写英文稿（稿匠）、不承担 Cursor 实验。
- 时区：Asia/Shanghai
- 共享目录：/home/box/research/
- 用户侧入口：用户每天主要开本对话。
- 队友：
  - 文献员（id 3502351）：写 cards / library.bib / inbox.md；原「找文献」已停用，勿再调用旧实例。
  - 主张工坊、稿匠、周会PPT、记忆管家、dr eggbot 等为同账号队友。
- Skill：每日科研简报（sand-workflow:skill-1789552364105）
- Routine：每日科研简报（folder automation-1789552370357）
  - schedule：`CRON_TZ=Asia/Shanghai 0 11 * * 1-5`（工作日 11:00；周末不汇报）
  - 状态：enabled（已 resume）
- 用户偏好：回复用中文。

---

## 2. 历史决策

1. 主张锁定为 **C**（2026-09-16）：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。
2. 实验场检索：两条并行（公开二维可复现 + 去身份合成三维），各抓几篇。
3. 本周深读优先：**OAREST**（NeurIPS 2025）；HubRouter、Wavestar 仅简报入选不深读。
4. 文献队友切换：找文献 → 文献员（3502351）。
5. 简报结构演进：
   - 五段固定：主张状态 / 今日 3 篇 / 一个问题 / ≤2 条待办（≤25 分钟） / 风险
   - 每篇必含：英文题名+链接、年份、相关理由、对应主干词、方法与结果摘记、作者自称贡献、文中不足、和主张关系与建议看摘要还是方法
   - **最推荐放第 1 篇，并写清推荐理由**
6. 定时：曾 12:00 → 11:00；先 paused 测格式 → 用户指示全部开放后 resume → 再改为工作日 only（周末不汇报）。
7. 保密（以 CONSTRAINTS.md 为准，2026-09-16 最新）：
   - 检索主词禁止：nuclear / 核岛 / 核电；仍禁甲方项目名当检索主词
   - 论文正文已放开核电相关表述；简报风险项勿再把「正文出现核电」当默认违规
   - 仍慎写甲方项目名与未公开内部规则名
   - 注意：CLAIM.md 内「对外禁止」段落可能仍为旧文，以 CONSTRAINTS 为准，待主张工坊/用户统一 CLAIM 文案

---

## 3. 现场快照

### 文件
- CLAIM.md：已锁定主张 C（见上）；实验场与基线 HubRouter/REST/NCO/OARSMT
- CONSTRAINTS.md：目标约 2027-03 前可投稿稿；文献员 10:30 更新 inbox；秘书工作日 11:00 简报；主张工坊周一 11:00
- inbox.md：20260916，5 篇（HubRouter / REST / OAREST / MRA* / Wavestar）
- cards/：20260916-*.md（含状态字段：OAREST=采用深读；HubRouter/Wavestar=简报入选不深读）
- library.bib：已追加 keys du2023hubrouter, liu2021rest, du2025oarest, du2020mra, reijgwart2025wavestar
- daily/2026-09-16.md：推荐置顶版简报（OAREST → HubRouter → Wavestar）已存档

### 今日简报结论（精简）
1. 最推荐 OAREST：与主张 C「可共享层 vs 须重学层」同构（RES + dynamic masking / 训针脚测障碍）
2. HubRouter：二维学习全局布线基线
3. Wavestar：三维多分辨率 coarse-to-fine；arXiv:2602.21174 可打开但日期标签偏后，采用前建议再核

### 待办 / 未闭环
- 用户应继续深读 OAREST 方法小节 + 一段摘要（约 15 分钟）
- Routine 已 enabled 且为工作日 11:00，但 automation_status 仍显示 never run（尚未到下一个工作日 11:00 触发）
- CLAIM.md 保密段与 CONSTRAINTS 可能不一致，建议后续对齐文案（不擅自改主张正文）

### 节奏约定
- 文献员：每天 10:30 更新 inbox/cards/bib
- 科研秘书：工作日 11:00 一页简报
- 用户回复协议：采用 1,3 / 不用 2 / 再查：… / 主张暂定：…

---

## 4. 密钥占位

本角色不持有、不需要、未存储任何外部 API token / 密码 / cookie。

| 用途 | 占位 |
|------|------|
| 外部检索 API | `<NO_SECRET_REQUIRED — use public arXiv/PDF links via literature agent>` |
| GitHub / 私有仓 | `<DELEGATE_TO_记忆管家_OR_用户 — 科研秘书不持有 git credentials>` |
| 会议 PDF 直链 | `<PUBLIC_URL_ONLY — NeurIPS proceedings / arXiv>` |
| MCP / 连接器 token | `<NONE_IN_THIS_AGENT>` |

禁止项确认：本文件无明文 token、密钥、cookie、session。

---

## 备份元数据

- 覆盖主题：身份与边界、主张 C、文献队友切换、OAREST 深读、简报格式规则、定时工作日 11:00、保密 CONSTRAINTS、共享路径与当日产物、密钥占位
- 待确认项见「现场快照 · 待办 / 未闭环」
