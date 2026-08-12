# ⚡ PWOS5 - 第五代全能系统

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-green)
![License](https://img.shields.io/badge/License-Apache%202.0-yellow)
![Version](https://img.shields.io/badge/Version-v4.0-red)
![Size](https://img.shields.io/badge/Size-553KB-brightgreen)

> 开源跨平台 Python 全能系统，极速启动，极致轻量，功能完整

🌐 **官方网站**：[pwos.cpolar.top](https://pwos.cpolar.top)

📧 **联系邮箱**：youismoyixi@qq.com

📥 **EXE版本**：请前往官方网站下载

---

## 🎯 项目简介

PWOS5 是 PWOS 系列的第五代旗舰版本。它在继承前代所有功能的基础上，进行了全面的性能优化和架构重构。**系统完整体积仅 553 KB（压缩后）**，二次启动速度最快可达 **2.20 秒**，同时保留了用户管理、四层加密、AI 助手（DeepSeek + 阿里云 + 本地 GGUF）、脚本引擎、网络诊断、远程控制等全部功能。

---

## ✨ 核心功能

- 👥 **用户管理**：添加、查看、查找、删除用户，多文件分组管理，数据备份恢复，CSV/JSON 导入导出，支持跨版本数据迁移

- 🔐 **四层加密防护**：随机密钥 + 双层 PBKDF2 哈希 + 机器指纹绑定 + 异或混合，密码哈希存储，支持暗号恢复和临时密钥

- 🌐 **网络工具**：端口扫描（快速/自定义/指定端口），DNS 查询，网络测速，网络接口信息查看，**内置 hosts 劫持检测与修复**

- 🤖 **AI 三驾马车**：支持 DeepSeek API、阿里云通义千问 API、**本地 GGUF 大模型**，提供智能对话和系统分析，支持故障自动切换

- 🖥️ **命令行模式**：提供原生、Windows、Linux 三种命令行风格切换，命令历史记录，文件管理，进程管理，磁盘/内存信息查看

- 📝 **PWOS 脚本引擎**：支持 `.pwos` 自定义脚本，可使用 `#main`、`#func`、`#import` 等标签编写自动化任务，**支持沙盒执行**

- 📦 **标准库 std**：内置 C++ 风格 STL 容器（Vector、Map、Stack、Queue）、算法、智能指针、位操作等，让 Python 拥有 C++ 的强大特性

- 🔄 **系统更新**：智能集成更新、手动更新、安全补丁检查、紧急修复功能

- 📋 **库依赖管理**：自动检测缺失库，一键安装，选择性安装，适配 EXE 和源码环境

- 🔧 **开发者模式**：隐藏的高级功能，用于系统诊断、性能测试、批量操作等

- 🖤 **黑匣子日志**：所有操作可追溯，崩溃自动记录堆栈，支持安全审计

---

## 🚀 对比 PWOS3（第三代）的主要提升

| 对比维度 | PWOS3（第三代） | PWOS5（第五代） | 提升幅度 |
| :--- | :--- | :--- | :--- |
| **系统体积** | ~2.2 MB | **553 KB** | **缩小 75%** |
| **启动速度（空载）** | ~5.31 秒 | **2.20 秒** | **快 58%** |
| **启动速度（300 用户）** | ~3.60 秒 | **2.84 秒** | **快 21%** |
| **加密系统** | 四层加密 | **四层加密 + 可选三层便携模式** | 更灵活 |
| **脚本引擎** | 支持 `.pwos` 脚本 | **完整 STD 库 + 沙盒执行 + 按需加载** | 更强大 |
| **日志系统** | 基础日志 | **黑匣子日志 + 安全审计 + 堆栈追踪** | 更安全 |

---

## 📦 安装方式

### 方式一：一键安装（推荐）

```bash
# 下载 install.py
python install.py
```

### 方式二：手动部署

```bash
# 下载 PWOS5.py 和 std_lib.py
python PWOS5.py
```

### 方式三：EXE 版本（无需 Python）

📥 前往官方网站下载：[pwos.cpolar.top](https://pwos.cpolar.top)

---

## 🌐 语言切换官方指南

系统默认为中文，如需切换为英文或其他语言：

| 步骤 | 操作 |
| :--- | :--- |
| **1** | 在主菜单输入 `a1b2c3d4e5` |
| **2** | 选择 **20. 🛠️ 开发者选项** |
| **3** | 选择 **17. 系统语言切换** |
| **4** | 输入目标语言编号（如 `3` = English） |
| **5** | 输入 `YES` 确认切换 |
| **6** | 等待切换完成，按回车返回 |

**支持的语言：**

| 编号 | 语言 | 代码 |
| :--- | :--- | :--- |
| 1 | 简体中文 | zh-CN |
| 2 | 繁體中文 | zh-TW |
| 3 | English (US) | en-US |
| 4 | 日本語 | ja-JP |
| 5 | 한국어 | ko-KR |
| 6 | Bahasa Indonesia | id-ID |

> **所有界面文字立即生效，无需重启！**

---

## 📖 PWOS 脚本编写教程

脚本文件以 `.pwos` 为后缀，放置在 `scripts/` 目录下。

### 基本语法

| 标签 | 说明 |
|------|------|
| `#main 编号:` | 定义菜单脚本块 |
| `#main 编号 stop` | 结束脚本块 |
| `#func 函数名:` | 定义函数 |
| `#func stop` | 结束函数 |
| `#import 库名` | 导入标准库 |

### Hello World

```python
#main 1:
print("Hello, PWOS5!")
#main 1 stop
```

### 文件操作

```python
#main 2:
#import std
std.file.write("hello.txt", "Hello PWOS5!")
content = std.file.read("hello.txt")
print(f"Content: {content}")
#main 2 stop
```

### C++ 风格容器

```python
#main 3:
#import std
v = std.vector([3, 1, 4, 1, 5])
v.push_back(9)
v.sort()
print(v.data())
#main 3 stop
```

### 批量添加用户（调用系统 API）

```python
#main 4:
#import std
users = [
    {"name": "TestA", "age": 25, "gender": "M", "job": "Engineer"},
    {"name": "TestB", "age": 30, "gender": "F", "job": "Designer"},
]
count = 0
for u in users:
    if User.add_user_quick(u["name"], u["age"], u["gender"], u["job"]):
        count += 1
print(f"✅ Added {count}/{len(users)} users")
#main 4 stop
```

### DNS 查询与网络诊断

```python
#main 5:
#import std
import socket
domain = input("Enter domain: ") or "github.com"
ip = socket.gethostbyname(domain)
print(f"✅ A record: {ip}")
if ip == "127.0.0.1":
    print("⚠️ Hosts hijacking detected!")
#main 5 stop
```

---

## 📂 项目结构

```
PWOS5/
├── PWOS5.py              # 主程序
├── std_lib.py            # 标准库
├── install_guide.py      # 一键安装器
├── scripts/              # 用户脚本目录
│   └── *.pwos            # 脚本文件
├── update_packages/      # 更新包目录
└── user_system_data/     # 用户数据目录（加密存储）
```

---

## 🔧 开发者模式

在主菜单输入 `a1b2c3d4e5` 激活开发者模式，提供以下功能：

- 系统内部状态查看
- 数据库诊断
- 性能测试
- 调试日志级别调整
- 批量数据操作
- 进程管理
- 磁盘与内存详细信息
- 修改系统版本号
- 紧急系统修复
- 安全引导管理
- 内置脚本管理
- **系统语言切换**
- **机器码绑定管理**

---

## 📊 系统要求

| | EXE 版本 | 源码版本 |
|------|----------|----------|
| 操作系统 | Windows 10/11 | Windows / Linux / macOS |
| Python | 不需要 | Python 3.6+ |
| 内存 | 512 MB 以上 | 512 MB 以上 |
| 磁盘 | 200 MB 以上 | 200 MB 以上 |
| 依赖 | 无需安装 | 可选（系统可自动安装） |

---

## ❓ 常见问题

**Q: EXE 打不开或被杀毒软件拦截？**

A: PyInstaller 打包可能误报，请添加信任或使用源码运行。

**Q: 如何配置 AI 助手？**

A: 主菜单 → AI智能助手 → 配置 API Key。

**Q: 如何加载本地 GGUF 模型？**

A: 将 `.gguf` 文件放入程序目录，在 AI 菜单选择本地模型。

**Q: 如何切换语言？**

A: 开发者模式 → 20 → 17 → 选择语言编号 → YES 确认。

**Q: 如何从旧版本迁移数据？**

A: 数据恢复 → 选择旧版备份文件 → 自动转换格式。

---

## 🤝 贡献

1. Fork 本仓库
2. 创建分支：`git checkout -b feature/xxx`
3. 提交修改：`git commit -m 'Add feature'`
4. 推送分支：`git push origin feature/xxx`
5. 提交 Pull Request

---

## 📜 许可证

Apache License 2.0

Copyright © 2024-2026 moyixi123-git

---

## 👨‍💻 作者

**维护者**：moyixi123-git

**官方网站**：[pwos.cpolar.top](https://pwos.cpolar.top)

**联系邮箱**：youismoyixi@qq.com

---

⭐ 如果这个项目对你有帮助，请点个 Star 支持一下！


---

## 🇬🇧 English Version


# ⚡ PWOS5 - Fifth Generation All-in-One System

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-green)
![License](https://img.shields.io/badge/License-Apache%202.0-yellow)
![Version](https://img.shields.io/badge/Version-v4.0-red)
![Size](https://img.shields.io/badge/Size-553KB-brightgreen)

> Open source cross-platform Python all-in-one system, blazing fast startup, ultra lightweight, full featured

🌐 **Official Website**: [pwos.cpolar.top](https://pwos.cpolar.top)

📧 **Contact Email**: youismoyixi@qq.com

📥 **EXE Version**: Please visit the official website

---

## 🎯 Introduction

PWOS5 is the fifth generation flagship of the PWOS series. Based on all previous features, it has undergone comprehensive performance optimization and architectural refactoring. **The complete system is only 553 KB (compressed)** with a startup time as fast as **2.20 seconds**, while retaining all features including user management, quad-layer encryption, AI assistant (DeepSeek + Aliyun + local GGUF), script engine, network diagnostics, and remote control.

---

## ✨ Core Features

- 👥 **User Management**: Add, view, search, delete users, multi-file group management, data backup and recovery, CSV/JSON import/export, cross-version data migration

- 🔐 **Quad-Layer Encryption**: Random key + Double PBKDF2 hash + Machine fingerprint binding + XOR mix, password hash storage, secret question recovery and temporary key support

- 🌐 **Network Tools**: Port scanning (quick/custom/specific), DNS query, network speed test, network interface info, **built-in hosts hijacking detection and repair**

- 🤖 **AI Triple Engine**: Supports DeepSeek API, Aliyun Tongyi Qianwen API, **local GGUF models**, intelligent conversation and system analysis, automatic failover

- 🖥️ **Command Line Mode**: Native/Windows/Linux style switching, command history, file/process management, disk/memory info

- 📝 **PWOS Script Engine**: Custom `.pwos` scripts with `#main`, `#func`, `#import` tags, **sandbox execution support**

- 📦 **Standard Library std**: C++ style STL containers (Vector, Map, Stack, Queue), algorithms, smart pointers, bit operations

- 🔄 **System Update**: Intelligent update, manual update, security patch check, emergency repair

- 📋 **Library Management**: Auto-detect missing libraries, one-click install, selective install

- 🔧 **Developer Mode**: Hidden advanced features for system diagnosis, performance testing, batch operations

- 🖤 **Black Box Logging**: All operations traceable, crash stack traces automatically recorded, security audit support

---

## 🚀 Improvements Over PWOS3 (Gen 3)

| Metric | PWOS3 (Gen 3) | PWOS5 (Gen 5) | Improvement |
| :--- | :--- | :--- | :--- |
| **System Size** | ~2.2 MB | **553 KB** | **75% smaller** |
| **Startup Time (empty)** | ~5.31 sec | **2.20 sec** | **58% faster** |
| **Startup Time (300 users)** | ~3.60 sec | **2.84 sec** | **21% faster** |
| **Encryption** | Quad-layer | **Quad-layer + optional 3-layer portable mode** | More flexible |
| **Script Engine** | `.pwos` scripts | **Full STD lib + Sandbox + Lazy loading** | More powerful |
| **Logging System** | Basic logs | **Black Box logging + Security audit + Stack traces** | More secure |

---

## 📦 Installation

### Method 1: One-Click Installer (Recommended)

```bash
# Download install.py
python install.py
```

### Method 2: Manual Deployment

```bash
# Download PWOS5.py and std_lib.py
python PWOS5.py
```

### Method 3: EXE Version (No Python Required)

📥 Download EXE: Visit the official website [pwos.cpolar.top](https://pwos.cpolar.top)

---

## 🌐 How to Switch Language

The system defaults to **Chinese (zh-CN)** on first boot. To switch to English or other languages:

| Step | Action |
| :--- | :--- |
| **1** | In the main menu, enter `a1b2c3d4e5` |
| **2** | Select **20. 🛠️ Developer Options** |
| **3** | Select **17. System Language Switching** |
| **4** | Enter the target language number (e.g., `3` = English) |
| **5** | Type `YES` to confirm |
| **6** | Wait for the switch to complete, press Enter to return |

**Available Languages:**

| Number | Language | Code |
| :--- | :--- | :--- |
| 1 | 简体中文 (Simplified Chinese) | zh-CN |
| 2 | 繁體中文 (Traditional Chinese) | zh-TW |
| 3 | English (US) | en-US |
| 4 | 日本語 (Japanese) | ja-JP |
| 5 | 한국어 (Korean) | ko-KR |
| 6 | Bahasa Indonesia (Indonesian) | id-ID |

> **All interface text is updated instantly. No restart required!**

---

## 📖 PWOS Script Tutorial

Script files use `.pwos` extension, placed in `scripts/` directory.

### Basic Syntax

| Tag | Description |
|------|------|
| `#main number:` | Define a menu script block |
| `#main number stop` | End script block |
| `#func name:` | Define a function |
| `#func stop` | End function |
| `#import lib` | Import standard library |

### Hello World

```python
#main 1:
print("Hello, PWOS5!")
#main 1 stop
```

### File Operations

```python
#main 2:
#import std
std.file.write("hello.txt", "Hello PWOS5!")
content = std.file.read("hello.txt")
print(f"Content: {content}")
#main 2 stop
```

### C++ Style Containers

```python
#main 3:
#import std
v = std.vector([3, 1, 4, 1, 5])
v.push_back(9)
v.sort()
print(v.data())
#main 3 stop
```

### Batch Add Users (Calling System API)

```python
#main 4:
#import std
users = [
    {"name": "TestA", "age": 25, "gender": "M", "job": "Engineer"},
    {"name": "TestB", "age": 30, "gender": "F", "job": "Designer"},
]
count = 0
for u in users:
    if User.add_user_quick(u["name"], u["age"], u["gender"], u["job"]):
        count += 1
print(f"✅ Added {count}/{len(users)} users")
#main 4 stop
```

### DNS Query & Network Diagnosis

```python
#main 5:
#import std
import socket
domain = input("Enter domain: ") or "github.com"
ip = socket.gethostbyname(domain)
print(f"✅ A record: {ip}")
if ip == "127.0.0.1":
    print("⚠️ Hosts hijacking detected!")
#main 5 stop
```

---

## 📂 Project Structure

```
PWOS5/
├── PWOS5.py              # Main program
├── std_lib.py            # Standard library
├── install_guide.py      # One-click installer
├── scripts/              # User scripts directory
│   └── *.pwos            # Script files
├── update_packages/      # Update packages directory
└── user_system_data/     # User data directory (encrypted)
```

---

## 🔧 Developer Mode

Enter `a1b2c3d4e5` in the main menu to activate developer mode, which provides:

- System internal status view
- Database diagnosis
- Performance testing
- Debug log level adjustment
- Batch data operations
- Process management
- Disk & memory detailed information
- System version modification
- Emergency system repair
- Safe boot management
- Built-in script management
- **System language switching**
- **Machine code binding management**

---

## 📊 System Requirements

| | EXE Version | Source Version |
|------|----------|----------|
| OS | Windows 10/11 | Windows/Linux/macOS |
| Python | Not required | 3.6+ |
| Memory | 512 MB+ | 512 MB+ |
| Disk | 200 MB+ | 200 MB+ |
| Dependencies | Not required | Optional |

---

## ❓ FAQ

**Q: EXE blocked by antivirus?**

A: PyInstaller packaging may trigger false positives. Add to trust list or use source code.

**Q: How to configure AI Assistant?**

A: Main menu → AI Assistant → Configure API Key.

**Q: How to load local GGUF models?**

A: Place `.gguf` file in the program directory, select local model in AI menu.

**Q: How to switch language?**

A: Developer mode → 20 → 17 → select language number → YES.

**Q: How to migrate data from older versions?**

A: Data Recovery → select old backup file → auto convert format.

---

## 🤝 Contributing

1. Fork this repository
2. Create branch: `git checkout -b feature/xxx`
3. Commit: `git commit -m 'Add feature'`
4. Push: `git push origin feature/xxx`
5. Submit Pull Request

---

## 📜 License

Apache License 2.0

Copyright © 2024-2026 moyixi123-git

---

## 👨‍💻 Author

**Maintainer**: moyixi123-git

**Official Website**: [pwos.cpolar.top](https://pwos.cpolar.top)

**Contact Email**: youismoyixi@qq.com

---

⭐ Star this project if you find it helpful!
