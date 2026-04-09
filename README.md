# VibeLockDsn

<p align="center">
  <a href="#中文介绍">中文</a> | <a href="#english-version">English</a>
</p>

---

## 中文介绍

通过这套技能集，让你的 Vibe Design 过程变得严谨高效，实现 Agentic Engineering，帮助你实现企业级产品经理的agent设计及开发、测试及落地。

## 核心方法论：Harness

本技能集采用 **Harness 方法**构建，具有以下四大核心特色：

### 1. 工程化管理
- **角色分离**：产品、开发、测试三个角色独立运作，各司其职
- **过程拆解**：每个角色的工作流程被拆解为清晰的步骤，确保可执行性
- **标准化产出**：每个步骤都有明确的交付物规范，保证输出质量

### 2. 上下文窗口管理
- **Session 机制**：通过 `dsg-session.md` 和 `dev-session.md` 记录进度状态
- **Tasks 目录**：规范每个步骤的产物存储，实现结构化的消息传递
- **上下文清空**：通过文件系统持久化，有效管理 LLM 上下文窗口，避免信息过载

### 3. 评估与观测机制
- **第三方约束**：通过独立的测试验收 skill 约束和管理产出物
- **质量把关**：设计阶段和开发阶段都有独立的检查验收流程
- **问题闭环**：发现问题必须修复并回归检查，确保质量可控

### 4. 蒸馏设计风格 ✨
- **独家原创**：从现有系统截图中提取设计规范，快速建立设计标准
- **智能识别**：深度识别 UI 元素、布局结构、颜色方案、交互模式
- **即插即用**：生成的组件库和设计文档可直接用于新项目开发

## 项目结构

本项目包含四个核心技能模块：

### 1. VibeLockDsn-product-manager-zh（产品经理技能）
负责产品设计全流程，包括：
- 需求分析与拆解
- 功能架构规划
- 流程架构规划
- 数据架构规划
- 交互规划
- 原型 UI 设计
- PRD 文档输出
- 测试用例编写

### 2. VibeLockDsn-product-developer-zh（产品开发者技能）
负责产品开发全流程，采用架构师统管下的分工协作模式：
- 前端工程师：负责 UI 开发与交互实现
- 后端工程师：负责业务逻辑与数据层
- 测试工程师：负责质量保障与测试
- 运维工程师：负责部署与运维

### 3. VibeLockDsn-product-tester-zh（产品测试验收技能）✨ 新增
负责产品测试与验收全流程，独立于设计和开发，确保质量：
- **设计阶段检查**：全局设计检查、模块设计检查、PRD/测试用例检查
- **原型检查监督**：原型绘制过程中的质量监督
- **开发阶段测试**：模块测试执行、集成测试执行
- **项目验收**：最终验收与交付确认

### 4. VibeLockDsn-design-distillation-zh（设计风格蒸馏技能）✨ 新增
专门用于拆解企业管理系统 Web/App 页面截图，能够：
- 深度识别截图中的核心 UI 元素、页面框架结构、颜色方案、交互模式
- 自动过滤无关元素，提取有效设计信息
- 生成 AI 友好的设计风格 MD 文档
- 在 pencil 工具中绘制完整组件库
- 检查组件完整性并保存 .pen 文件
- 生成组件使用说明文档

## 如何使用

### 安装步骤

#### 1. 选择语言版本
中文用户使用 `-zh` 后缀的技能，英文用户使用无后缀版本

#### 2. 安装技能
将技能文件夹下载并安装到你的 Coding Agent（如 Claude Code、Cursor、Trae 等）的 skills 根目录下

#### 3. 安装配套工具

##### Obsidian 安装
```bash
# macOS
brew install --cask obsidian

# Windows
# 从官网下载安装包：https://obsidian.md/download

# Linux
sudo snap install obsidian --classic
```

##### Pencil 安装
```bash
# 访问官网下载对应平台安装包
# https://pencil.evolus.vn/

# macOS 也可以使用
brew install --cask pencil
```

