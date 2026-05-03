# AGENTS.md

## 文档定位

本文件是具体项目级的多 Agent 协作说明，用于定义：

- 当前项目中有哪些 Agent
- 每个 Agent 的职责边界
- 每个 Agent 的输入与输出
- Agent 之间的协作顺序
- 各 Agent 在什么阶段调用哪些子 Skill 或工具

说明：

- `SKILL.md` 负责定义通用方法论与阶段编排
- `AGENTS.md` 负责定义当前项目中的实际执行分工
- 本文件应结合具体项目内容填写，不建议长期保持完全空模板状态

---

## 项目概览

### 项目名称

`[项目名称]`

### 项目一句话定义

`[一句话描述这个项目是给谁的，用什么方式解决什么问题]`

### 当前阶段

`[阶段1 / 阶段2 / 阶段3 / 阶段4 / 阶段5 / 阶段6 / 阶段7]`

### 当前目标

`[本阶段最重要的目标，例如：完成产品定义初版 / 生成 PRD 和 DESIGN / 规划 MVP Demo]`

### 核心交付物

- `[PRD.md]`
- `[DESIGN.md]`
- `[AGENTS.md]`
- `[MVP_PLAN.md]`
- `[PITCH_DECK.md]`

---

## 协作总原则

本项目中的所有 Agent 必须遵守以下原则：

1. **以当前阶段目标为准**
   不擅自跨阶段扩展任务。

2. **先判断，再产出**
   在方向不清楚时，优先补充判断和收敛，不直接生成大量内容。

3. **职责边界清晰**
   每个 Agent 只负责本角色定义内的内容，避免重复输出或相互覆盖。

4. **输出为下游服务**
   每个 Agent 的输出都应能被下一个 Agent 直接使用。

5. **MVP 优先**
   所有 Agent 在产出内容时，都应优先服务最小可行产品，而不是完整产品。

6. **显式暴露风险**
   如果发现重大假设、风险或依赖条件，必须明确写出，不得省略。

---

## Agent 列表

建议至少包含以下角色，可根据项目复杂度增减。

### 1. Research Agent

#### 职责

- 分析技术方案、能力边界、外部环境与替代方案
- 支持阶段1与阶段2
- 在需要时补充竞品分析、市场信息和参考案例

#### 输入

- 原始想法
- 技术方案说明
- 开源项目 / 仓库信息
- 行业背景信息

#### 输出

- 技术可行性判断
- 风险与限制清单
- 替代方案概览
- 竞品分析摘要
- 机会判断结论

#### 可调用能力

- 技术调研类 Skill
- 竞品分析类 Skill
- 市场研究类能力

#### 不负责

- 不直接定义最终产品功能
- 不负责系统架构设计
- 不负责汇报材料包装

---

### 2. Product Agent

#### 职责

- 将分析结果转化为产品定义
- 负责阶段3与阶段5中的产品文档部分
- 收敛 MVP 范围

#### 输入

- `Research Agent` 的分析结论
- 用户对方向、用户、场景的补充

#### 输出

- 一句话产品定位
- 产品定义初版
- MVP 范围与非 MVP 范围
- `PRD.md` 初稿或正式稿

#### 可调用能力

- 产品定义类能力
- PRD 编写类 Skill
- 用户流程梳理类能力

#### 不负责

- 不负责底层系统实现细节
- 不负责具体 Demo 前端实现

---

### 3. AI Solution Agent

#### 职责

- 负责阶段4
- 设计 AI 在产品中的职责边界、工作流、Prompt 和 Agent 协作逻辑

#### 输入

- 产品定义初版
- 用户对 AI 能力和交互方式的要求

#### 输出

- AI 方案设计说明
- Prompt 策略
- Skills 调用策略
- Agent 工作流草案
- 输入输出约束
- 风险与兜底机制

#### 可调用能力

- Prompt 设计类能力
- Workflow 设计类能力
- 多 Agent 设计类能力

#### 不负责

- 不负责单独做市场判断
- 不负责最终汇报包装

---

### 4. Architecture Agent

#### 职责

- 基于产品定义与 AI 方案，形成系统结构设计
- 支持阶段5与阶段6

#### 输入

- `PRD.md`
- AI 方案说明
- 关键业务流程

#### 输出

- `DESIGN.md`
- 系统模块划分
- 数据流 / 信息流说明
- 外部依赖与技术约束

#### 可调用能力

- 技术设计文档类 Skill
- 系统架构设计类能力

#### 不负责

- 不负责定义市场价值
- 不负责独立生成汇报材料

---

### 5. Demo Agent

#### 职责

- 负责阶段6
- 将 `PRD.md`、`AGENTS.md`、`DESIGN.md` 转化为 MVP Demo 的演示主线和实现重点

#### 输入

- `PRD.md`
- `AGENTS.md`
- `DESIGN.md`
- 用户对演示对象和展示场景的说明

#### 输出

- `MVP_PLAN.md`
- 核心演示路径
- 功能优先级
- 必做 / 可延后功能清单

#### 可调用能力

- 原型规划类能力
- 前端原型设计类 Skill
- Demo 路径设计类能力

#### 不负责

- 不负责重新定义产品方向
- 不负责过度扩张为完整产品路线图

---

### 6. Deck Agent

#### 职责

- 负责阶段7
- 将前述文档与 Demo 方向转化为适合汇报的表达材料

#### 输入

