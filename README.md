
# 心灵捕捉助手 MindCapture - AI心理陪伴平台

<div align="center">

**基于 DeepSeek AI 的心理健康陪伴与博客社区平台**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)](https://www.typescriptlang.org)
[![DeepSeek](https://img.shields.io/badge/AI-DeepSeek-0066FF)](https://deepseek.com)
[![Vercel](https://img.shields.io/badge/Deploy-Vercel-black?logo=vercel)](https://vercel.com)

</div>

## 项目简介

心灵捕捉助手是一个集 **AI 心理陪伴对话**、**博客社区**、**评论互动**和**个人成长测评**于一体的全栈 Web 应用。采用现代化大厂级 UI 设计，支持 Markdown 写作、九维量表测评、DeepSeek AI 实时对话。

> 🏗️ **在线体验**: [mindcapture-app 官网](https://supu7796.github.io/mindcapture-app/)

## 功能特性

### AI 心理陪伴对话
- 集成 **DeepSeek API**，温暖专业的心理陪伴对话
- **客户端隐私保护**：对话记录仅存储于用户设备浏览器 localStorage，不上传服务器
- 多轮对话管理，支持新建/切换/删除会话
- 大厂级聊天 UI，打字动画、消息气泡

### 博客社区
- **Markdown 编辑器**：支持标题、加粗、列表、引用，一键插入工具栏
- **文章发布/编辑/删除**：完整的 CRUD 操作
- **评论系统**：文章内评论互动
- 分类标签、阅读统计

### 九维个人成长量表
- 9 道李克特量表题，覆盖知觉、归因、决策、价值观等九大维度
- **SVG 雷达图**实时可视化得分
- 低/中/高分段个性化解读与微行动建议
- 独立部署版本可扫码即用

### 技术亮点
- 微信风格 UI 到现代化大厂级设计迭代
- HashRouter 解决静态托管 SPA 刷新 404
- GitHub API 作为持久化存储

## 技术栈

| 层级 | 技术 |
|------|------|
| **前端** | React 18, TypeScript, TailwindCSS, Vite, React Router |
| **后端** | Express.js (Vercel Serverless) |
| **AI** | DeepSeek API (OpenAI SDK) |
| **存储** | GitHub API (articles/comments), localStorage (chats) |
| **部署** | GitHub Pages (前端), Vercel (后端) |

## 本地开发

```bash
# 安装依赖
cd backend && npm install && cd ..
cd frontend && npm install && cd ..

# 启动后端 (端口 3001)
cd backend && npm run dev

# 启动前端 (端口 5173)
cd frontend && npm run dev
```

## 项目结构

```
心灵捕捉助手/
├── frontend/                # React 前端
│   └── src/
│       ├── pages/           # 页面: 首页, AI对话, 文章, 编辑器, 问卷
│       ├── components/      # 组件: 导航, 卡片, 聊天气泡, 雷达图
│       └── api/             # API 调用层
├── backend/                 # Express 后端 (本地开发)
├── deploy/
│   ├── api/                 # Vercel Serverless 部署
│   └── backend/             # 通用后端
└── standalone/              # 独立问卷页面 + 二维码
```

## 部署架构

```
用户浏览器
    │
    ├─ GitHub Pages (frontend)：supu7796.github.io/mindcapture-app
    │
    └─ Vercel Serverless (API)：mindcapture-api.vercel.app
           │
           ├─ DeepSeek API：AI 对话
           └─ GitHub API：文章/评论持久化存储
```

## License

MIT © 2025 Supu7796
