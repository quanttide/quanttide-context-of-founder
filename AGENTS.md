# AGENTS.md

量潮创始人第二大脑的记忆仓库：日志时间线、个人档案、方向决策。

## 记忆集

记忆只保留 `default/` 一个集，按日期存原始日志；档案、方向、洞察与意图随做随迁到独立仓库。档案层统一在 `data/profile/`，见「档案分区」。

| 记忆集 | 主题域 | 收什么 |
|--------|--------|------|
| `default/` | 创业与个人主线 | 业务、平台、认知与日常日志 |

**分集规则**：

- 本仓只保留 `default/` 一个集；拿不准去向的内容放这里。
- 成熟内容随做随迁：档案归 `data/profile`，方向归 `data/roadmap`，洞察归 `data/insight`，意图归 `data/intention`，日志归 `data/journal`。
- 同一内容只在一处完整展开，跨层留互链。

## 档案分区

`data/profile/` 已迁出本仓，分区不再与记忆集一一对应：

| 分区 | 收什么 | 来源 |
|------|--------|------|
| `think/` | 认知档案：怎么想、怎么应对 | 各集日志蒸馏后按事情重组 |
| `work/` | 事项台账：事实、决定与下一步 | 各集日志中的在办事项 |
| `write/` | 创作认知地图与创作档案 | `write/` 日志 |

同一集日志可同时贡献多个分区；`think/` 允许跨集重组，不要求与记忆集同名。

## 目录与边界

| 层级 | 目录 | 内容特征 |
|------|------|---------|
| 时间线 | `<集>/journal/` | 原始日志，按日期记录 |
| 特征 | `data/profile/`（已迁出本仓） | 跨日期蒸馏的稳定特征，按用途分区 |
| 认知 | `<集>/insight/` | 想通的机制与规律，按实测分已确认/假说 |
| 方向 | `data/roadmap/<集>/`（已迁出本仓） | 愿景、选择、待定方向 |
| 对齐 | `<集>/intention/` | 人机协作的意图对齐信息（仅 `default/` 设此层） |

**边界规则**：

- 单次事件与业务状态不进 `data/profile/`，也不进 `<集>/insight/` 与 `<集>/roadmap/`——它们只存在于 `<集>/journal/` 时间线中。
- 人机协作中「要 X，不要 Y」的意图澄清归 `<集>/intention/`；沉淀为稳定判断后归 `data/profile/`，成形为决策后归 `<集>/roadmap/`，同一内容只在一处完整展开。
- 认识三分：想通的一句归 `<集>/insight/`，套用成框架归 `data/profile/think/`，引出的选择归 `<集>/roadmap/`；同一认识只在一处展开，跨层留互链。
- 决策（无论已/待）归 `<集>/roadmap/`；元目标是目标的子层，随目标归 `<集>/roadmap/`；跨时间稳定的个人特征归 `data/profile/`。
- `data/profile/` 只描述特征，不给建议；建议是对话输出，不是档案内容。
- **日志落位**：日志一律在 `<集>/journal/YYYY-MM-DD.md`，不设中间层；`qtfounder asset maintain` 把当天日期的文件留在原地，隔天搬进 `data/journal/<域>/`。

## 工作流

### 触发规则

日志更新后，分诊一次跑完，不必等用户再指示。读主仓的 `meta-classify`，同一遍日志分别更新 `data/insight/`、`data/intention/` 与 `data/roadmap/<集>/`（意图层目前只有 `default/` 启用）。

### Skill 索引

| Skill | 用途 | 路径 |
|-------|------|------|
| `meta-classify` | 判类、跨域、从日志分诊到各层、按类形状写入 | 随主仓的 `qtfounder` CLI 发布，装在 `~/.agents/skills/meta-classify/` |

## 相关文档

- [README](README.md)：仓库概述、目录树、数据流。
- [CONTRIBUTING](CONTRIBUTING.md)：工作原则、输出规范、提交规范、Skill 维护。
- [CHANGELOG](CHANGELOG.md)：版本变更记录。

## 如何维护 AGENTS.md

- 协作原则、输出规范、提交规范写进 [CONTRIBUTING.md](CONTRIBUTING.md)。
- 详细说明与工作流步骤写进主仓 `.agents/skills/` 的 Skill 文件。
- 目录结构与数据流写进 [README.md](README.md)。
- 记忆集、分层边界与触发规则留在本文件。

更新时机：新增记忆集、新增分层、触发规则变化时更新；README / CONTRIBUTING / Skill 已有的内容不重复。
