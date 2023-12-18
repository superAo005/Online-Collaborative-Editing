
## ⚡ 项目简介
Wise投研平台系统
主要是为满足金融研究院以及九方投顾老师在投研工作中的痛点问题，如观点如何管理、观点分发、模拟股池等相关方面的需求
项目背景是为了满足资产管理行业在投研业务发展、团队建设、系统方案设计等多方面的需求，以适应行业的快速变化和高度竞争


## 技术栈
- **Vue3**：采用 Vue3 + script setup 最新的 Vue3 组合式 API
- **Element Plus**：Element UI 的 Vue3 版本
- **Pinia**: 传说中的 Vuex5
- **Vite**：真的很快
- **Vue Router**：路由路由
- **TypeScript**：JavaScript 语言的超集
- **PNPM**：更快速的，节省磁盘空间的包管理工具
- **Scss**：和 Element Plus 保持一致
- **CSS 变量**：主要控制项目的布局和颜色
- **ESlint**：代码校验
- **Prettier**：代码格式化
- **Axios**：发送网络请求（已封装好）
- **UnoCSS**：具有高性能且极具灵活性的即时原子化 CSS 引擎

## 🚀 开发

```bash
# 配置
1. 一键安装 .vscode 目录中推荐的插件
2. node 版本 18.x 或 20+
3. pnpm 版本 8.x 或最新版

# 安装依赖
pnpm i

# 启动服务
pnpm dev
```

## 📦️ 多环境打包

```bash
# 构建预发布环境
pnpm build:uat

# 构建正式环境
pnpm build:prod
```

## 🔧 代码检查

```bash
# 代码格式化
pnpm lint

```

## Git 提交规范参考

- `feat` 增加新的业务功能
- `fix` 修复业务问题/BUG
- `perf` 优化性能
- `style` 更改代码风格, 不影响运行结果
- `refactor` 重构代码
- `revert` 撤销更改
- `test` 测试相关, 不涉及业务代码的更改
- `docs` 文档和注释相关
- `chore` 更新依赖/修改脚手架配置等琐事
- `workflow` 工作流改进
- `ci` 持续集成相关
- `types` 类型定义文件更改
- `wip` 开发中


