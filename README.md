# 量潮创始人工作记忆

创始人整合自我与自由创造的记忆空间。本仓只保留 `default/`（创业与个人主线）一个集：日志在这里写入，成熟的档案、方向、洞察、意图与作品随做随迁到对应正式仓库，由主仓 `quanttide-founder` 挂载为 `data/context`。

## 目录

```text
data/context/
└── default/   # 创业与个人主线
```

当天日志写在集根（如 `default/2026-10-24.md`），便于手机端直接写；更早的日志平铺在 `default/journal/YYYY-MM-DD.md`。

## 数据流

日志是唯一入口。日志新增或修改后，一次分诊按 `meta-classify` 自动执行，无需人工指示：

```text
default/journal/（日志）→ meta-classify ─┬→ data/roadmap/<集>/（主题路线图）
                                        ├→ data/insight/（认知洞察）
                                        └→ data/intention/（意图对齐）
```

三条通道的取舍一致：只收跨时间稳定的内容。路线图收方向与先后顺序，洞察收能被后来的事推翻的机制与规律，意图收人机协作现场的澄清。感受、单次事件与业务状态只留在日志里。

## 相关文档

- [AGENTS.md](AGENTS.md)：记忆集划分、分层边界与蒸馏触发规则
- [CONTRIBUTING.md](CONTRIBUTING.md)：记日志、蒸馏、迁出与提交的日常约定
- [CHANGELOG.md](CHANGELOG.md)：版本变更记录
