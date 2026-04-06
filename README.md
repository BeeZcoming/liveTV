# <img src="https://ouonnki.site/upload/logo.svg" alt="OuonnkiTV Logo" width="80" style="position:relative; top:1rem;"/> OuonnkiTV

[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](LICENSE) [![Node.js](https://img.shields.io/badge/node-%3E%3D20-brightgreen)]() [![pnpm](https://img.shields.io/badge/pnpm-%3E%3D9.15.4-blue)]() [![Vite](https://img.shields.io/badge/vite-%5E6.3.5-yellowgreen)]()

<p align="center">
  <img src="https://ouonnki.site/upload/CleanShot%202025-07-13%20at%2016.53.42%402x.png" alt="App Screenshot" width="600"/>
</p>

## 📑 目录

- [ OuonnkiTV](#-ouonnkitv)
  - [📑 目录](#-目录)
  - [🚀 一键部署](#-一键部署)
  - [📖 简介](#-简介)
  - [✨ 特性](#-特性)
  - [🚀 快速开始](#-快速开始)
    - [🛠 环境依赖](#-环境依赖)
    - [💻 本地开发](#-本地开发)
    - [📦 构建 \& 预览](#-构建--预览)
  - [🌳 环境变量](#-环境变量)
  - [🗂 项目结构](#-项目结构)
  - [⚙️ 配置](#️-配置)
  - [📋 常用命令](#-常用命令)
  - [🤝 贡献](#-贡献)
  - [📜 许可证](#-许可证)
  - [⚠️ 免责声明](#️-免责声明)

## 🚀 一键部署

点击下面按钮，一键部署到 Vercel：

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/BeeZcoming/liveTV&build-command=pnpm%20build&install-command=pnpm%20install&output-directory=dist)

**Vercel手动详细部署方法**
- Fork 或克隆本仓库到您的 GitHub/GitLab 账户
- 登录 Vercel，点击 "New Project"
- 导入您的仓库
- 在 "Build & Output Settings" 中配置：
  - Install Command：`pnpm install`
  - Build Command：`pnpm build`
  - Output Directory：`dist`
- ⚠️ 重要：在 "Settings" > "Environment Variables" 中添加 `VITE_PROXY_URL`，值为 `/api/proxy?url=`
- 点击 "Deploy"

---

## 📖 简介

**OuonnkiTV** 是一个使用 **React** + **Vite** + **TypeScript** 构建的现代化视频播放和搜索前端应用，支持跨设备流畅播放、历史记录管理和个性化设置。
本项目基于 LibreSpark/LibreTV 进行重构与增强。

## ✨ 特性

- 🔍 **视频搜索**：实时关键词推荐与历史记录
- ▶️ **流畅播放**：集成 `xgplayer` 播放 HLS/MP4
- 📝 **详情展示**：视频封面、标题与描述一目了然
- 🕒 **历史记录**：自动保存观看和搜索记录
- ⚙️ **设置面板**：自定义主题、语言等偏好
- 🚀 **性能优化**：按需加载、代码分割与缓存
- 📱 **响应式设计**：桌面和移动设备无缝适配

## 🚀 快速开始

### 🛠 环境依赖

- **Node.js** >= 20.0.0
- **pnpm** >= 9.15.4

```bash
# 克隆仓库
git clone https://github.com/Ouonnki/OuonnkiTV.git
cd OuonnkiTV

# 安装依赖
pnpm install
```

### 💻 本地开发

```bash
pnpm run dev
# 访问 http://localhost:3000
```

### 📦 构建 & 预览

```bash
pnpm run build
pnpm run preview
# 访问 http://localhost:4173
```

## 🌳 环境变量

部署到 Vercel 时，需要在 Vercel 仪表盘的 **Environment Variables** 中添加以下变量：
- `VITE_PROXY_URL`：`/api/proxy?url=`

本地开发可在项目根目录创建 `.env.local` 文件，并添加：
```env
VITE_PROXY_URL=https://cors.zme.ink/
```

---

## 🗂 项目结构

```text
.
├─ api/                  本地开发代理配置
├─ public/               静态资源
├─ src/                  源代码
│  ├─ assets/            图像与 SVG
│  ├─ components/        通用组件
│  ├─ config/            全局配置
│  ├─ hooks/             自定义 Hooks
│  ├─ pages/             页面组件
│  ├─ router/            路由配置
│  ├─ services/          API 服务封装
│  ├─ store/             全局状态 (Zustand)
│  ├─ styles/            样式与 TailwindCSS
│  ├─ types/             TypeScript 类型定义
│  ├─ App.tsx            根组件
│  └─ main.tsx           渲染入口
├─ vite.config.ts        Vite 配置
├─ tsconfig.json         TypeScript 配置
└─ package.json          依赖与脚本
```

---

## ⚙️ 配置

- **`src/config/api.config.ts`**：后端 API 地址与超时配置
- **`src/config/analytics.config.ts`**：统计与日志埋点配置
- **`api/proxy.ts`**：本地开发代理规则

## 📋 常用命令

| 命令             | 描述             |
| ---------------- | ---------------- |
| `pnpm run dev`   | 启动开发服务器   |
| `pnpm run build` | 生产环境构建     |
| `pnpm run preview` | 预览生产包     |
| `pnpm run lint`  | ESLint 检查      |

---

## 🤝 贡献

欢迎通过提交 [Issue](https://github.com/<your-username>/OuonnkiTV/issues) 或 [Pull Request](https://github.com/<your-username>/OuonnkiTV/pulls) 参与贡献！

## 📜 许可证

本项目遵循 [Apache License 2.0](LICENSE)。 

## ⚠️ 免责声明
 **本项目仅作为视频搜索工具，不存储、上传或分发任何视频内容。所有视频均来自第三方 API 接口提供的搜索结果。如有侵权内容，请联系相应的内容提供方。**

本项目开发者不对使用本项目产生的任何后果负责。使用本项目时，您必须遵守当地的法律法规。 
