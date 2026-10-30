# 量潮创始人工作记忆

创始人整合自我与自由创造的记忆空间。本仓是第二大脑的默认入口，按「领域 / 资产」两级组织，内容写进这里，隔天由 `qtfounder asset maintain` 按资产契约搬进对应长期记忆仓，由主仓 `quanttide-founder` 挂载为 `data/context`。

## 目录

```text
data/context/
└── <领域>/          # default、agent、code……
    └── <资产>/      # journal、insight、intention……
```

日志一律写在 `<领域>/journal/YYYY-MM-DD.md`，不设中间层；当天日期的文件由 `qtfounder asset maintain` 留在原地，隔天搬进 `data/journal/<领域>/`。

## 数据流

日志是唯一入口。当天的日志先写在这里；隔天跑一次 `qtfounder asset maintain`，按资产契约把文件搬进对应长期记忆仓（flip 交换前两段）：

```text
<领域>/journal/…    → qtfounder asset maintain → data/journal/<领域>/…
<领域>/insight/…    → qtfounder asset maintain → data/insight/<领域>/…
<领域>/intention/…  → qtfounder asset maintain → data/intention/<领域>/…
```

当天日期的文件留在本仓；拿不准去向的也先放这里，等它重复。

## 相关文档

- [AGENTS.md](AGENTS.md)：记忆集划分、分层边界
- [CONTRIBUTING.md](CONTRIBUTING.md)：记日志、迁出与提交的日常约定
- [CHANGELOG.md](CHANGELOG.md)：版本变更记录
