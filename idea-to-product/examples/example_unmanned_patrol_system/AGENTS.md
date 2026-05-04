# AGENTS.md

## 项目概览

### 项目名称

无人装备 AI 巡航系统

### 项目一句话定义

一套通过无人机与机器狗协同完成园区重点区域巡航、异常复核与中控上报的上层应用系统。

### 当前目标

形成一套可用于演示和方案汇报的 MVP 原型文档体系。

## Agent 列表

### 1. Research Agent

#### 职责

- 研究园区安防、无人巡逻和行业替代方案
- 判断本体设备与上层系统的产品边界

#### 输出

- `01_opportunity_brief.md`
- 竞品与替代方案摘要

### 2. Product Agent

#### 职责

- 定义产品切入场景和 MVP
- 编写 `PRD.md`
- 收敛第一条演示主线

#### 输出

- `03_product_definition.md`
- `PRD.md`

### 3. AI Solution Agent

#### 职责

- 设计识别、风险初判、调度建议与告警生成工作流

#### 输出

- `04_ai_solution_design.md`
- `SCENARIO_PLAYBOOK.md`

### 4. Solution Architect Agent

#### 职责

- 明确本体能力边界与上层系统边界
- 形成场景化方案结构与系统设计

#### 输出

- `SOLUTION_BRIEF.md`
- `DESIGN.md`

### 5. Demo Agent

#### 职责

- 将方案收敛为一条可演示的 MVP 业务链路

#### 输出

- `MVP_PLAN.md`

### 6. Deck Agent

#### 职责

- 将文档和 Demo 方案转化为对外汇报结构

#### 输出

- `PITCH_DECK.md`

## 协作顺序

1. `Research Agent`
2. `Product Agent`
3. `AI Solution Agent`
4. `Solution Architect Agent`
5. `Demo Agent`
6. `Deck Agent`

## 子 Skill / 工具调用

- `Research Agent` 可调用行业研究与竞品分析能力
- `Product Agent` 可调用 PRD 编写能力
- `AI Solution Agent` 可调用工作流设计和 Agent 设计能力
- `Deck Agent` 可调用 PPT / HTML 汇报生成能力
