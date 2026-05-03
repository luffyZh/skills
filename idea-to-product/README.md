# idea-to-product

## 简介

`idea-to-product` 是一套从“想法 / 技术方案 / 能力原型”到“产品定义 / AI 方案 / MVP Demo / 汇报材料”的方法论 Skill 目录。

## 版本信息

- 当前版本：`0.1.0`
- 发布状态：`draft`
- 主入口文件：`SKILL.md`

它适用于：

- 只有一个模糊想法，想判断值不值得做
- 已有技术方案，想进一步产品化
- 基于 AI / Agent / 开源项目寻找产品方向
- 希望沉淀出 `PRD.md`、`AGENTS.md`、`DESIGN.md`、`MVP_PLAN.md`、`PITCH_DECK.md`

---

## 当前目录结构

```text
idea-to-product/
├── CHANGELOG.md
├── README.md
├── SKILL.md
├── VERSION
├── examples/
│   ├── README.md
│   └── example_ai_meeting_copilot/
│       ├── 01_opportunity_brief.md
│       ├── 02_problem_space.md
│       ├── 03_product_definition.md
│       ├── 04_ai_solution_design.md
│       ├── AGENTS.md
│       ├── DESIGN.md
│       ├── MVP_PLAN.md
│       ├── PITCH_DECK.md
│       ├── PRD.md
│       └── README.md
└── templates/
    ├── README.md
    ├── docs/
    │   ├── README.md
    │   ├── AGENTS.template.md
    │   ├── DESIGN.template.md
    │   ├── MVP_PLAN.template.md
    │   ├── PITCH_DECK.template.md
    │   └── PRD.template.md
    └── phase/
        ├── README.md
        ├── 01_opportunity_brief.template.md
        ├── 02_problem_space.template.md
        ├── 03_product_definition.template.md
        └── 04_ai_solution_design.template.md
```

---

## 文件说明

### 1. `SKILL.md`

这是总控 Skill 说明文件，负责定义：

- 7 阶段流程
- 启动协议
- 默认决策规则
- 子 Skill 调用策略
- 模板引用策略
- 文档生成规则

它回答的是：

**这套方法论应该怎么跑。**

---

### 2. `templates/phase/`

这组文件用于沉淀前四个阶段的过程性判断文档。

#### `01_opportunity_brief.template.md`

用于机会判断与前置分析，重点包括：

- 技术特点
- 市场规模
- 竞品格局
- 替代方案
- 切入机会
- Go / No-Go 判断

#### `02_problem_space.template.md`

用于定义：

- 目标用户
- 核心场景
- 核心痛点
- 当前替代方式
- 差异化价值

#### `03_product_definition.template.md`

用于收敛：

- 一句话产品定位
- 产品方案
- 核心价值
- MVP 范围

#### `04_ai_solution_design.template.md`

用于设计：

- AI 在产品中的角色
- Prompt 策略
- Skills / 工具调用策略
- Agent / Workflow
- 输入输出约束
- 风险与兜底机制

---

### 3. `templates/docs/`

这组文件用于生成执行型和表达型核心文档。

#### `PRD.template.md`

用于定义产品目标、用户、场景、功能与指标。

注意：

- `PRD.md` 包含的是**市场与竞品摘要**
- 完整版市场规模、竞品格局、替代方案分析，优先放在 `01_opportunity_brief.md`

#### `AGENTS.template.md`

用于定义具体项目中的多 Agent 分工，包括：

- Agent 列表
- 每个 Agent 的职责
- 输入 / 输出
- 协作顺序
- 子 Skill / 工具调用规则

#### `DESIGN.template.md`

用于描述 MVP 或原型系统的结构设计，包括：

- 系统目标
- 模块划分
- 数据流 / 信息流
- 外部依赖
- 风险与约束

#### `MVP_PLAN.template.md`

用于将产品定义转化为 Demo 计划，包括：

- Demo 目标
- 核心演示主线
- 必做功能
- 可延后功能
- 演示建议

#### `PITCH_DECK.template.md`

用于组织汇报材料结构，可进一步生成 PPT 或 HTML 汇报页。

---

## PRD 与机会分析文档的边界

这是这套体系里非常重要的一条规则：

### `01_opportunity_brief.md`

负责完整版的：

- 市场规模
- 竞品格局
- 替代方案
- 切入机会
- 为什么值得做

### `PRD.md`

负责精简版的：

- 背景与机会摘要
- 市场与竞品摘要
- 为什么这个产品值得立项
- 这些结论如何转化为产品目标、用户、功能和 MVP

### 设计原则

不要把 PRD 写成一份很长的市场研究报告。  
更好的做法是：

- 机会分析文档负责“研究与判断”
- PRD 负责“产品定义与执行”

---

## 建议使用方式

### 方式一：按阶段推进

1. 先参考 `SKILL.md`
2. 从 `templates/phase/01_opportunity_brief.template.md` 开始
3. 依次推进到：
   - `02_problem_space`
   - `03_product_definition`
   - `04_ai_solution_design`
4. 再进入 `templates/docs/` 中的核心文档

推荐顺序：

1. 先阅读 `README.md`
2. 再阅读 `SKILL.md`
3. 根据阶段选择 `templates/phase/` 或 `templates/docs/`
4. 如需快速上手，可直接参考 `examples/`

### 方式二：快速生成核心交付物

如果前面已经想清楚了，也可以直接用：

- `PRD.template.md`
- `AGENTS.template.md`
- `DESIGN.template.md`
- `MVP_PLAN.template.md`
- `PITCH_DECK.template.md`

---

## 当前已包含的模板清单

### phase 模板

- `templates/phase/01_opportunity_brief.template.md`
- `templates/phase/02_problem_space.template.md`
- `templates/phase/03_product_definition.template.md`
- `templates/phase/04_ai_solution_design.template.md`

### docs 模板

- `templates/docs/AGENTS.template.md`
- `templates/docs/PRD.template.md`
- `templates/docs/DESIGN.template.md`
- `templates/docs/MVP_PLAN.template.md`
- `templates/docs/PITCH_DECK.template.md`

---

## 目录规范

### 顶层文件

- `SKILL.md`：方法论与执行规范主文件
- `README.md`：使用说明与目录导航
- `CHANGELOG.md`：版本变更记录
- `VERSION`：当前版本号

### `templates/`

- `phase/`：阶段性分析与判断模板
- `docs/`：执行型和表达型核心文档模板

### `examples/`

- 放置完整示例项目
- 用于展示模板如何落地成真实文档

### 命名约定

- 阶段文档采用数字前缀，如 `01_`、`02_`
- 通用模板采用 `*.template.md`
- 项目实例文档使用正式文件名，如 `PRD.md`、`AGENTS.md`

---

## 一句话总结

这个目录的职责是：

**用一套统一的方法论，把“想法”逐步推进成“可定义、可实现、可演示、可汇报”的产品化结果。**
