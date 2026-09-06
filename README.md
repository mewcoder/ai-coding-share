# AI Coding：从原理到实践

这是一份基于 Slidev 的 Markdown 技术分享，内容围绕 AI Coding 的发展、Agent 基本原理、Coding Agent 工具链，以及个人与团队的工作流实践展开。

## 源文件在哪里

本项目的演示文稿源代码是项目根目录下的 [`slides.md`](./slides.md)。Slidev 会读取这个文件并生成演示文稿，因此修改幻灯片内容时，优先编辑这个文件。

文稿版内容整理在 [`docs/AI_Coding分享-从原理到实践.md`](./docs/AI_Coding分享-从原理到实践.md)，适合阅读、备课和继续整理讲稿。它不是 Slidev 的直接入口文件。

所有图片素材统一放在 [`public/images/`](./public/images/)。幻灯片中的图片路径都从 `/images/` 开始，文稿中的图片使用相对路径引用这里的文件。

## 文件结构

```text
ai-coding-share/
├── slides.md                                  # Slidev 演示文稿源代码
├── docs/                                      # 文稿与备课材料
│   └── AI_Coding分享-从原理到实践.md
├── public/images/                             # 全部图片素材
├── style.css                                  # 全局样式
├── package.json                               # 运行与构建脚本
├── package-lock.json                          # 依赖版本锁定
└── README.md                                  # 项目说明
```

## 运行与构建

安装依赖：

```bash
npm install
```

启动本地预览：

```bash
npm run dev
```

构建演示文稿：

```bash
npm run build
```

导出 PDF 或 PNG：

```bash
npm run export:pdf
npm run export:png
```

## 视觉风格

整体采用荧光黄与墨黑为主色，搭配纸白、淡紫、粉红和浅蓝，使用粗边框与硬阴影，形成偏编辑部风格的技术分享视觉语言。
