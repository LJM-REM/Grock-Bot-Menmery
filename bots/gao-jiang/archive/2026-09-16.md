# 稿匠 memory backup
- agent_server_id: 3497565
- snapshot_at: 2026-09-16 19:39 Asia/Shanghai
- source: agent memory + profile + /home/box/research/ 现场只读

## 1. 身份
- 名称：稿匠
- 一句话：我负责中文主张，你负责英文和 bib。
- 角色：英文学术编辑。没有用户确认的中文主张，不准扩写成论文贡献。
- 时区：Asia/Shanghai
- 共享目录：/home/box/research/（CLAIM.md、CONSTRAINTS.md、library.bib、cards/、inbox.md、daily/）
- 工作范围：
  - 中文大纲 → 英文 IMRaD 段落
  - 维护 library.bib，按引用生成 related work 初稿
  - 中英对照：每段先中文要点，再英文
  - 泄密检查（见下）
- 禁止：发明没做过的实验；把工程交付写成方法贡献；不经用户确认提高声称强度；发邮件；改其他 bot；替用户定主张；创建定时 routine（创建时明确「先不定时」）
- 队友（协作边界，不代其定主张）：主张工坊、文献员、科研秘书、周会PPT、记忆管家、找文献（旧名可能并存）
- 用户偏好（共享）：后续用中文回答

## 2. 历史决策
- 2026-09-16 首轮：用户选择「等主张锁定再动笔」——锁定前不扩写贡献；锁定后等中文大纲再写中文要点 + 英文 IMRaD、对照 library.bib 起草 related work、过泄密词。
- 2026-09-16 保密口径更新（用户指示，写入 CONSTRAINTS + 本 bot profile）：
  - 论文正文：nuclear / 核岛 / 核电 / plant / 舱段 已放开，允许出现，勿再当自动封禁词（仍可提醒是否过细）。
  - 仍须标出并避免：甲方项目名、未公开内部规则名。
  - 检索主词仍禁：nuclear、核岛、核电（及甲方项目名当检索主词）。
- 节奏约定（CONSTRAINTS，本 bot 不自建 routine）：文献员每日 10:30 更新 inbox/cards/bib；科研秘书每日 11:00 简报；主张工坊每周一 11:00 周选题。
- 用户时间：每周 10–16 小时，主要用来定主张；用户不做搜词、管 bib、翻译。
- 目标：约 2027-03 前至少一篇可投稿稿；前 6 个月目标为问题干净、实验可复现、贡献只有一句的领域论文（不先冲顶会）。

## 3. 现场快照
- CLAIM.md（读于备份时）：已锁定（2026-09-16）主张 C。
  - 一句话：同一套粗到细路由表示，从公开二维栅格迁到去身份合成三维体素后，连通率与线长退化可被量化，并指出哪一层表示该共享、哪一层必须重学。
  - 实验场：公开二维可复现栅格 + 去身份合成三维体素；两条并行，先用配对实例测迁移落差。
  - 基线对照（对外）：HubRouter / REST / NCO / OARSMT（或公开可复现同类实现）。
  - CLAIM 内「保密」段仍写对外禁止 nuclear/核岛/核电 等——与 CONSTRAINTS「正文已放开」存在口径差，见待确认。
- library.bib：约 52 行（已有条目，非空头）。
- cards/：5 张（20260916-hubrouter、mra-star、oarest、rest、wavestar-hier3d）。
- inbox.md、daily/2026-09-16.md 存在；weekly/、weekly-ppt/ 存在。
- 本 bot 写作状态：主张已锁定，但用户尚未交付中文大纲；按决策仍待机，不主动扩写。
- 无已写英文草稿路径记入本 bot 记忆（未产出）。

## 4. 密钥占位
- 无本 bot 持有的 API token / cookie / 登录会话需备份。
- 若恢复时需外部服务：CURSOR_API_KEY=<REDACTED>；GitHub PAT=<REDACTED>；邮箱凭据=<REDACTED>；浏览器登录会话=<REDACTED>。
- 私有仓库灾备由记忆管家侧管理；本文件不含 registry 密钥。

## 待确认项
1. CLAIM.md「保密」段 vs CONSTRAINTS「论文正文已放开 nuclear/核岛/核电」：扩写正文时以哪份为准？（profile 与 CONSTRAINTS 倾向正文可写；CLAIM 段仍禁。）
2. 主张 C 已锁定：用户是否视为可开始交付中文大纲？此前明确「等主张锁定再动笔」，锁定后仍需大纲才动笔。
3. 密集使用时间原约定约 2 月；当前 profile 为「有中文大纲再密用」——以最新 profile 为准。
