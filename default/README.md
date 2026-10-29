# default 集迁出规则

本集收拿不准去向的内容与原始日志；一旦内容明确属于某个资产仓，随做随迁，来源侧不留复制件。现行规则以 `qtfounder asset maintain` 的资产契约为准，不再单设去向表。

## 怎么迁

`default/<资产>/<余下>` 按 flip 交换前两段搬进资产仓，`default/insight/x.md` → `data/insight/default/x.md`，`journal`、`intention` 同理。当天日期的日志留在本集，隔天再搬。契约里没有的资产可以新建：首段当新资产名，落到同级资产仓（如 `data/create/`）。

```bash
qtfounder asset maintain --dry-run   # 预览
qtfounder asset maintain             # 搬
```

## 留在本集

个人感受、边界体验、状态收束语、日志管理元规则本身。
