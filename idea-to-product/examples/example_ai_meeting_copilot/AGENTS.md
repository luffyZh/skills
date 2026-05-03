# AGENTS.md

## 项目概览

### 项目名称

Meeting Copilot

### 项目一句话定义

帮助中小团队在会议结束后自动完成纪要、行动项和会后跟进输出的 AI 会议助手。

### 当前目标

完成一个可用于领导或客户演示的 MVP Demo。

## Agent 列表

### 1. Research Agent

#### 职责

- 分析会议协作工具赛道
- 判断差异化切入点

#### 输出

- 机会分析
- 竞品摘要

### 2. Product Agent

#### 职责

- 形成产品定义
- 编写 `PRD.md`

#### 输出

- 产品定位
- MVP 范围
- `PRD.md`

### 3. AI Solution Agent

#### 职责

- 设计摘要、行动项提取和审核工作流

#### 输出

- `04_ai_solution_design.md`
- Prompt 与流程规则

### 4. Architecture Agent

#### 职责

- 形成系统结构设计

#### 输出

- `DESIGN.md`

### 5. Demo Agent

#### 职责

- 规划演示主线
- 收敛 MVP 功能

#### 输出

- `MVP_PLAN.md`

### 6. Deck Agent

#### 职责

- 形成汇报结构

#### 输出

- `PITCH_DECK.md`

## 协作顺序

1. `Research Agent`
2. `Product Agent`
3. `AI Solution Agent`
4. `Architecture Agent`
5. `Demo Agent`
6. `Deck Agent`

## 子 Skill / 工具调用

- `Research Agent` 可调用竞品分析能力
- `Product Agent` 可调用 PRD 编写能力
- `Deck Agent` 可调用 PPT / HTML 生成能力
