# 协作与贡献指南

本仓是 `data/context` 的工作约定。目录结构、分层边界与触发规则见 [AGENTS.md](AGENTS.md)，变更记录见 [CHANGELOG.md](CHANGELOG.md)。

## 工作原则

### 最小干预
- 仅在用户明确请求时操作
- 不主动创建文件（除非必要）
- 优先编辑现有文件

### 原子提交
- 每次提交独立完整
- 不提交不完整的更改
- 验证后再提交

### 验证优先
- 修改后运行构建验证
- 确保更改符合预期

## 输出规范

### 内容格式
- 不使用 emoji（除非用户明确请求）
- 输出简洁，适合 CLI 显示

### 文件引用
- 使用 `code` 格式表示文件路径
- 每个引用独立，不合并

## Git 提交规范

遵循 Conventional Commits 格式：

| 类型 | 说明 |
|------|------|
| `docs` | 文档更新 |
| `refactor` | 重构 |
| `chore` | 构建/工具 |

## Skill 维护

Skill 文件统一在主仓 `quanttide-founder` 的 `.agents/skills/` 维护，本仓不自建；新增或修改后，只需同步 [AGENTS.md](AGENTS.md) 的「Skill 索引」与「触发规则」。

## 如何维护本文档

| 类型 | 写在哪里 |
|------|---------|
| 详细说明、工作流步骤 | `.agents/skills/` 中的 Skill 文件（主仓） |
| 协作原则、输出规范、提交规范 | CONTRIBUTING.md |
| 目录结构、分层边界、触发规则 | [AGENTS.md](AGENTS.md) |

更新时机：新增分层、新增记忆集、协作规则变化时更新。
