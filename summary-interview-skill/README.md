# summary-interview-skill

`summary-interview-skill` 用于围绕现有前端项目生成一套完整的“项目分析 -> 项目经验提炼 -> 面试题准备”文档。

## 外层入口

最外层统一入口文件是 [skill.md](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/skill.md)。

如果希望直接使用整套 skill，优先从这个入口文件开始，默认走 `summary-interview` 总入口，再按需拆分到单阶段 skill。

## 能力说明

该技能集包含 4 个 skill：

- `summary-interview`：总入口，串联完整流程。
- `init`：扫描前端项目架构、技术栈、目录职责和工程化配置。
- `project-insights`：基于架构文档提炼项目经验、亮点、难点与面试表达素材。
- `interview-questions`：基于前两阶段文档生成项目相关面试题与追问题。

## 项目结构

```text
summary-interview-skill/
├── skills/
│   ├── summary-interview/
│   ├── init/
│   ├── project-insights/
│   └── interview-questions/
├── skill.md
├── docs/
│   ├── README.md
│   ├── project-architecture/
│   ├── project-insights/
│   └── interview-questions/
└── README.md
```

结构说明：

- `skills/`：存放 4 个 skill 的定义文件和 UI 元数据。
- `skill.md`：最外层统一入口，说明如何调度整套 skill。
- `docs/`：存放所有阶段的产出文档，并按流程拆分子目录。
- 根目录 `README.md`：提供整体使用说明。

## 使用方式

### 推荐用法

优先直接触发 `summary-interview`，让流程按顺序执行：

```text
请使用 summary-interview skill，扫描当前前端项目，并在 docs 下沉淀项目架构、项目亮点难点和相关面试题。
```

### 分阶段用法

如果你只想执行其中一个阶段，也可以分别触发：

```text
请使用 init skill，扫描当前前端项目架构并沉淀到 docs/project-architecture。
```

```text
请使用 project-insights skill，基于 docs/project-architecture 提炼项目经验、亮点和难点。
```

```text
请使用 interview-questions skill，基于已有项目文档生成相关面试题示例和追问问题。
```

## 输出目录

执行后，文档默认生成在以下目录：

- `docs/README.md`
- `docs/project-architecture/`
- `docs/project-insights/`
- `docs/interview-questions/`

## 推荐流程

1. 先执行 `summary-interview` 或 `init`，沉淀项目架构与技术栈。
2. 再执行 `project-insights`，提炼项目经验、亮点和难点。
3. 最后执行 `interview-questions`，生成面试题、追问方向和回答提示。

## 文档说明

### `docs/project-architecture/`

- `README.md`：项目架构总览。
- `tech-stack.md`：技术栈分析。
- `project-structure.md`：目录结构与模块职责。
- `engineering.md`：工程化、环境和发布分析。

### `docs/project-insights/`

- `README.md`：项目经验总览。
- `highlights-and-challenges.md`：亮点、难点和解决思路。
- `interview-storylines.md`：适合面试表达的项目经历素材。

### `docs/interview-questions/`

- `README.md`：题目来源和使用方式。
- `frontend-interview-questions.md`：项目相关面试题示例。
- `follow-up-questions.md`：追问问题和回答提示。

## 注意事项

- 推荐先有真实项目代码，再触发技能，避免输出空泛结论。
- 后续阶段依赖前置文档，若 `docs/project-architecture/` 信息不足，提炼和出题质量会受影响。
- 文档应优先增量更新，不建议重复生成同主题文件。
- 推荐默认走 `summary-interview` 总入口，只有在明确需要单独阶段时再分开调用。
