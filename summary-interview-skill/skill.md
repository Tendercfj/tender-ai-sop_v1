# summary-interview-skill 入口

这个文件是 `summary-interview-skill` 在最外层的统一入口，用于说明如何使用整套 skill 完成前端项目总结与面试准备。

## 推荐入口

默认优先使用 `summary-interview`，它会按顺序串联以下 3 个阶段：

1. `init`：扫描前端项目架构，沉淀技术栈、目录结构和工程化分析。
2. `project-insights`：基于架构文档提炼项目经验、亮点、难点和面试表达素材。
3. `interview-questions`：基于前两阶段文档生成项目相关面试题、追问问题和回答提示。

## 推荐调用方式

```text
请使用 summary-interview skill，完整分析当前前端项目，并在 docs 下输出项目架构、项目亮点难点和面试题。
```

## 分阶段调用方式

如果只需要某一部分，也可以单独调用：

```text
请使用 init skill，扫描当前前端项目架构并沉淀到 docs/project-architecture。
```

```text
请使用 project-insights skill，基于 docs/project-architecture 提炼项目经验、亮点和难点。
```

```text
请使用 interview-questions skill，基于已有项目文档生成相关面试题示例和追问问题。
```

## 输出位置

所有产出统一沉淀到 `docs/` 下：

- `docs/project-architecture/`
- `docs/project-insights/`
- `docs/interview-questions/`

## 相关说明

- 详细使用说明见 `README.md`。
- 文档索引见 `docs/README.md`。
- skill 定义位于 `.codex/skills/`。
