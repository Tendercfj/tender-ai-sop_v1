---
name: init
description: 当用户需要扫描现有前端项目、梳理技术栈、分析目录职责或初始化项目认知时，扫描项目架构并将结果沉淀到 docs/project-architecture/ 目录。
---

# 前端项目初始化分析指南

`init` skill 的目标是快速建立对现有前端项目的结构化认知，并把扫描结果沉淀到 `docs/project-architecture/` 中，便于后续继续维护、交接和扩展。

## 触发方式

适合以下场景：

- 用户要求扫描当前前端项目结构。
- 用户要求梳理技术栈、目录职责、工程化配置。
- 用户刚接手项目，希望先输出项目初始化分析文档。

示例提示词：

- “请扫描这个前端项目，并把架构分析写到 docs 里。”
- “请梳理当前项目的技术栈、目录结构和工程化配置。”

## 阶段定位

这是整个技能集的第一阶段，优先为 `project-insights` 和 `interview-questions` 提供基础依据。

## 输出要求

如果 `docs/project-architecture/` 不存在，则创建该目录；如果已存在，则基于现状增量更新，避免重复创建相同主题文档。

默认产出以下文档：

- `docs/project-architecture/README.md`：项目总览、核心结论、入口信息。
- `docs/project-architecture/tech-stack.md`：技术栈、依赖、构建与运行方式。
- `docs/project-architecture/project-structure.md`：目录结构、模块职责、页面与公共能力拆分。
- `docs/project-architecture/engineering.md`：工程化配置、代码规范、环境变量、发布与质量保障方式。

如果项目规模较小，可以合并为更少的文档；如果项目复杂，可以补充同目录下的新文档，但不要输出到 `docs/` 之外。

## 扫描范围

优先基于真实代码和配置判断，不要凭文件名臆测。至少检查以下内容：

1. 根目录关键文件：`package.json`、锁文件、`tsconfig*`、`jsconfig*`、`vite.config*`、`webpack*`、`next.config*`、`nuxt.config*`、`tailwind.config*`、`postcss.config*`、`eslint*`、`prettier*`、`.env*`。
2. 应用目录：`src/`、`app/`、`pages/`、`components/`、`views/`、`layouts/`、`router/`、`store/`、`services/`、`api/`、`hooks/`、`composables/`、`utils/`、`styles/`。
3. 运行与构建线索：`scripts`、CI/CD 配置、容器配置、代理配置、部署脚本。
4. UI 与状态管理线索：组件库、样式方案、路由方案、状态管理、请求封装、权限方案、多语言方案。

## 执行流程

1. 先从根目录配置判断框架与工具链，例如 React、Vue、Angular、Vite、Webpack、Next.js、Tailwind CSS、TypeScript。
2. 再扫描源码目录，梳理页面层、组件层、状态层、服务层和基础设施层的职责边界。
3. 结合 `package.json` 的依赖与脚本，确认开发、构建、测试、Lint、格式化等工程能力是否存在。
4. 发现别名、环境变量、自动生成代码、主题系统、设计系统或 monorepo 结构时，单独记录。
5. 将结论写入 `docs/project-architecture/`，优先沉淀“已确认信息”，对无法确认的内容明确标记“待确认”与依据。

## 文档写法

- 只记录从仓库中可以验证的信息。
- 每条结论尽量附带依据来源，例如配置文件、目录、脚本或依赖名。
- 保持面向接手者可读，优先写“项目是怎么组织的”和“关键技术为什么存在”。
- 不要泛泛介绍通用技术概念，聚焦当前项目实际使用情况。
- 不要修改业务代码；此 skill 的主要产出是分析和文档沉淀。

## 推荐文档结构

### `README.md`

- 项目定位与入口
- 核心框架与运行方式
- 目录导航
- 关键工程结论

### `tech-stack.md`

- 框架与语言
- 构建工具与包管理器
- UI 技术方案
- 路由、状态管理、数据请求方案
- 测试与代码质量工具

### `project-structure.md`

- 根目录结构说明
- `src` 或主应用目录拆分
- 页面、组件、服务、工具模块职责
- 重要模块之间的调用关系

### `engineering.md`

- 环境变量与多环境配置
- 代码规范与提交流程
- 构建发布链路
- 性能、监控、埋点或国际化等补充能力

## 质量标准

- 文档内容要能帮助新成员在短时间内理解项目。
- 文档命名、标题和术语要统一。
- 如果项目已有现成文档，优先更新现有文档，而不是生成冲突版本。
- 如果仓库不是前端项目，要明确指出，并说明识别依据。
