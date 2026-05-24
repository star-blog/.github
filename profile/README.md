# StarBlog

**现代化博客生态系统 — 从想法到文章，为你打造无缝的创作之旅**

我们围绕个人博客创作者的需求，构建了一套完整的开源工具链。无论你是撰写技术文章、记录生活点滴，还是建立个人品牌，StarBlog 生态都能帮助你专注于内容本身，轻松实现从构思、创作、管理到发布的全流程。

---

## 生态架构

下图展示了 StarBlog 生态中各项目的核心关系与协作流程：

```mermaid
graph LR
    subgraph 创作端
        P["StarBlog Publisher<br/>跨平台桌面发布工具"]
        AI["AI 写作助手<br/>ChatGPT / Claude / Gemini / DeepSeek"]
    end

    subgraph 管理端
        A["Admin-React<br/>React 管理后台"]
    end

    subgraph 博客系统
        S["博客主系统<br/>(ASP.NET Core)<br/><a href='https://github.com/Deali-Axy/StarBlog'>主仓库</a>"]
    end

    P -->|"一键发布"| S
    A -->|"内容与数据管理"| S
    AI -.->|"智能辅助创作"| P

    style P fill:#e0f2fe,stroke:#0284c7,color:#0c4a6e
    style A fill:#fef3c7,stroke:#d97706,color:#78350f
    style S fill:#dcfce7,stroke:#16a34a,color:#14532d
    style AI fill:#f3e8ff,stroke:#9333ea,color:#581c87
```

---

## 项目总览

以下是 StarBlog 生态中的核心开源项目：

| 项目 | 说明 | 语言 | Stars |
| :--- | :--- | :--- | :--- |
| [**StarBlog (主系统)**](https://github.com/Deali-Axy/StarBlog) | 生态核心，基于 ASP.NET Core 的现代化博客引擎。 | C# | — |
| [**starblog-publisher**](https://github.com/star-blog/starblog-publisher) | 跨平台 AI 驱动的 Markdown 文章发布工具。 | C# | ⭐ 26 |
| [**Admin-React**](https://github.com/star-blog/Admin-React) | 基于 React 和 Ant Design Pro 的博客管理后台。 | TypeScript | — |

---

## 项目详情

### StarBlog（主系统）
生态的核心与基石。一个使用 ASP.NET Core 构建的、功能完备的现代化博客系统，负责内容存储、用户访问和网站渲染。
🔗 **了解更多：[github.com/Deali-Axy/StarBlog](https://github.com/Deali-Axy/StarBlog)**

### StarBlog Publisher（发布工具）
一款为创作者打造的桌面利器，旨在革新博客发布的传统流程。
- **AI 深度集成**：内置主流大模型助手，提供标题优化、内容润色、摘要生成等智能辅助，激发创作灵感。
- **高效发布流**：Markdown 编辑、实时预览、一键发布，无缝衔接。
- **智能图片处理**：自动识别并上传本地图片至博客服务器，彻底解放你的双手。
- **跨平台体验**：基于 .NET 8 与 Avalonia UI 构建，原生支持 Windows、macOS 和 Linux。

### Admin-React（管理后台）
一个清晰、现代的博客管理界面，用于对文章、分类、标签等数据进行可视化操作与管理。
- **开箱即用**：基于成熟的 [Ant Design Pro](https://pro.ant.design/) 模板初始化，提供标准化的前端项目结构和组件。
- **高效开发**：支持 `npm start` 等便捷脚本，加速开发与调试流程。

---

## 技术栈概览

| 层级 | 技术选型 |
| :--- | :--- |
| **博客系统** | ASP.NET Core / C# |
| **发布工具** | .NET 8 + Avalonia UI (AOT) |
| **管理后台** | React + Ant Design Pro |
| **AI 集成** | 支持主流大模型 API (ChatGPT, Claude, Gemini, DeepSeek 等) |

---

感谢你对 StarBlog 生态的关注！我们致力于为创作者提供最佳的工具体验。欢迎探索各个项目，提出宝贵意见，或加入我们一起构建这个生态。