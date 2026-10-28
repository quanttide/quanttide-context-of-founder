它缺一个设计操作系统，只有一堆风格碎片。

别让模型直接吐像素或 Widget 树，让它在一个强约束的中间层里做选择。模型负责”意图与取舍“，确定性系统负责”落地与校验“。

{
  ”intent“: ”quick_scan“,        // 任务类型：扫读/对比/沉浸式阅读/录入
  ”primary“: ”current_price“,    // 唯一视觉锚点
  ”hierarchy“: [”price“, ”trend_24h“, ”volume“, ”detail_tabs“],
  ”density“: ”compact“,          // sparse | compact | rich
  ”tone“: ”data_cool“,
  ”max_elements“: 7,             // 硬预算
  ”avoid“: [”gradient_card“, ”emoji_icon“, ”redundant_label“]
}

这是计算设计真正发力的地方。DSL 进来后，由一个不会犯错的老工程师（代码）去算：

• 信息预算：7±2 原则，首屏元素数超了直接报错回退

• 栅格与间距系统：8pt 基准，间距只许取 [4,8,12,16,24,40] 这个离散集合，禁止 13、17 这种野值

• 字号阶梯：定义一条 modular scale（如 1.25 倍率），层级差不够一个台阶就拒绝

• 视觉重量守恒：页面只有一个 weight: 1.0 的锚点，其余 ≤0.6，避免”五个标题抢眼球“

• 可访问性硬约束：对比度 WCAG AA、触控区 ≥44pt、禁用纯色彩编码

• 布局有效性：用 Flutter 的 TextPainter / CustomPainter 预演一次，溢出即重排

这一步完全不用模型，快、可验证、可测试。

