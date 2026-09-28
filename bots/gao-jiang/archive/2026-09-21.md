# 稿匠 memory backup
- agent_server_id: 3497565
- uuid: f8d8dfc0-ac98-4eff-8147-0412f0e91dd7
- 备份时间：2026-09-21 12:10 Asia/Shanghai
- 请求方：记忆管家
- 文件：/workspace/3497565-memory-backup.md（覆盖写）
- source: prior MEMORY + profile + /home/box/research/ 现场只读
- 重建方式：SendToAgent 不可用

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
  - 泄密检查（见历史决策）
- 禁止：发明没做过的实验；把工程交付写成方法贡献；不经用户确认提高声称强度；发邮件；改其他 bot；替用户定主张；创建定时 routine（创建时明确「先不定时」）
- 队友：主张工坊、文献员、科研秘书、周会PPT、记忆管家
- 用户偏好（共享）：后续用中文回答

## 2. 历史决策
- 2026-09-16 首轮：用户选择「等主张锁定再动笔」——锁定前不扩写贡献；锁定后等中文大纲再写。
- 2026-09-16 保密口径：论文正文 nuclear/核岛/核电/plant/舱段已放开；仍须避免甲方项目名、未公开内部规则名；检索主词仍禁 nuclear/核岛/核电。
- 节奏约定（CONSTRAINTS，本 bot 不自建 routine）：文献员工作日 10:30；科研秘书工作日 11:00；主张工坊每周一 11:00。
- 目标：约 2027-03 前至少一篇可投稿稿；前 6 个月目标为问题干净、实验可复现、贡献只有一句的领域论文。
- 2026-09-16..21：主张 C 持续锁定；CLAIM 增 PathBench 平台候选与 FlexPath 方法叙事近邻；本 bot 仍待机（无中文大纲）。

## 3. 现场快照
- CLAIM.md：已锁定主张 C；PathBench 候选；FlexPath 近邻；基线 HubRouter/REST/NCO/OARSMT。
- CLAIM「保密」段 vs CONSTRAINTS「正文已放开」口径差仍在。
- library.bib：约 229 行（较 09-16 的约 52 行显著增长）。
- cards/：约 20 张（含 OAREST、TransPath、PathBench、FlexPath 等）。
- inbox.md、daily/09-16..21、weekly/W38+W39、weekly-ppt/ 均存在。
- 本 bot 写作状态：主张已锁定，用户尚未交付中文大纲；按决策仍待机，不主动扩写。
- 无已写英文草稿路径记入本 bot 记忆（未产出）。

## 4. 密钥占位
- 无本 bot 持有的 API credential / session 需备份。
- 若恢复时需外部服务：CURSOR_API_CREDENTIAL=<REDACTED>；GitHub PAT=<REDACTED>；邮箱凭据=<REDACTED>；浏览器登录会话=<REDACTED>。
- 私有仓库灾备由记忆管家侧管理；本文件不含 registry 密钥。

## 待确认项
1. CLAIM vs CONSTRAINTS 保密口径：扩写正文时以哪份为准？
2. 用户是否视为可开始交付中文大纲？
3. 密集使用时间：以最新 profile「有中文大纲再密用」为准。
