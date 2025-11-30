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

## 注意事项
- 在windows上打包经常受图标缓存影响，需要清理图标缓存再打包
开管理员 PowerShell，复制粘贴执行：
```powershell
# 停掉 explorer
taskkill /f /im explorer.exe

# 删除图标/缩略图缓存（Win10/11 通用）
Remove-Item "$env:LOCALAPPDATA\IconCache.db" -Force -ErrorAction SilentlyContinue
Remove-Item "$env:LOCALAPPDATA\Microsoft\Windows\Explorer\iconcache*" -Force -ErrorAction SilentlyContinue
Remove-Item "$env:LOCALAPPDATA\Microsoft\Windows\Explorer\thumbcache*" -Force -ErrorAction SilentlyContinue

# 可选：重建字体缓存（有时图标走字体）
Remove-Item "$env:WINDIR\ServiceProfiles\LocalService\AppData\Local\FontCache*" -Force -ErrorAction SilentlyContinue

# 重启 explorer
start explorer
```

## 许可证

MIT