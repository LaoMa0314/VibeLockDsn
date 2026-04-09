name:dev-tools
description:开发工具集参考，提供各类开发工具的核心作用说明。

# 开发工具参考

## 前端技术栈

| 类别 | 轻量级 | 企业级 |
|------|--------|--------|
| 框架 | Vue3 | React |
| 构建 | Vite | Vite |
| 路由 | Vue Router | React Router |
| 状态管理 | Pinia | Redux Toolkit |
| 表单验证 | VeeValidate | React Hook Form |
| HTTP请求 | Axios | Axios |
| UI组件 | ShadCN UI / Tailwind CSS | ShadCN UI / Tailwind CSS |

## 后端技术栈

| 类别 | 轻量级 | 企业级 |
|------|--------|--------|
| 框架 | Node.js Express | Python FastAPI |
| ORM | better-sqlite3 | SQLAlchemy |
| 数据验证 | Joi / Zod | Pydantic |
| 认证 | jsonwebtoken | python-jose |
| API文档 | 手写 | 自动生成 |

## 数据库

| 类别 | 轻量级 | 企业级 |
|------|--------|--------|
| 数据库 | SQLite | MySQL |
| 迁移工具 | 手写SQL脚本 | Alembic |
| 连接方式 | 文件路径 | 连接字符串 |

## 测试工具

| 类别 | 工具 |
|------|------|
| 前端单元测试 | Vitest / Jest |
| 后端单元测试 | Pytest / Jest |
| 端到端测试 | Playwright / Cypress |

## 动画库

| 工具 | 用途 |
|------|------|
| GSAP | 高性能动画 |
| Motion One | 轻量级动画 |
| Lottie | JSON动画 |
| Three.js | 3D动画 |

## 运维工具

| 类别 | 工具 |
|------|------|
| 版本控制 | Git |
| 容器化 | Docker |
| CI/CD | GitHub Actions / GitLab CI |
| 反向代理 | Nginx |
| 进程管理 | PM2 / Supervisor |

## 开发规范

### 端口约定
- 前端默认：5173
- 后端默认：8000（FastAPI）/ 3000（Node.js）
- MySQL默认：3306

### 目录约定
- `docs/` - 开发文档（API文档、数据库设计、启动说明）
- `frontend/` - 前端代码
- `backend/` - 后端代码
- `database/` - 数据库相关文件

### 文档约定
- `README.md` - 项目启动说明
- `API.md` - API接口文档
- `DATABASE.md` - 数据库设计说明
- `TEST-REPORT.md` - 测试报告
