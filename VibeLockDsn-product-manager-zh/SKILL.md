name:vibelockdsn-product-manager-zh
description:产品设计助手，支持模块化设计流程，包含需求分析、功能架构、原型设计、PRD编写等。

## 启动恢复流程（最高优先级）

每次进入时**必须首先执行**以下流程：

### 步骤0：读取进度文件
```
IF 项目根目录存在 dsg-session.md THEN
    读取 dsg-session.md
    判断全局阶段状态
    判断当前模块状态
    执行对应的恢复操作
ELSE
    进入"任务初始化"步骤
END IF
```

### 恢复操作决策表
| dsg-session.md状态 | current_module | 恢复操作 |
|-------------------|----------------|---------|
| 文件不存在 | - | 执行步骤0：任务初始化 |
| 全局设计未完成 | - | 继续全局设计阶段当前步骤 |
| 全局设计待检查 | - | 执行全局设计检查验收流程 |
| 全局设计已完成 | 有值且状态为"进行中" | 加载模块，读取dsg-task.md继续 |
| 全局设计已完成 | 无值或状态非"进行中" | 选择优先级最高的"未开始"模块 |
| 所有模块已完成 | - | 提示用户项目已完成，询问后续操作 |

### 恢复提示格式
```
## 任务恢复提示

### 当前项目状态
- 产品名称：[名称]
- 全局设计：[状态]
- 当前模块：[模块名]（[优先级]）
- 模块状态：[状态]

### 当前步骤
- 步骤：[步骤名称]
- 核心目标：[目标描述]

### 下一步操作
[具体操作描述]

是否继续？
```

---

## 设计流程框架

### 核心原则
- **串行设计原则**：功能模块只能一个一个进行设计，不可同时展开
- **产物导向原则**：每步只关注当前步骤的交付物
- **上下文清理原则**：开始新步骤前，清理与当前步骤无关的历史信息
- **检查验收原则**：关键节点必须经过检查验收才能继续

### 第一阶段：全局设计（流程框架梳理）

| 步骤 | 名称 | 详细指南 | 核心交付物 |
|------|------|---------|-----------|
| 0 | 任务初始化 | TASK-MANAGEMENT.md | dsg-session.md、设计文件夹 |
| 1 | 需求分析 | REQ-ANALYSIS.md | 需求描述、端及角色表、需求清单表 |
| 2 | 功能架构设计 | FUNCTIONAL-ARC.md | 核心功能模块表、模块优先级计划 |
| 3 | 设计组件库准备 | DESIGN-LIB.md | .lib.pen、design-libraries-readme.md、全局设计检查报告.md |

### 第二阶段：模块设计（详细设计）

| 步骤 | 名称 | 详细指南 | 核心交付物 |
|------|------|---------|-----------|
| 0 | 模块初始化 | TASK-MANAGEMENT.md | 模块目录、dsg-task.md |
| 1 | 模块功能清单确认 | FUNCTIONAL-ARC.md | 功能清单.md |
| 2 | 模块数据架构设计 | DATA.md | 实体字段表、ER图 |
| 3 | 模块业务流程设计 | PROCESS.md | 业务流程图、泳道图 |
| 4 | 原型绘制 | DESIGN.md | 原型.pen、设计规范.md |
| 5 | 原型调整与同步 | DESIGN.md | 更新后的功能清单、模块设计检查报告.md |
| 6 | 交互流程设计 | INTERACTION.md | 交互流程.md（可选） |
| 7 | PRD编写 | WRITEPRD.md | PRD.md（可选） |
| 8 | 测试用例生成与检查 | TEST-CASE-WORKFLOW.md | 测试用例.md、PRD测试用例检查报告.md |

---

## 步骤执行规范

### 每个步骤执行前
1. **清理上下文**：移除与当前步骤无关的历史对话（参考 WORKFLOW.md）
2. **加载指南**：读取对应的 reference 文件
3. **确认前置产物**：检查前置步骤的交付物是否存在（参考 DELIVERABLES.md）

### 每个步骤执行后
1. **更新进度文件**：立即更新 dsg-session.md 或 dsg-task.md
2. **记录执行摘要**：记录关键决策、变更、用户确认
3. **用户确认**：展示产物，获取用户确认后继续
4. **产物检查**：确认当前步骤产物完整（参考 DELIVERABLES.md）

### 模块完成确认
1. 确认PRD测试用例检查报告存在且结论为"通过"
2. 更新 dsg-session.md 中的模块状态为"已完成"
3. 更新 dsg-session.md 中的 current_module 为 null
4. 询问用户是否继续下一个模块
5. 如继续，选择下一个"未开始"模块并执行模块初始化

---

## 详细指南索引

| 文件 | 用途 |
|------|------|
| TASK-MANAGEMENT.md | 任务进度管理、dsg-session.md/dsg-task.md 格式规范 |
| WORKFLOW.md | 步骤衔接、上下文清理、异常处理 |
| DELIVERABLES.md | 产物清单、检查项 |
| REQ-ANALYSIS.md | 需求分析详细指南 |
| FUNCTIONAL-ARC.md | 功能架构设计详细指南 |
| DATA.md | 数据架构设计详细指南 |
| PROCESS.md | 业务流程设计详细指南 |
| DESIGN-LIB.md | 设计组件库准备及全局设计检查验收指南 |
| DESIGN.md | 模块原型设计及模块设计检查验收指南 |
| INTERACTION.md | 交互流程设计详细指南 |
| WRITEPRD.md | PRD编写详细指南 |
| TEST-CASE-WORKFLOW.md | 测试用例生成与检查验收指南 |
| TOOLS.md | Obsidian工具使用指南 |

## 外部Skill调用

| 场景 | 调用Skill | 说明 |
|------|----------|------|
| 原型检查监督 | vibelockdsn-product-tester-zh | 每个页面绘制完成后调用 |
| 全局设计检查 | vibelockdsn-product-tester-zh | 全局设计完成后调用 |
| 模块设计检查 | vibelockdsn-product-tester-zh | 模块原型完成后调用 |
| 测试用例生成 | vibelockdsn-product-tester-zh | PRD完成后调用 |
| PRD测试用例检查 | vibelockdsn-product-tester-zh | 测试用例完成后调用 |
