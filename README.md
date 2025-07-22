# VulCMS - 易受攻击的 CMS 靶场集合

[![zh-CN](https://img.shields.io/badge/language-中文-blue.svg)](README.md)

这是一个精心收集的、存在已知漏洞的 CMS 靶场环境集合。该项目的初衷是在我近期的工作中，需要收集验证存在漏洞的 CMS 应用。为了方便安全研究人员、渗透测试工程师和爱好者们进行复现、学习和测试，我将这些环境打包成了独立的 Docker 应用，并在此分享给大家。

## ✨ 项目特点

- **一键启动**：所有 CMS 环境均已容器化，使用 Docker Compose 即可一键启动，无需繁琐配置。
- **环境隔离**：每个靶场都在独立的 Docker 容器中运行，与主机系统完全隔离，确保安全。

## 🚀 快速开始

确保您的系统已经安装了 `Docker` 和 `Docker Compose`。

1.  **克隆项目到本地：**
    ```bash
    git clone https://github.com/le31ei/vulcms.git
    ```

2.  **选择一个靶场：**
    进入任意一个您感兴趣的 CMS 目录。例如，要启动 `some-vulnerable-cms`：
    ```bash
    cd vulcms/cms/some-vulnerable-cms/
    ```

3.  **启动环境：**
    执行以下命令，靶场将在后台启动。
    ```bash
    docker-compose up -d
    ```

4.  **访问和测试：**
    打开浏览器，访问 `http://localhost:PORT`（具体端口请查看对应靶场的 `docker-compose.yml` 文件）即可开始您的测试。

## ⚠️ 免责声明

本项目中提供的所有靶场环境仅供授权的、合法的安全研究和教育目的使用。

**严禁**将此项目中的任何内容用于非法活动或未经授权的渗透测试。项目作者不对任何因滥用或误用本项目内容而导致的直接或间接损失负责。

---
*如果您觉得这个项目对您有帮助，请给一个 Star ⭐！*