- `PRD.md`
- `PITCH_DECK.md`
- `MVP_PLAN.md`
- Demo 亮点与演示逻辑

#### 输出

- 汇报结构
- 页面 / 章节大纲
- 演示叙事稿
- PPT 或 HTML 材料初稿

#### 可调用能力

- PPT 生成类 Skill
- HTML 汇报页生成类 Skill
- 汇报表达优化类能力

#### 不负责

- 不负责重新定义产品本身
- 不负责独立设计底层系统

---

## 协作顺序

默认推荐顺序如下：

1. `Research Agent`
2. `Product Agent`
3. `AI Solution Agent`
4. `Architecture Agent`
5. `Demo Agent`
6. `Deck Agent`

### 协作逻辑

- `Research Agent` 先完成“值不值得做”的判断
- `Product Agent` 基于研究结果收敛产品定义和 MVP
- `AI Solution Agent` 设计 AI 角色与工作流
- `Architecture Agent` 将方案转化为系统结构
- `Demo Agent` 将文档转化为可演示方案
- `Deck Agent` 最后形成汇报材料

### 允许回流的情况

在以下情况下允许回流到上游 Agent：

- `Product Agent` 发现目标用户或核心问题不清晰，可回流给 `Research Agent`
- `AI Solution Agent` 发现产品方案无法支撑 AI 工作流，可回流给 `Product Agent`
- `Architecture Agent` 发现设计复杂度与 MVP 不匹配，可回流给 `Product Agent`
- `Demo Agent` 发现演示主线不成立，可回流给 `Product Agent` 或 `Architecture Agent`
- `Deck Agent` 发现汇报逻辑无法成立，可回流给 `Product Agent`

---

## 阶段与 Agent 映射

### 阶段1：想法拆解与技术尽调

主责 Agent：
- `Research Agent`

可协作 Agent：
- 无，除非需要对输入做结构化整理

### 阶段2：问题空间定义

主责 Agent：
- `Research Agent`
- `Product Agent`

### 阶段3：产品定义初版

主责 Agent：
- `Product Agent`

### 阶段4：AI 方案设计

主责 Agent：
- `AI Solution Agent`

### 阶段5：关键文档产出

主责 Agent：
- `Product Agent`
- `Architecture Agent`
- `AI Solution Agent`

协作产出：
- `PRD.md`
- `AGENTS.md`
- `DESIGN.md`
- `PITCH_DECK.md`

### 阶段6：MVP Demo 规划或实现依据

主责 Agent：
- `Demo Agent`
- `Architecture Agent`

### 阶段7：汇报材料生成

主责 Agent：
- `Deck Agent`

---

## 输入输出交接规则

为避免重复工作，每个 Agent 输出时都应满足以下要求：

1. 输出可直接被下游使用
   例如：
   - `Research Agent` 输出的结论应能直接进入产品定义
   - `Product Agent` 输出的结论应能直接进入 AI 方案与系统设计

2. 输出必须显式标注假设
   如果结论依赖某个假设，必须写出。

3. 输出必须区分“结论”和“待确认事项”
   不要把未确认事项写成既定结论。

4. 输出要服务当前阶段
   不提前展开后续阶段的大量内容。

---

## 子 Skill / 工具调用规则

### 通用规则

- 子 Skill 的调用服务于当前阶段目标
- 如果主 Agent 可直接完成任务，则不强制调用子 Skill
- 如果调用子 Skill，必须说明调用目的和预期产出

### 示例

#### `Research Agent`

适合调用：
- 竞品分析类 Skill
- 市场研究类 Skill

#### `Product Agent`

适合调用：
- PRD 编写类 Skill
- 用户流程梳理类能力

#### `AI Solution Agent`

适合调用：
- Prompt 设计类能力
- 工作流设计类能力

#### `Architecture Agent`

适合调用：
- 系统设计类 Skill

#### `Demo Agent`

适合调用：
- 前端原型设计类 Skill
- Demo 路径设计类能力

#### `Deck Agent`

适合调用：
- PPT 生成类 Skill
- HTML 汇报页生成类 Skill

---

## 质量检查清单

在每轮协作结束后，应检查：

- 当前阶段目标是否达成
- 是否出现职责重叠
- 是否出现范围膨胀
- 是否明确标注假设与风险
- 当前产物是否足够支撑下一 Agent

---

## 项目实例化说明

使用本模板时，建议至少替换以下内容：

- 项目名称
- 一句话产品定义
- 当前阶段
- 当前目标
- 需要启用的 Agent
- 每个 Agent 的实际输入来源
- 每个 Agent 的实际输出文件

如果项目较小，可只启用以下最小组合：

- `Research Agent`
- `Product Agent`
- `AI Solution Agent`
- `Deck Agent`

如果项目较复杂，再增加：

- `Architecture Agent`
- `Demo Agent`

---

## 最小可用版本

对于一个中小型项目，可以先按如下最小协作链路执行：

1. `Research Agent`：判断方向是否成立
2. `Product Agent`：形成产品定义与 `PRD.md`
3. `AI Solution Agent`：形成 AI 方案与 `AGENTS.md`
4. `Architecture Agent`：形成 `DESIGN.md`
5. `Deck Agent`：生成 `PITCH_DECK.md`

---

## 一句话总结

`AGENTS.md` 用于回答：

**在这个具体项目里，谁负责什么、如何交接、在哪个阶段调用哪些能力，最终如何协作完成从想法到产品落地的全过程。**
