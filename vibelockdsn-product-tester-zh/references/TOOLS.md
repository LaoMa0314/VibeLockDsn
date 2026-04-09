name:test-tools
description:测试工具参考，提供各类测试工具的核心作用说明。

# 测试工具参考

## 单元测试工具

| 语言/框架 | 工具 | 用途 |
|---------|------|------|
| JavaScript | Vitest | Vite项目单元测试 |
| JavaScript | Jest | React/Vue单元测试 |
| Python | Pytest | Python单元测试 |
| Node.js | Jest/Mocha | Node.js单元测试 |

## 端到端测试工具

| 工具 | 用途 | 特点 |
|------|------|------|
| Playwright | 跨浏览器E2E测试 | 支持多浏览器、自动等待 |
| Cypress | Web应用E2E测试 | 实时重载、时间旅行 |
| Selenium | Web自动化测试 | 成熟稳定、多语言支持 |

## API测试工具

| 工具 | 用途 |
|------|------|
| Postman | API手动测试 |
| REST Client | VS Code插件API测试 |
| httpie | 命令行HTTP客户端 |
| curl | 命令行HTTP请求 |

## 性能测试工具

| 工具 | 用途 |
|------|------|
| k6 | 负载测试 |
| Apache Bench | HTTP性能测试 |
| Locust | Python负载测试 |
| JMeter | 全功能性能测试 |

## 测试覆盖率工具

| 工具 | 用途 |
|------|------|
| Istanbul/nyc | JavaScript覆盖率 |
| Coverage.py | Python覆盖率 |
| JaCoCo | Java覆盖率 |

## 测试命令参考

### 前端测试
```bash
# Vitest
npm run test
npm run test:coverage

# Jest
npm test
npm run test:coverage
```

### 后端测试
```bash
# Pytest
pytest tests/
pytest --cov=app tests/

# Jest (Node.js)
npm test
```

### E2E测试
```bash
# Playwright
npx playwright test
npx playwright test --ui

# Cypress
npx cypress run
npx cypress open
```

## 测试报告格式

### 单元测试报告
```
Test Suites: 5 passed, 5 total
Tests:       25 passed, 25 total
Coverage:    85% statements
```

### E2E测试报告
```
Passed:  15
Failed:  0
Skipped: 2
Duration: 45s
```

## 测试最佳实践

### 测试命名规范
- 描述性命名：`should_return_user_when_id_exists`
- 中文命名：`测试_用户登录_正常情况_应成功登录`

### 测试数据管理
- 使用独立的测试数据库
- 测试前准备数据，测试后清理数据
- 使用工厂模式创建测试数据

### 测试隔离
- 每个测试独立运行
- 不依赖其他测试的结果
- 不依赖执行顺序
