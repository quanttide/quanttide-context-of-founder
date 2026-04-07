# 量潮创始人工作语境

本项目是量潮创始人工作语境的文档库，以 MYST Markdown 格式编写，使用 Jupyter Book 构建。

## 许可证

本项目采用 [CC BY 4.0](LICENSE) 许可证。

## 贡献指南

欢迎贡献！详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 格式规范

### 文件命名

- 使用小写字母
- 单词之间用下划线 `_` 分隔
- 示例：`context.md`、`project_context.md`、`decision_context.md`

### 目录结构

```
.
├── index.md           # 首页（内容总览）
├── README.md          # 格式规范与构建命令
├── CONTRIBUTING.md    # 贡献指南
├── _config.yml        # Jupyter Book 配置
├── _toc.yml           # 目录结构
├── AGENTS.md          # Agent 工作指南
├── CHANGELOG.md       # 版本变更记录
├── 板块名/            # 按主题划分的目录
│   ├── index.md       # 板块内容摘要
│   ├── README.md      # 板块说明（可选）
│   └── *.md           # 具体文档
└── _static/           # 静态资源（图片等）
```

### 目录命名

- 使用小写字母
- 使用复数形式
- 示例：`contexts/`、`scenarios/`、`decisions/`

### Markdown 规范

- 标题使用 ATX 风格（`#`、`##`、`###`）
- 代码块使用 fenced code（\`\`\`）
- 列表使用 `-` 或 `1.`
- 链接使用 `[文字](路径)` 格式
- 区块之间保留空行

## 构建命令

```bash
# 构建 HTML
jupyter-book build index.md --site

# 构建并预览
jupyter-book start .

# 清理构建文件
jupyter-book clean .
```

## 质量检查

### Linting

```bash
markdownlint "**/*.md"
```

### 验证清单

- [ ] 所有内部链接指向已存在的文件
- [ ] `_toc.yml` 中引用的文件均已创建
- [ ] YAML 文件语法正确
- [ ] 新增文件已添加到 `_toc.yml`
- [ ] 构建无错误
