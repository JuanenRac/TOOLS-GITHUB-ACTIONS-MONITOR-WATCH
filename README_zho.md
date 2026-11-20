<p align="center">
  <img src="images/TOOLS_GITHUB_ACTIONS_MONITOR_WATCH_BANNER.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH banner" width="100%">
</p>

# 🛠️ TOOLS-GITHUB-ACTIONS-MONITOR-WATCH

<p align="center"><a href="README.md">🇺🇸 English</a> | <a href="README_spa.md">🇪🇸 Español</a> | <a href="README_fra.md">🇫🇷 Français</a> | <a href="README_ita.md">🇮🇹 Italiano</a> | <a href="README_deu.md">🇩🇪 Deutsch</a> | 🇨🇳 <b>中文</b> | <a href="README_jpn.md">🇯🇵 日本語</a> | <a href="README_por.md">🇵🇹 Português</a></p>

### GitHub Actions Monitor 的 Android 应用计划中的极简Wear OS 手表版：在手腕上快速查看你的工作流。仅为脚手架：目前尚未实现任何功能。

<p align="center">
  <img src="https://img.shields.io/badge/License-GPL%203.0--or--later-blue.svg" alt="GPL 3.0 or later">
  <img src="https://img.shields.io/badge/Stack-Kotlin%20%2B%20Wear%20OS%20(planned)-blue.svg" alt="Kotlin and Wear OS (planned)">
  <img src="https://img.shields.io/badge/Languages-8-00E5FF.svg" alt="Languages">
  <img src="https://img.shields.io/badge/Tests-none%20yet-lightgrey.svg" alt="Tests">
  <img src="https://img.shields.io/badge/Version-0.0.1-0f6cbd.svg" alt="Version">
  <img src="https://img.shields.io/badge/Maturity-scaffolding-FFB020.svg" alt="Maturity">
</p>

---

**诚实性核对 - 今天真正能运行的内容：** 手表应用本身没有任何内容。本仓库只有它的基础：文档、清单、许可证和共享的仓库检查。没有代码、没有安装包、没有界面、没有通知服务、没有应用的测试，也没有在手表上试过任何东西。

---

## 📋 速览

| | |
|---|---|
| 版本 | `0.0.1` |
| 成熟度 | 脚手架 |
| 测试 | 暂无（仅有仓库检查） |
| 技术栈 | Kotlin 和 Wear OS（计划） |
| 真实硬件 | 尚未在手表上运行 |

