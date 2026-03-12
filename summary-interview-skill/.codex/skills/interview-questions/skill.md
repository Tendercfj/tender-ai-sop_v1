---
name: interview-questions
description: 当用户需要基于真实项目前端架构和项目经验生成面试题、追问问题或回答思路时，基于 docs/project-architecture/ 与 docs/project-insights/ 输出 docs/interview-questions/ 文档。
---

# 项目面试题生成指南

`interview-questions` skill 用于基于已有项目分析文档，生成更贴近真实项目的前端面试题示例，帮助围绕项目经历进行模拟面试和准备追问。

## 触发方式

适合以下场景：

- 用户希望生成基于当前项目的前端面试题。
- 用户希望围绕项目亮点、难点准备追问问题。
- 用户需要一组贴近真实项目背景的模拟面试素材。

示例提示词：

- “请基于当前项目文档生成一组前端面试题。”
- “请围绕这个项目的亮点和难点补一组追问问题。”

## 阶段定位

这是整个技能集的第三阶段，优先基于 `docs/project-architecture/` 和 `docs/project-insights/` 生成面试题与追问材料。

## 输入前提

优先读取以下文档：

- `docs/project-architecture/README.md`
- `docs/project-architecture/tech-stack.md`
- `docs/project-architecture/project-structure.md`
- `docs/project-architecture/engineering.md`
- `docs/project-insights/highlights-and-challenges.md`
- `docs/project-insights/interview-storylines.md`

如果 `docs/project-insights/` 尚未生成，则可以仅基于 `docs/project-architecture/` 输出，但要在文档中说明题目深度可能受限。

## 输出要求

将内容统一沉淀到 `docs/interview-questions/`。如果目录不存在则创建，已存在则增量更新。

默认产出以下文档：

- `docs/interview-questions/README.md`：题目范围、生成依据、建议使用方式。
- `docs/interview-questions/frontend-interview-questions.md`：项目相关面试题示例。
- `docs/interview-questions/follow-up-questions.md`：围绕亮点和难点的追问问题、考察点与回答提示。

如果项目的技术面很复杂，可以补充同目录下的新文档，但不要输出到 `docs/` 之外。

## 题目生成原则

1. 题目必须尽量贴合当前项目实际技术栈和架构特点。
2. 优先围绕项目亮点、难点、架构决策、工程化能力、性能优化、组件设计、状态管理和发布流程出题。
3. 同时覆盖基础题、进阶题和追问题，避免只有宽泛八股题。
4. 题目中涉及项目事实时，必须能从已有文档中找到依据。
5. 如果某一方向证据不足，可以生成“可延展讨论题”，但需标注是基于现有线索推导。

## 执行流程

1. 先梳理项目的核心技术栈、架构特点、亮点和难点。
2. 按主题归类生成题目，例如框架设计、工程化、性能、协作与交付。
3. 为每个题目补充考察点，必要时补充参考回答思路。
4. 对明显适合深挖的亮点和难点，再生成一组追问问题。
5. 将结果写入 `docs/interview-questions/`，保证题目与项目背景关联清晰。

## 文档写法

- 题目描述尽量简洁，避免泛化成脱离项目背景的模板题。
- 参考回答思路只提供方向和要点，不伪造项目中不存在的事实。
- 对“基础题”和“项目题”做适当区分，方便不同阶段准备。
- 追问问题优先围绕方案取舍、边界条件、问题复盘和可优化空间。

## 推荐文档结构

### `README.md`

- 题目来源
- 使用方式
- 推荐练习顺序

### `frontend-interview-questions.md`

- 基础题
- 项目结合题
- 架构与工程化题

### `follow-up-questions.md`

- 针对亮点的追问
- 针对难点的追问
- 针对方案取舍的追问
- 参考回答要点

## 质量标准

- 题目应能真实反映当前项目的技术特征。
- 题目层次要有区分，不能全部停留在概念层。
- 追问方向要能帮助暴露理解深度。
- 如果项目信息不足，应明确标注，不强行扩写。
