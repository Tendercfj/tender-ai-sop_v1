# tender-ai-sop_v1

## summary-interview-skill 简介

`summary-interview-skill` 是一个面向前端项目总结与面试准备的技能集，用于围绕真实项目代码生成一套完整的文档沉淀链路：

- 扫描现有前端项目架构与技术栈。
- 提炼项目经验、技术亮点、工程亮点和实现难点。
- 生成贴合当前项目背景的前端面试题、追问问题和回答提示。

它适合以下场景：

- 接手陌生前端项目，希望快速完成项目认知。
- 想把项目经历整理成可复盘、可面试表达的材料。
- 想基于真实项目文档准备技术面试，而不是只看通用八股题。

## 技能组成

`summary-interview-skill` 包含 4 个 skill：

- `summary-interview`：总入口，串联完整流程。
- `init`：扫描项目架构并输出技术栈、目录结构、工程化分析。
- `project-insights`：提炼项目亮点、难点、经验和面试表达素材。
- `interview-questions`：生成项目相关面试题、追问方向和回答提示。

## 使用方法

### 推荐方式

优先直接使用 `summary-interview`，一次性完成完整流程：

```text
请使用 summary-interview skill，扫描当前前端项目，并在 docs 下沉淀项目架构、项目亮点难点和相关面试题。
```

### 分阶段使用

如果你只想执行某个阶段，可以单独调用对应 skill：

```text
请使用 init skill，扫描当前前端项目架构并沉淀到 docs/project-architecture。
```

```text
请使用 project-insights skill，基于 docs/project-architecture 提炼项目经验、亮点和难点。
```

```text
请使用 interview-questions skill，基于已有项目文档生成相关面试题示例和追问问题。
```

如果你希望从 `summary-interview-skill` 目录最外层进入，可以直接查看入口文件 [summary-interview-skill/skill.md](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/skill.md)。

## 输出位置

所有文档默认生成在 [summary-interview-skill/docs](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/docs) 下：

- [docs/README.md](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/docs/README.md)：总索引。
- [docs/project-architecture](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/docs/project-architecture)：项目架构与技术栈分析。
- [docs/project-insights](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/docs/project-insights)：项目经验、亮点与难点提炼。
- [docs/interview-questions](/Users/tender/Desktop/Tender/tender-ai-sop_v1/summary-interview-skill/docs/interview-questions)：面试题与追问问题。

## 使用建议

1. 先确保仓库里有真实前端项目代码或已有项目分析资料。
2. 首次使用时优先走 `summary-interview` 或 `init`。
3. 如果已经有 `docs/project-architecture/`，可以直接执行后续阶段。
4. 文档建议增量更新，避免重复生成同主题内容。
