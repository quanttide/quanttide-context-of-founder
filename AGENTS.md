# AGENTS.md

量潮创始人第二大脑的记忆仓库：日志时间线、个人档案、方向决策。

## 记忆集

记忆按主题域分集存放。每个记忆集在本仓是独立的时间线、洞察与方向结构，`journal/`、`insight/`、`roadmap/` 目录名在各集内保持一致，层内文件由各集按自身主题定义；`default/` 另设对齐层 `intention/`，收人机协作的意图澄清（其余集暂不启用）。档案层统一在 `data/profile/`，见「档案分区」。

| 记忆集 | 主题域 | 说明 |
|--------|--------|------|
| `default/` | 创业与个人主线 | 业务、平台、认知与日常日志；档案为五轴（emotions / values / triggers / methods / expressions） |
| `work/` | 工作主线 | 从 `default/` 提炼的工作主体：业务、组织、平台、AI 协作；含日志、档案与 roadmap / insight / intention 三层 |

**分集规则**：

- 写入前先判断这条内容属于哪个集；拿不准时归 `default/`。
- **work 从 default 提炼**：工作相关的主体（业务、组织、平台、AI 协作）不留在 default，提炼到 work 集；`default/` 因此只保留 `journal/`。
- 路线图与洞察在集内闭环：某集的日志只产出该集自己的路线图与洞察；档案例外，允许跨集重组。
- 记忆集之间不互设依赖，单集可独立删除或归档。

## 档案分区

`data/profile/` 已迁出本仓，分区不再与记忆集一一对应：

| 分区 | 收什么 | 来源 |
|------|--------|------|
| `think/` | 认知档案：怎么想、怎么应对 | 各集日志蒸馏后按事情重组 |
| `work/` | 事项台账：事实、决定与下一步 | 各集日志中的在办事项 |
| `write/` | 创作认知地图与创作档案 | `write/` 日志 |

同一集日志可同时贡献多个分区；`think/` 允许跨集重组，不要求与记忆集同名。

## 目录与边界

| 层级 | 目录 | 内容特征 | 示例 |
|------|------|---------|------|
| 时间线 | `<集>/journal/` | 原始日志，按日期记录 | 新增/修改日志 |
| 特征 | `data/profile/`（已迁出本仓） | 跨日期蒸馏的稳定特征，按用途分区 | `think/`、`work/`、`write/` |
| 认知 | `<集>/insight/` | 想通的机制与规律，按实测分已确认/假说 | 已确认、假说 |
| 方向 | `data/roadmap/<集>/`（已迁出本仓） | 愿景、选择、待定方向 | 目标（含元目标）、核心问题、已决策、待决策 |
| 对齐 | `<集>/intention/` | 人机协作的意图对齐信息（`default/` 不设此层，见分集规则） | AI 提问时的澄清、交互摩擦处的澄清 |

**边界规则**：
- 单次事件与业务状态不进 `data/profile/`，也不进 `<集>/insight/` 与 `<集>/roadmap/`——它们只存在于 `<集>/journal/` 时间线中。
- 人机协作中「要 X，不要 Y」的意图澄清归 `<集>/intention/`；沉淀为稳定判断后归 `data/profile/`，成形为决策后归 `<集>/roadmap/`，同一内容只在一处完整展开。
- 认识三分：想通的一句话归 `<集>/insight/`；它反复套用成思维框架后归 `data/profile/think/` 的对应事情组；它引出的选择归 `<集>/roadmap/`。同一认识只在一处完整展开，跨层只留互链。
- 决策（无论已/待）归 `<集>/roadmap/`；元目标是目标的子层，随目标归 `<集>/roadmap/`；跨时间稳定的个人特征归 `data/profile/`。
- `data/profile/` 只描述特征，不给建议；建议是对话输出，不是档案内容。
- **日志落位**：当天日志直接放在记忆集根部（如 `default/2026-09-26.md`），便于在手机端直接写入；更早的日志平铺在 `<集>/journal/YYYY-MM-DD.md`。不设按来源的中间层目录。

## 工作流

### 触发规则

- **日志更新后蒸馏档案**：`<集>/journal/` 中新增或修改日志后，读取主仓 `quanttide-founder` 的 `.agents/skills/journal-to-profile/SKILL.md` 并按其流程更新 `data/profile/` 的对应分区（允许跨集重组），无需用户再次指示。
- **日志更新后更新路线图**：同一时机，读取主仓 `.agents/skills/journal-to-roadmap/SKILL.md` 并按其流程更新同一集 `<集>/roadmap/` 下的主题路线图，无需用户再次指示。
- **日志更新后提炼洞察**：同一时机，读取主仓 `.agents/skills/journal-to-insight/SKILL.md` 并按其流程更新同一集 `<集>/insight/` 下的认知洞察，无需用户再次指示。
- **日志更新后补充意图对齐**：同一时机，读取主仓 `.agents/skills/journal-to-intention/SKILL.md` 并按其流程更新同一集 `<集>/intention/` 下的意图记录（当前仅 `default/` 设该目录），无需用户再次指示。

### Skill 索引

| Skill | 用途 | 路径 |
|-------|------|------|
| `journal-to-profile` | 从日志蒸馏个人档案 | 主仓 `.agents/skills/journal-to-profile/SKILL.md` |
| `journal-to-roadmap` | 从日志蒸馏方向层路线图 | 主仓 `.agents/skills/journal-to-roadmap/SKILL.md` |
| `journal-to-insight` | 从日志提炼认知洞察 | 主仓 `.agents/skills/journal-to-insight/SKILL.md` |
| `journal-to-intention` | 从日志提取人机协作意图 | 主仓 `.agents/skills/journal-to-intention/SKILL.md` |

## 相关文档

| 文档 | 用途 |
|------|------|
| [README](README.md) | 仓库概述、目录树、数据流 |
| [CONTRIBUTING](CONTRIBUTING.md) | 工作原则、输出规范、提交规范、Skill 维护 |
| [CHANGELOG](CHANGELOG.md) | 版本变更记录 |

## 如何维护 AGENTS.md

| 类型 | 写在哪里 |
|------|---------|
| 协作原则、输出规范、提交规范 | [CONTRIBUTING.md](CONTRIBUTING.md) |
| 详细说明、工作流步骤 | 主仓 `.agents/skills/` 中的 Skill 文件 |
| 目录结构、数据流 | [README.md](README.md) |
| 记忆集、分层边界、触发规则 | AGENTS.md |

更新时机：新增记忆集、新增分层、触发规则变化时更新；README / CONTRIBUTING / Skill 已有的内容不重复。
