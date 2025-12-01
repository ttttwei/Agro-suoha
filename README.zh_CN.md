# Argo-suoha（中文）🌐 语言切换:  
[English](README.md) | [中文说明](README.zh_CN.md)

# Argo-suoha

> TT Cloudflare Tunnel 一键suoha脚本  无需公网 IP | 无需端口转发 Argo隧道 | 支持 VMess/VLESS | 自动优选伪装域名

# 🚀 Argo-suoha

> **基于 Cloudflare Tunnel 的新一代轻量级穿透工具**
>
> 无需公网 IP | 无需端口转发 | 极致隐藏 | 专为 NAT VPS 打造

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Language](https://img.shields.io/badge/Language-Bash-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey.svg)
![Powered By](https://img.shields.io/badge/Powered%20By-Cloudflare%20Tunnel-orange)

---

## 📖 项目简介

**Argo-suoha** 是一个基于 Cloudflare Tunnel (Argo) 技术的全自动化一键部署脚本。

它旨在解决无公网 IP、防火墙严格或 NAT 机器（如 HAX, IPv6 only VPS）无法对外提供服务的难题。通过建立出站隧道，无需任何端口映射，即可实现从公网到本地服务的安全访问。

本项目由 **tt** 进行二次开发与深度优化，集成了最新的 Xray 内核，并修复了原版逻辑，实现了更稳定的连接与更完美的伪装。

## ✨ 核心功能

* **⚡️ 零门槛部署**：无需公网 IP，无需配置复杂的防火墙规则，一行命令即可“梭哈”。
* **🛡️ 极致伪装**：自动配置域名作为连接（SNI/Host 分离技术），有效防止主动探测。
* **🛠 多协议支持**：灵活选择 **VMess** 或 **VLESS** 协议，满足不同客户端需求。
* **🌍 全架构兼容**：完美支持 `x86_64` (AMD64), `arm64` (Mac M1/VPS), `armv7` 等多种 CPU 架构。
* **🚀 智能优选**：内置 Argo 隧道优选逻辑，自动寻找最佳 Cloudflare 接入点。
* 
## 📌 功能特点
* **🚀梭哈模式（临时 Tunnel）**
不需要自己提供域名
重启服务器后临时隧道失效，需要重新运行

* **🚀服务模式（固定 Tunnel）**
需要 CF 托管域名并绑定 Argo 隧道
重启后仍然保持服务运行

均可自动优选 CF Argo 节点
支持 VMess 和 VLESS 协议
无需公网 IP，无需端口转发，极致隐藏

---
## ⭐ Star 星星走起
💖 如果你在用这个项目，请给我打个 star，好让我知道有多少人从这个项目中受益。


## ⚠️ 免责声明

本免责声明适用于 GitHub 上的 “Argo-suoha” 项目（以下简称“本项目”）。

### 用途
本项目仅供教育、研究和安全测试目的而设计和开发。旨在为安全研究人员、学术界人士及技术爱好者提供一个探索和实践网络通信技术的工具。

### 合法性
在下载和使用本项目代码时，必须遵守使用者所适用的法律和规定。使用者有责任确保其行为符合所在地区的法律框架、规章制度及其他相关规定。

### 免责
1. 作为本项目的 **二次开发作者**（以下简称“作者”），我 **tt** 强调本项目仅应用于合法、道德和教育目的。
2. 作者不认可、不支持亦不鼓励任何形式的非法使用。如果发现本项目被用于任何非法或不道德的活动，作者将对此强烈谴责。
3. 作者对任何人或组织利用本项目代码从事的任何非法活动不承担责任。使用本项目代码所产生的任何后果，均由使用者自行承担。
4. 作者不对使用本项目代码可能引起的任何直接或间接损害负责。
5. 为避免任何意外后果或法律风险，使用者应在使用本项目代码后的 24 小时内删除代码。不得用作任何商业用途, 代码、数据及图片均有所属版权, 如转载须注明来源。
使用本程序必循遵守部署免责声明。使用本程序必循遵守部署服务器所在地、所在国家和用户所在国家的法律法规, 程序作者不对使用者任何不当行为负责。

通过使用本项目代码，使用者即表示理解并同意本免责声明的所有条款。如使用者不同意这些条款，应立即停止使用本项目。
作者保留随时更新本免责声明的权利，且不另行通知。最新版本的免责声明将发布在本项目的 GitHub 页面上。
## 💻 一键安装 (Quick Start)

在您的 VPS 终端中执行以下命令即可（支持 Debian / Ubuntu / CentOS / Alpine）：

**方式一：短链接（推荐）**
```bash
bash <(curl -sL suoha.ggff.net | tr -d '\r')
```
**方式二：GitHub 原始链接（备用）**
```bash
bash <(curl -sL [https://raw.githubusercontent.com/ttttwei/Argo-suoha/main/suoha.sh](https://raw.githubusercontent.com/ttttwei/Argo-suoha/main/suoha.sh) | tr -d '\r')
```
**📌根据菜单选择模式**

1 梭哈模式（无需cloudflare域名重启会失效！）  
2 安装服务（需要cloudflare域名重启不会失效！）  
3 卸载服务  
4 清理缓存  
5 管理服务  
0.退出脚本

**✨服务安装完成,管理服务请运行命令`suoha`即可进行查看链接,启动停止重启卸载,管理TUNNEL等操作**


