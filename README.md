# Selab UI 组件库

![Vue 3](https://img.shields.io/badge/Vue%203-16835D?style=flat-square&logo=vuedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![VitePress](https://img.shields.io/badge/VitePress-334155?style=flat-square)
![Vitest](https://img.shields.io/badge/Vitest-4A752C?style=flat-square&logo=vitest&logoColor=white)

## 📌 项目简介

Selab UI 是一套基于 Vue 3 和 TypeScript 的组件库，配套提供组件示例、文档站点和交互式组件脚手架。

> 我在大三时主导了 Selab UI 项目。因为之前使用的 GitHub 账号丢失，我用现在的账号重新 Fork 了这个仓库，留存这段项目经历。 [原项目仓库](https://github.com/tyut-se-innovation-lab/selab-ui)

## 🏗️ 系统架构

- **组件库**使用 Vue 3、TypeScript 和 Less，通过 Gulp 构建，使用 Vitest 运行组件测试。
- **组件脚手架**通过交互式 CLI 创建组件，支持 Vue 和 TSX 两种模板。
- **开发与文档**使用 Vite 运行示例，通过 VitePress 提供组件文档。

## 📁 项目结构

| 路径 | 用途 |
| --- | --- |
| [packages/components](packages/components) | 组件源码、样式、测试和构建脚本 |
| [packages/utils](packages/utils) | 公共工具 |
| [packages/assets](packages/assets) | 共享资源 |
| [cli](cli) | 交互式组件脚手架 |
| [examples](examples) | 本地组件示例 |
| [site/docs](site/docs) | VitePress 文档站源码 |

## 🚀 如何启动

准备 Node.js 18 和 pnpm。克隆后在仓库根目录执行。

```bash
git clone https://github.com/wxk2378643343-cloud/selab-ui.git
cd selab-ui
pnpm run install:selab
```

查看组件示例运行 `pnpm run dev:examples`，查看文档运行 `pnpm run docs:dev`。启动后打开终端显示的本地地址。

| 命令 | 用途 |
| --- | --- |
| `pnpm run build:selab` | 使用 Gulp 构建组件库 |
| `pnpm run create:selab` | 交互式创建组件 |
| `pnpm run test:selab` | 运行组件测试 |
| `pnpm run coverage:selab` | 生成测试覆盖率报告 |
| `pnpm run lint:script` | 检查并自动修复脚本 |
| `pnpm run lint:style` | 检查并自动修复样式 |
| `pnpm run docs:build` | 构建静态文档站 |

组件目录约定和 Vue、TSX 模板写法见 [组件开发指南](DEVELOPMENT_GUIDE.md)。

---
## ✨ 核心工程亮点

1. **双模式主题动态换肤**：结合 Vite / Gulp 构建链路，支持通过全局 CSS 变量与组件级 Less 变量快速定制主题风格，兼顾运行时动态切换与编译期样式隔离。
2. **交互式双模板组件脚手架（`cli/`）**：执行 `pnpm run create:selab` 即可通过命令行交互一键生成标准组件目录、样式、单测与入口导出，同时支持 **Vue SFC** 与 **TSX** 两种组件编写范式，大幅降低团队成员新增组件的样板成本。
3. **复杂业务组件沉淀**：
   - **高性能虚拟滚动表格**：针对大数据量列表场景采用虚拟滚动按需渲染，并通过插槽机制支持单元格高度自定义；
   - **JSON Schema 动态表单**：支持基于 JSON 配置动态生成表单项、字段动态增减与联动控制，以及异步表单校验。
4. **完整质量与文档闭环**：集成 Vitest 单元测试与覆盖率报告（`coverage:selab`）、脚本与样式双 Lint 自动修复、Vite 实时组件沙盒以及 VitePress 静态文档站。

---

## 📄 开源许可证

本项目基于 [MIT License](LICENSE) 开源，详见根目录 [LICENSE](LICENSE) 文件。
