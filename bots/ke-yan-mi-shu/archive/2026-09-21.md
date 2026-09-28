# 科研秘书 — 记忆备份快照

- 备份时间：2026-09-21 12:10 Asia/Shanghai
- 请求方：记忆管家（灾备）
- Agent：科研秘书 / uuid 4793a740-0795-427c-90e5-ecd25c1388a8 / serverId 3496483
- 文件：/workspace/3496483-memory-backup.md（覆盖写）
- 重建方式：SendToAgent 不可用；自 prior MEMORY + profile.json + /home/box/research/ 现场重建

---

## 1. 身份

- 名称：科研秘书
- 一句话职责：每天（工作日）11:00 给用户一页中文简报，并问一个决定。
- 角色边界：用户每周 10–16 小时只做「定主张」；不代搜词、不管 bib、不翻译、不定主张本身（主张工坊）、不写英文稿（稿匠）、不承担 Cursor 实验。
- 时区：Asia/Shanghai
- 共享目录：/home/box/research/
- 用户侧入口：用户每天主要开本对话。
- 队友：
  - 文献员（serverId 3502351 / uuid 2be3fa28-5969-4ea0-abad-7eb14dd76ac1）：写 cards / library.bib / inbox.md；原「找文献」已停用。
  - 主张工坊、稿匠、周会PPT、记忆管家、dr eggbot 等为同账号队友。
- Skill：每日科研简报（sand-workflow:skill-1789552364105）
- Routine：每日科研简报（folder automation-1789552370357）
  - schedule：`CRON_TZ=Asia/Shanghai 0 11 * * 1-5`（工作日 11:00；周末不汇报）
- 用户偏好：回复用中文。

---

## 2. 历史决策

1. 主张锁定为 **C**（2026-09-16）：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。
2. 实验场检索：两条并行（公开二维可复现 + 去身份合成三维），各抓几篇。
3. 深读优先演进：
   - 2026-09-16：本周深读优先 **OAREST**（NeurIPS 2025）；HubRouter、Wavestar 仅简报入选不深读。
   - 2026-09-17：跟读默认 **TransPath**（AAAI 2023；公开二维启发式→三维列为未来工作）。
   - 2026-09-18：默认将 **PathBench** 列入实验平台候选（写入 CLAIM）。
   - 2026-09-21：默认将 **FlexPath**「连通先验共享 / 偏好重学」写入主张 C 方法叙事近邻（CLAIM 已更新）。
4. 文献队友切换：找文献 → 文献员（3502351）。
5. 简报结构：五段固定；最推荐放第 1 篇并写清推荐理由；每篇含题名链接/年份/相关理由/主干词/方法结果/作者贡献/不足/与主张关系。
6. 定时：曾 12:00 → 11:00；工作日 only（周末不汇报）。
7. 保密（以 CONSTRAINTS.md 为准）：检索主词禁 nuclear/核岛/核电与甲方项目名；论文正文已放开核电相关表述；甲方项目名与未公开内部规则名仍须谨慎。CLAIM「对外禁止」段仍可能偏旧——风险项按 CONSTRAINTS。

---

## 3. 现场快照

### 文件
- CLAIM.md：已锁定主张 C；实验平台候选 PathBench；方法叙事近邻 FlexPath；基线 HubRouter/REST/NCO/OARSMT
- CONSTRAINTS.md：目标约 2027-03 前可投稿；文献员工作日 10:30；秘书工作日 11:00；主张工坊周一 11:00
- inbox.md：20260921，5 篇（FlexPath / UPath / AMRA* / OctoPath / DRL-global-routing）
- cards/：自 09-16 起累计约 20 张（09-16×5、09-17×5、09-18×5、09-21×5）
- library.bib：约 229 行
- daily/：2026-09-16、09-17、09-18、09-21（周末 09-19/20 无简报，符合工作日约定）
- weekly/：2026-W38.md、2026-W39.md（W39 已含 FlexPath 措辞校准）

### 近期简报结论（精简）
- 09-16：最推荐 OAREST（可共享 vs 须重学同构）
- 09-17：最推荐 TransPath（启发式能否迁的问题骨架）
- 09-18：最推荐 PathBench（2D/3D 统一评测平台）
- 09-21：最推荐 FlexPath（连通先验共享 / 偏好重学；二维；非跨维）

### 待办 / 未闭环
- 用户 W38/W39 实验数字与截图尚未回传（pairs_manifest / conn_* / shared_layers 等）
- FlexPath/UPath 为预印本，venue 待确认
- CLAIM 保密段与 CONSTRAINTS 口径差仍待用户统一
- 本轮灾备未向本 BOT 发 SendToAgent 请求（harness 无该工具）

### 节奏约定
- 文献员：工作日 10:30 更新 inbox/cards/bib
- 科研秘书：工作日 11:00 一页简报
- 用户回复协议：采用 1,3 / 不用 2 / 再查：… / 主张暂定：…

---

## 4. 密钥占位

本角色不持有、不需要、未存储任何外部 API credential / 密码 / session。

| 用途 | 占位 |
|------|------|
| 外部检索 API | `<NO_SECRET_REQUIRED — use public arXiv/PDF links via literature agent>` |
| GitHub / 私有仓 | `<DELEGATE_TO_记忆管家_OR_用户 — 科研秘书不持有 git credentials>` |
| 会议 PDF 直链 | `<PUBLIC_URL_ONLY — NeurIPS proceedings / arXiv>` |
| MCP / 连接器 | `<NONE_IN_THIS_AGENT>` |

禁止项确认：本文件无明文 credential、密钥、session。

---

## 备份元数据

- 覆盖主题：身份与边界、主张 C、OAREST/TransPath/PathBench/FlexPath 演进、简报格式、定时工作日 11:00、保密 CONSTRAINTS、共享路径与 09-16..21 产物、密钥占位
- 一致性抽查：主张 C 与 OAREST「可共享层 vs 须重学层」主题仍与主张工坊 MEMORY 一致
