# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个基于 React 19 + Vite 7 的现代前端项目，使用 pnpm 作为包管理器。

## 常用命令

### 开发
```bash
pnpm dev          # 启动开发服务器（带 HMR）
pnpm build        # 构建生产版本
pnpm preview      # 预览生产构建
pnpm lint         # 运行 ESLint 检查
```

## 技术栈

- **构建工具**: Vite 7.x
- **UI 框架**: React 19.x
- **包管理器**: pnpm
- **代码规范**: ESLint（使用 flat config 格式）
- **热更新**: Vite HMR + React Fast Refresh

## 项目架构

### 入口文件
- `src/main.jsx`: 应用入口，使用 React 19 的 `createRoot` API
- `src/App.jsx`: 根组件
- `index.html`: HTML 模板

### 配置文件
- `vite.config.js`: Vite 配置，使用 `@vitejs/plugin-react`（基于 Babel）
- `eslint.config.js`: ESLint flat config，包含 React Hooks 和 React Refresh 规则

### ESLint 规则
- 使用 ESLint 9.x flat config 格式
- 自定义规则：未使用的大写或下划线开头变量不报错（`varsIgnorePattern: '^[A-Z_]'`）
- 忽略 `dist` 目录
- 启用 React Hooks 和 React Refresh 推荐规则

## 开发注意事项

- 使用 JSX 文件扩展名（`.jsx`）
- React 19 使用 StrictMode 包裹根组件
- 项目未启用 React Compiler（出于性能考虑）
- 使用 ES Modules（`"type": "module"`）
