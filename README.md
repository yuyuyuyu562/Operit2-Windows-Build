# Operit2 Windows Build

> Operit2 v1.99.0 Windows x64 非官方编译版本，基于 [Anvil-Project/operit2](https://github.com/Anvil-Project/operit2) 开源项目构建。

---

## 简介

Operit2 是一个功能强大的桌面 AI 助手应用，支持 MCP（Model Context Protocol）市场、多模型接入、Web Access 等功能。本仓库提供 Windows x64 平台的预编译版本，方便用户直接下载使用，无需自行编译。

## 版本信息

| 项目 | 内容 |
|------|------|
| 版本号 | 1.99.0 |
| 平台 | Windows x64 |
| 构建日期 | 2026-08-17 |
| 原始项目 | [Anvil-Project/operit2](https://github.com/Anvil-Project/operit2) |

## 下载

前往 [Releases](../../releases) 页面下载最新版本：

- `Operit2-v1.99.0-windows-x64.zip` — 完整编译产物（约 58.7 MB）
- `Operit2-v1.99.0-windows-x64.zip.sha256` — SHA256 校验文件

## 安装步骤

1. 下载 `Operit2-v1.99.0-windows-x64.zip`
2. 解压到任意目录（如 `D:\Operit2`）
3. 双击运行 `operit2.exe`
4. 首次运行时，在设置中配置模型 API（支持 OpenAI、DeepSeek、豆包等）

## SHA256 校验

下载后请验证文件完整性：

```powershell
certutil -hashfile Operit2-v1.99.0-windows-x64.zip SHA256
```

预期输出：
```
EAF468A0AF20D398DEB54E06561FB28D85FC84E1B147B3F155F5479DDAE49292
```

## 包含内容

| 文件 | 说明 |
|------|------|
| `operit2.exe` | 主程序 |
| `operit_flutter_bridge.dll` | Flutter 桥接库 |
| `flutter_windows.dll` | Flutter 引擎 |
| `pdfium.dll` | PDF 渲染库 |
| 7 个插件 DLL | 音频、文件、图像等插件 |
| `data/web_access/` | Web Access 资源 |

## 已知修复

本版本包含以下问题修复：

- **Web Access 端口占用**（os error 10048）— 启动前强制清理僵尸状态
- **Web Access 关闭失败**（Bad state）— 独立 try-catch + finally 状态清理
- **MCP 市场版本限制** — 版本号设为 1.99.0 以兼容市场 max_app_ver:1.99

## 免责声明

- 本仓库为社区非官方编译版本，仅供学习交流用途
- 原始项目版权归 [Anvil-Project](https://github.com/Anvil-Project) 所有
- 使用者需自行承担运行风险
- 建议仅在信任环境下使用
- 不保证任何形式的可用性或适用性

## 相关链接

- [原始项目仓库](https://github.com/Anvil-Project/operit2)
- [问题反馈](../../issues)
- [下载页面](../../releases)

---

<p align="center">Made with Flutter + Rust</p>
