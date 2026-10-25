# 量潮创始人工作记忆

创始人整合自我与自由创造的记忆空间。本仓是工作集：原始日志按主题域分集存放，蒸馏出的档案与方向层已迁到独立仓库，由主仓 `quanttide-founder` 挂载为 `data/context`。

## 目录

记忆按主题域分为 `default/`（创业与个人主线）、`life/`（生活）和 `work/`（工作主线）三个集：

```text
data/context/
├── default/   # 创业与个人主线
├── life/      # 生活
└── work/      # 工作主线
```

每个集都有 `README.md` 与 `journal/`。当天的日志写在集根（如 `default/2026-10-24.md`），便于手机端直接写；更早的日志平铺在 `journal/YYYY-MM-DD.md`。`work/` 按文档类型分 `bylaw/`、`handbook/` 子目录。档案、路线图与洞察已迁出本仓，`profile/`、`roadmap/`、`insight/` 不再在此保留。

## 数据流

日志是唯一入口。日志新增或修改后，一次分诊按 `meta-classify` 自动执行，无需人工指示：

```text
<集>/journal/（日志）→ meta-classify ─┬→ data/roadmap/<集>/（主题路线图）
                                      ├→ <集>/insight/（认知洞察）
                                      └→ <集>/intention/（意图对齐）
```

三条通道的取舍一致：只收跨时间稳定的内容。路线图收方向与先后顺序，洞察收能被后来的事推翻的机制与规律，意图收人机协作现场的澄清。感受、单次事件与业务状态只留在日志里。

## 相关文档

- [AGENTS.md](AGENTS.md)：记忆集划分、分层边界与蒸馏触发规则
- [CONTRIBUTING.md](CONTRIBUTING.md)：记日志、蒸馏、迁出与提交的日常约定
- [CHANGELOG.md](CHANGELOG.md)：版本变更记录
- [default/README.md](default/README.md)：`default/` 集的日志迁出判断与迁移方式
