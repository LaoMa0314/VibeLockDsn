name:project-init
description:项目初始化，创建目录结构、安装依赖、配置环境变量。

# 项目初始化指南

## 一、读取设计产物

项目初始化前建议读取以下设计产物：

| 产物 | 文件 | 用途 |
|------|------|------|
| 功能架构 | 02-功能架构.md | 了解功能模块划分 |
| 需求分析 | 01-需求分析.md | 了解产品目标和技术要求 |

---

## 二、目录结构

### 轻量级（Vue3 + Node.js/Python + SQLite）
```
project-root/
├── docs/                    # 开发文档（API文档、数据库设计、启动说明）
├── frontend/                # Vue3 前端
│   ├── src/
│   │   ├── components/
│   │   ├── views/
│   │   ├── stores/          # Pinia 状态管理
│   │   ├── api/             # API 请求层
│   │   └── assets/
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
├── backend/                 # Node.js 或 Python 后端
│   ├── src/ 或 app/
│   ├── tests/
│   └── package.json 或 requirements.txt
├── database/
│   ├── migrations/
│   ├── seeds/
│   └── app.db               # SQLite 数据库文件
└── .env                     # 环境变量
```

### 企业级（React + Python FastAPI + MySQL）
```
project-root/
├── docs/                    # 开发文档（API文档、数据库设计、启动说明）
├── frontend/                # React 前端
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── store/           # Redux Toolkit 状态管理
│   │   ├── api/             # API 请求层
│   │   └── assets/
│   ├── index.html
│   ├── vite.config.ts
│   └── package.json
├── backend/                 # Python FastAPI 后端
│   ├── app/
│   │   ├── api/
│   │   ├── models/
│   │   ├── services/
│   │   └── core/
│   ├── tests/
│   ├── alembic/             # 数据库迁移
│   └── requirements.txt
└── .env                     # 环境变量
```

## 初始化步骤

### 1. 创建目录结构
- 按照对应技术栈创建上述目录
- 在项目根目录创建 `docs/` 文件夹

### 2. 安装依赖
**轻量级前端（Vue3）：**
```bash
npm create vite@latest frontend -- --template vue
cd frontend && npm install
npm install pinia vue-router axios
```

**企业级前端（React）：**
```bash
npm create vite@latest frontend -- --template react-ts
cd frontend && npm install
npm install @reduxjs/toolkit react-redux react-router-dom axios
```

**轻量级后端（Node.js）：**
```bash
npm init -y && npm install express better-sqlite3 dotenv cors
```

**企业级后端（Python FastAPI）：**
```bash
pip install fastapi uvicorn sqlalchemy alembic pymysql python-dotenv pydantic
```

### 3. 配置环境变量
在项目根目录创建 `.env`，包含：
- 数据库连接信息
- 后端服务端口（配置前先检查端口是否被占用，被占用则自动选择闲置端口）
- 前端 API 基础地址（与后端端口保持一致）
- JWT 密钥（如需认证）

### 4. 验证初始化结果
- 前端：`npm run dev` 能正常启动，浏览器可访问
- 后端：服务启动无报错，健康检查接口返回 200
- 数据库：连接成功，可执行基础查询
- **以上三项全部通过才算初始化完成**

### 5. 创建初始文档
在 `docs/` 下创建：
- `README.md` — 项目启动说明
- `API.md` — API 接口文档（开发过程中持续更新）
- `DATABASE.md` — 数据库设计说明

### 6. 初始化Git仓库
```bash
git init
git add .
git commit -m "[阶段2] 项目初始化完成

- 创建项目目录结构
- 安装基础依赖
- 配置环境变量
- 创建初始文档"
git tag v0.1-init
```

## 开发工具参考：
详见 [TOOLS.md](TOOLS.md)