##### Obsidian 官方 Skill 安装
```bash
# 方法1：通过 npm 安装（如果可用）
npm install -g @anthropic-ai/claude-code

# 方法2：手动安装
# 1. 访问 Obsidian 官方 Skill 仓库
# 2. 下载最新版本
# 3. 将 skill 文件夹放置到你的 Coding Agent 的 skills 目录下
```

### 使用流程
1. **设计风格蒸馏**（可选）：使用 `/VibeLockDsn-design-distillation-zh` 拆解现有系统截图，快速建立设计规范
2. **产品设计**：使用 `/VibeLockDsn-product-manager-zh` 完成需求分析、架构设计、原型设计等
3. **设计验收**：使用 `/VibeLockDsn-product-tester-zh` 对设计产物进行检查验收（设计阶段）
4. **产品开发**：使用 `/VibeLockDsn-product-developer-zh` 进行模块化开发、测试和部署
5. **测试验收**：使用 `/VibeLockDsn-product-tester-zh` 执行测试和项目验收（开发阶段）

### 工作流特点
- **模块化设计**：支持按模块逐步推进，每个模块可独立设计、开发、测试
- **进度持久化**：通过 session 文件记录进度，支持随时中断和恢复
- **多角色协作**：模拟真实团队协作模式，各司其职又紧密配合
- **独立测试验收**：测试验收独立于设计和开发，确保客观公正的质量保障
- **全流程覆盖**：从设计提炼到最终验收，完整覆盖产品全生命周期

## 核心优势

相比传统的 Vibe Coding 和 Vibe Design：

| 传统方式 | VibeLockDsn 方式 |
|---------|-----------------|
| 依赖多轮 Prompt 对话 | 结构化工作流引导 |
| 难以处理复杂架构 | 系统化的架构设计方法 |
| 缺乏进度管理 | 完善的进度持久化机制 |
| 单一角色视角 | 多角色协作模式 |
| 设计规范不统一 | 可从现有系统提炼设计规范 |
| 缺乏独立测试验收 | 独立的测试验收流程，确保质量 |

## 适用场景

- ✅ 企业级管理系统开发
- ✅ 复杂业务流程应用
- ✅ 需要严格设计规范的项目
- ✅ 团队协作开发场景
- ✅ 从现有系统重构或迁移

## 写在结尾

这个想法和场景还在不断完善中，真诚期望您的试用与反馈，我们一起来打造更好用的方法！

---

## English Version

With this skill set, make your Vibe Design process rigorous and efficient, achieving Agentic Engineering.

## Core Methodology: Harness

This skill set is built using the **Harness Method** with four core features:

### 1. Engineering Management
- **Role Separation**: Product, development, and testing roles operate independently with clear responsibilities
- **Process Decomposition**: Each role's workflow is decomposed into clear steps for executability
- **Standardized Outputs**: Each step has defined deliverable specifications to ensure output quality

### 2. Context Window Management
- **Session Mechanism**: Progress tracking through `dsg-session.md` and `dev-session.md`
- **Tasks Directory**: Standardized storage for each step's deliverables, enabling structured message passing
- **Context Clearing**: File system persistence effectively manages LLM context windows, avoiding information overload

### 3. Evaluation & Observation Mechanism
- **Third-party Constraints**: Independent testing & acceptance skill constrains and manages deliverables
- **Quality Assurance**: Both design and development phases have independent inspection and acceptance processes
- **Issue Closure**: Issues must be fixed and regression-checked to ensure quality control

### 4. Design Style Distillation ✨
- **Original Innovation**: Extract design specifications from existing system screenshots to quickly establish design standards
- **Intelligent Recognition**: Deep recognition of UI elements, layout structures, color schemes, and interaction patterns
- **Plug-and-Play**: Generated component libraries and design documents can be directly used in new project development

## Project Structure

This project contains four core skill modules:

### 1. VibeLockDsn-product-manager (Product Manager Skill)
Responsible for the entire product design process, including:
- Requirements analysis and breakdown
- Functional architecture planning
- Process architecture planning
- Data architecture planning
- Interaction planning
- Prototype UI design
- PRD document output
- Test case writing

### 2. VibeLockDsn-product-developer (Product Developer Skill)
Responsible for the entire product development process, adopting a collaborative model under architect leadership:
- Frontend Engineer: UI development and interaction implementation
- Backend Engineer: Business logic and data layer
- Test Engineer: Quality assurance and testing
- DevOps Engineer: Deployment and operations

