# Changelog

## 0.2.0

### Added

- 增强 `SKILL.md`，支持解决方案型项目、多设备协同系统和“本体设备 + 上层应用”模式
- 在方法层补充：
  - 本体能力与上层系统边界规则
  - 付费主体 / 场景优先级判断
  - 人工接管与安全兜底要求
- 新增核心模板：
  - `SOLUTION_BRIEF.template.md`
  - `SCENARIO_PLAYBOOK.template.md`
- 升级现有模板，使其更适合无人装备、机器人、IoT、安防巡检等场景
- 新增真实产业示例项目：
  - `examples/example_unmanned_patrol_system/`

### Changed

- `README.md` 更新为更正式的包结构说明
- `VERSION` 升级为 `0.2.0`
- `PRD.template.md`、`DESIGN.template.md`、`04_ai_solution_design.template.md` 增加解决方案型项目所需字段

### Notes

- `0.2.0` 开始，这个 Skill 不再只是偏通用 AI 产品，也开始面向多设备协同和行业解决方案型产品。

## 0.1.0

### Added

- 初始化 `idea-to-product` Skill 包主结构
- 新增 `SKILL.md`，包含：
  - 7 阶段流程
  - 启动协议
  - 默认决策规则
  - 子 Skill 调用策略
  - 模板引用策略
  - 文档生成规则
- 新增阶段模板：
  - `01_opportunity_brief.template.md`
  - `02_problem_space.template.md`
  - `03_product_definition.template.md`
  - `04_ai_solution_design.template.md`
- 新增核心文档模板：
  - `PRD.template.md`
  - `AGENTS.template.md`
  - `DESIGN.template.md`
  - `MVP_PLAN.template.md`
  - `PITCH_DECK.template.md`
- 新增完整示例项目：
  - `examples/example_ai_meeting_copilot/`
- 新增发布级说明文件：
  - `README.md`
  - `VERSION`
  - `CHANGELOG.md`

### Notes

- 当前版本为首版草案，适合内部使用、继续迭代和作为方法论包基础。
- `PRD.md` 采用“市场与竞品摘要 + 前置机会分析文档承载完整版研究”的边界设计。
