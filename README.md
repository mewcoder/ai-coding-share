# AI Coding：从原理到实践

一份围绕 AI Coding 的技术分享幻灯片，内容从模型与 Agent 原理出发，介绍 Coding Agent 工具链、项目配置、能力扩展、工作流和 AI 工程实践。

## 在线演示

GitHub Pages 部署完成后访问：

<https://mewcoder.github.io/ai-coding-share/>

每次推送到 `main` 分支后，GitHub Actions 会自动构建并更新页面。

## 内容结构

- AI Coding 的发展与模型趋势
- Agent 的基本原理、Loop、Context、MCP 与 Skills
- 本地开发环境、主流 Agent、模型网关与浏览器自动化
- Agent 配置目录、长期上下文、能力扩展与工作流
- SDD、AI 工程化、Agent 元能力与软件工程思考

## 项目文件

```text
ai-coding-share/
├── slides.md                    # Slidev 幻灯片源文件
├── style.css                    # 全局与页面样式
├── global-bottom.vue            # 页面右下角页码组件
├── docs/                        # 文稿与备课材料
├── public/images/               # 幻灯片图片素材
├── .github/workflows/deploy.yml # GitHub Pages 自动部署
├── package.json                 # 脚本与依赖
└── package-lock.json            # 锁定依赖版本
```

## 本地运行

安装依赖：

```bash
npm ci
```

启动本地预览：

```bash
npm run dev
```

默认访问 <http://localhost:3030/>。

## 构建与导出

构建静态页面：

```bash
npm run build
```

导出 PDF 或 PNG：

```bash
npm run export:pdf
npm run export:png
```

构建产物位于 `dist/`，GitHub Pages workflow 会自动使用它进行部署。

## GitHub Pages

部署配置位于 `.github/workflows/deploy.yml`，使用 GitHub Pages 官方 Actions 完成：

1. 检出仓库并安装 Node.js 依赖。
2. 使用仓库名作为 base path 构建 Slidev。
3. 上传 `dist/` 静态产物。
4. 发布到 GitHub Pages。

也可以在 GitHub 仓库的 **Actions** 页面手动运行部署 workflow。

## 视觉风格

整体采用荧光黄与墨黑为主色，搭配纸白、粉红和浅蓝，使用粗边框、硬阴影和本地字体栈，形成偏编辑部风格的技术分享视觉语言。