### 3. VibeLockDsn-product-tester (Product Testing & Acceptance Skill) ✨ NEW
Responsible for the entire product testing and acceptance process, independent of design and development to ensure quality:
- **Design Phase Inspection**: Global design check, module design check, PRD/test case check
- **Prototype Inspection Supervision**: Quality supervision during prototype drawing
- **Development Phase Testing**: Module test execution, integration test execution
- **Project Acceptance**: Final acceptance and delivery confirmation

### 4. VibeLockDsn-design-distillation (Design Style Distillation Skill) ✨ NEW
Specifically designed to deconstruct enterprise management system Web/App page screenshots:
- Deep recognition of core UI elements, page framework structure, color schemes, and interaction patterns
- Automatic filtering of irrelevant elements to extract valid design information
- Generation of AI-friendly design style MD documents
- Drawing complete component libraries in pencil tool
- Checking component completeness and saving .pen files
- Generating component usage documentation

## How to Use

### Installation Steps

#### 1. Choose Language Version
Chinese users use skills with `-zh` suffix, English users use versions without suffix

#### 2. Install Skills
Download and install skill folders to your Coding Agent's (Claude Code, Cursor, Trae, etc.) skills root directory

#### 3. Install Companion Tools

##### Obsidian Installation
```bash
# macOS
brew install --cask obsidian

# Windows
# Download from official website: https://obsidian.md/download

# Linux
sudo snap install obsidian --classic
```

##### Pencil Installation
```bash
# Visit official website to download platform-specific installer
# https://pencil.evolus.vn/

# macOS alternative
brew install --cask pencil
```

##### Obsidian Official Skill Installation
```bash
# Method 1: Install via npm (if available)
npm install -g @anthropic-ai/claude-code

# Method 2: Manual installation
# 1. Visit Obsidian official Skill repository
# 2. Download the latest version
# 3. Place the skill folder in your Coding Agent's skills directory
```

### Usage Flow
1. **Design Style Distillation** (Optional): Use `/VibeLockDsn-design-distillation` to deconstruct existing system screenshots and quickly establish design standards
2. **Product Design**: Use `/VibeLockDsn-product-manager` to complete requirements analysis, architecture design, prototype design, etc.
3. **Design Acceptance**: Use `/VibeLockDsn-product-tester` to inspect and accept design deliverables (design phase)
4. **Product Development**: Use `/VibeLockDsn-product-developer` for modular development, testing, and deployment
5. **Testing & Acceptance**: Use `/VibeLockDsn-product-tester` to execute tests and project acceptance (development phase)

### Workflow Features
- **Modular Design**: Support progressive advancement by modules, each module can be independently designed, developed, and tested
- **Progress Persistence**: Record progress through session files, support interruption and resumption at any time
- **Multi-role Collaboration**: Simulate real team collaboration patterns with clear responsibilities
- **Independent Testing & Acceptance**: Testing and acceptance independent of design and development, ensuring objective and fair quality assurance
- **Full Lifecycle Coverage**: From design distillation to final acceptance, complete coverage of the entire product lifecycle

## Core Advantages

Compared to traditional Vibe Coding and Vibe Design:

| Traditional Approach | VibeLockDsn Approach |
|---------------------|---------------------|
| Relies on multi-turn Prompt conversations | Structured workflow guidance |
| Difficult to handle complex architectures | Systematic architecture design methodology |
| Lacks progress management | Comprehensive progress persistence mechanism |
| Single role perspective | Multi-role collaboration model |
| Inconsistent design standards | Can extract design standards from existing systems |
| Lacks independent testing & acceptance | Independent testing and acceptance process ensuring quality |

## Suitable Scenarios

- ✅ Enterprise management system development
- ✅ Complex business process applications
- ✅ Projects requiring strict design standards
- ✅ Team collaboration development scenarios
- ✅ Refactoring or migration from existing systems

## Final Note

This idea and scenario are still under continuous improvement. We sincerely look forward to your trial and feedback, so we can work together to create a more efficient methodology!