**跳转到：** [概述](#-概述) · [架构](#-架构) · [快速开始](#-快速开始) · [测试](#-测试) · [仓库结构](#-仓库结构) · [相关项目](#-相关项目)

## 🚦 项目状态

每一行是本仓库的一个部分，灯号表示它今天做到了哪一步。内容依据仓库能够展示的证据（测试、构建、运行），而不是计划。

🟢 已完成并验证 · 🟡 可用，有已知限制 · 🟠 部分完成或尚未验证 · 🔴 未完成或不可用

| 领域 | 状态 | 在这里的含义 |
|---|---|---|
| 仓库基础 | 🟡 | 清单、八种语言的 README、许可证和共享的仓库检查在 CI 中运行。 |
| 手表应用代码 | 🔴 | 尚未开始：本仓库中还没有手表项目。 |
| 测试 | 🔴 | 应用没有测试；只运行仓库检查。 |
| 与监控器的连接 | 🔴 | 尚未开始。手表如何获取数据（通过 Android 应用还是直接获取）尚未决定。 |
| 手表与通知 | 🔴 | 尚未开始，也从未在手表上运行；没有连接任何通知服务。 |

## 🎯 概述

* **它将是什么：** Android 应用的极简Wear OS 手表版，快速查看是否有红色项目，以及你自己的监控器最近的重要告警。
* **它跟随 Android 应用：** 它在 [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) 之后构建，只显示该应用所展示内容的一个子集。
* **只读：** 它只会从你的监控器读取。不会写入 GitHub，也不会改变监控器中的任何内容。
* **它（目前）不是什么：** 没有可安装的应用，没有发布版本，也没有日期。本仓库只是预留位置，并如实说明计划内容。

## 🧩 在 EH3D 中的角色

TOOLS-GITHUB-ACTIONS-MONITOR-WATCH 的目标是成为 GitHub Actions Monitor（[TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR)）的 Android 应用 [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) 的极简Wear OS 手表版。它只显示监控器已经知道的一小部分内容，自己不做任何决定。

## 🏛️ 架构

<p align="center">
  <img src="images/architecture.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH 的架构：谁在使用、包含什么、依赖什么" width="100%">
</p>

本仓库各部分如何协作：谁在使用它、它包含什么、它依赖什么。图片由 `docs/architecture.json` 绘制，并与代码核对。

## ✨ 功能

**计划中，目前都尚不存在：**
* 一眼查看：是否有红色项目。
* 以简短形式显示最近的重要告警。
* 可选地，对重要告警震动提示，默认关闭。
* 八种语言的文本。

**不在计划内：** 写入 GitHub、长列表，或除查看之外的任何操作。运行监控器不需要手表。

## 🔒 安全与防护

* 设计意图：手表应用只读，任何访问令牌都留在你的设备上，并且只发送到你的监控器地址（或 Android 应用）。
* 本仓库中不应出现任何机密：没有密钥、令牌、推送服务文件或签名密钥。
* 这些只是设计意图。目前什么都还不存在，因此无人能够审查。

## 🚀 快速开始

目前没有可安装或运行的内容。要检查本仓库的基础，需要 Python 3.10 或更高版本：

```bash
python -I tools/ci_validate.py
python -I tools/make_architecture.py --check
python -I tools/make_structure.py --check --readmes
python -I -m unittest discover -s tools -p "test_*.py"
```

## 🧪 测试

CI 运行仓库检查以及这些检查自身的测试。手表应用本身没有测试，因为还没有代码，这里也不声称任何测试数量。

## 🏗️ 构建与发布

没有构建，也没有发布，因为应用还没有任何版本。`VERSION`、清单和变更日志中的版本 `0.0.1` 是仓库基础的版本。

## 📂 仓库结构

<p align="center">
  <img src="images/repository-structure.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH 的仓库结构" width="100%">
</p>

<details>
<summary>目录树的文本版</summary>

```text
MONITOR-WATCH/
├── tools/
│   ├── ci_validate.py                           清单、版本、README 一致性
│   └── make_architecture.py make_structure.py   绘制 README 的两张图
├── docs/                                        两张图的数据源
├── images/                                      横幅图和两张图片
├── .github/                                     CI 工作流和模板
├── VERSION                                      仓库的版本
├── electro-hobby-3d.project.json                项目清单
├── CHANGELOG.md                                 每个版本的变更
├── SECURITY.md SUPPORT.md                       如何报告漏洞及在哪里提问
└── CONTRIBUTING.md CODE_OF_CONDUCT.md LICENSE   参与贡献、行为准则和许可证
```

</details>

## 🗺️ 路线图与已知限制

**当前已知限制**

* 没有代码：没有应用、没有安装包、没有界面。
* 没有在手表上或与真实监控器一起试过任何东西。
* 手表跟随 Android 应用，因此在该应用出现之前无法开始。
* 手表如何获取数据尚未决定。

**下一步**

* 等待 Android 应用，再决定手表如何获取数据，并构建最小而有用的界面，在 CI 中配上测试。

## 🌍 语言

README 和文本提供英语、西班牙语、法语、意大利语、德语、汉语、日语和欧洲葡萄牙语版本。

## 🔗 相关项目

* [TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR)：Wear OS 手表计划显示其数据的监控器
* [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID)：本Wear OS 手表版所跟随的计划中的 Android 应用
* [EH3D-DOCS](https://github.com/JuanenRac/EH3D-DOCS)：约定和共享检查

## 📚 文档

* [套件的约定](https://github.com/JuanenRac/EH3D-DOCS/blob/main/docs/CONVENTIONS.md)
* [变更日志](CHANGELOG.md)

## 🤝 参与贡献与社区

* 提交 pull request 之前请运行 `python -I tools/ci_validate.py`；其他检查在 CI 中运行。参见 [CONTRIBUTING.md](CONTRIBUTING.md) 和[行为准则](CODE_OF_CONDUCT.md)。
* README 有八种语言版本：修改文字时要在八个文件中同步修改，两张图片由 `tools/make_architecture.py` 和 `tools/make_structure.py` 根据 `docs/architecture.json` 和 `docs/structure.json` 绘制。
* 请私下报告漏洞：[SECURITY.md](SECURITY.md)。问题、想法和报告：electrohobby3d@gmail.com（[SUPPORT.md](SUPPORT.md)）。

## 👤 作者

**JuanenRac (Electro Hobby 3D)** · electrohobby3d@gmail.com

## 📜 许可证

软件：GPL-3.0-or-later。见 [LICENSE](LICENSE)。套件的硬件设计使用 CERN OHL-S。
