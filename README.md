# Electron Test Application

这是一个基于 Electron 的简单桌面应用程序，展示了如何创建一个基本的跨平台桌面应用。

## 功能特点

- 创建一个简单的桌面窗口
- 显示基本的 HTML 内容
- 支持 Windows 平台打包
- 使用自定义图标

## 技术栈

- Electron 31.7.6
- HTML/CSS/JavaScript

## 快速开始

### 安装依赖

```bash
npm install
```

### 运行开发环境

```bash
npm start
```

或者

```bash
npm run dev
```

### 打包应用程序

```bash
npm run pack
```

打包后的应用程序将位于 `dist/packaged-new-with-icon/electron-test-app-win32-x64/` 目录中。

## 项目结构

```
.
├── main.js              # Electron 主进程文件
├── index.html           # 应用程序界面
├── package.json         # 项目配置文件
├── start.bat            # Windows 启动脚本
└── assets/              # 资源文件目录
    └── icon/            # 图标文件目录
```

## 许可证

MIT