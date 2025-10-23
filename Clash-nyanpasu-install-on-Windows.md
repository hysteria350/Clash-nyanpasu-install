# Windows 平台 Clash nyanpasu 安装与使用教程

## Clash Nyanpasu 简介

Clash Nyanpasu 是基于 Tauri 的 Clash GUI 软件实现，利用 Tauri 的特性实现了跨平台的支持。 它能在 Windows、Linux 和 macOS 系统上提供代理服务，并支持 TUN 网卡模式。

软件原生支持多种内核，包括 Clash Premium、Mihomo 和 Clash Rust，用户可以根据个人喜好选择使用。 此外，该软件内置强大的脚本处理功能，为用户提供了更灵活的使用体验。 设计上，完全符合 Google Material You 的设计理念，为用户带来视觉上的愉悦感受。

*   Clasg Nyanpasu 官网：[https://nyanpasu.elaina.moe/](https://nyanpasu.elaina.moe/)
*   Clasg Nyanpasu Github: [https://github.com/LibNyanpasu/clash-nyanpasu](https://github.com/LibNyanpasu/clash-nyanpasu)

## **界面预览**

![Clash Nyanpasu 主界面](https://clashnyanpasu.org/wp-content/uploads/2024/10/1730106861-Clash-Nyanpasu-interface-cn.jpg)

## **下载与安装**

### 官网地址

**Clash Nyanpasu官网**下载地址：[https://github.com/LibNyanpasu/clash-nyanpasu/releases](https://github.com/LibNyanpasu/clash-nyanpasu/releases) 新手使用建议下载稳定版本，即版本号后标记为 `Latest` 的版本。

### 如何选择版本？

在官网下载地址中，有众多版本可供下载，如下表所示，其中文件名当中的数字为版本号，版本号之后跟着的是平台名称及包名称。

| package | description |
| --- | --- |
| clash-nyanpasu-1.6.1-1.x86\_64.rpm | Linux Redhat 系列安装包 |
| clash-nyanpasu\_1.6.1\_amd64.AppImage | Linux 跨发行版免安装软件 |
| clash-nyanpasu\_1.6.1\_amd64.AppImage.tar.gz | Linux 跨发行版免安装软件 压缩包 |
| clash-nyanpasu\_1.6.1\_amd64.deb | Linux Debian 系列安装包 |
| Clash.Nyanpasu.aarch64.app.tar.gz | Linux Debian 系列安装包 |
| Clash.Nyanpasu\_1.6.1\_aarch64.dmg | Macos ARM64位（M1,M2,M3）系列安装包 |
| Clash.Nyanpasu\_1.6.1\_x64-setup.exe | Windows 64位系统 exe 安装包 |
| Clash.Nyanpasu\_1.6.1\_x64-setup.nsis.zip | Windows 64位系统 exe 安装包 压缩包 |
| Clash.Nyanpasu\_1.6.1\_x64.dmg | Macos 64位系统安装包 |
| Clash.Nyanpasu\_1.6.1\_x64\_portable.zip | Windows 64位系统 绿色 免安装版 |
| Clash.Nyanpasu\_x64.app.tar.gz | Macos 64位系统安装包 |

### Windows 上如何安装Clash Nyanpasu？

在本文中我们使用 [Clash.Nyanpasu\_1.6.1\_x64-setup.exe](https://ghfast.top/https://github.com/libnyanpasu/clash-nyanpasu/releases/download/v1.6.1/Clash.Nyanpasu_1.6.1_x64-setup.exe) 安装包进行安装。

软件的安装教程和一般安软件没什么不同，一般按照默认的选项直接安装即可，默认以Windows平台的安装包举例，在第一次打开安装包的时候，会提示 `Windows 已保护你的电脑`，只需要点击`更多信息`，然后在点击`仍要运行`就可以，如下图所示，接下来的步骤和安装一般的软件没有区别。

![Microsoft Defender SmartScreen](https://clashnyanpasu.org/wp-content/uploads/2024/11/1730617327-Microsoft-Defender-SmartScreen-01.jpg)

点击更多信息

![Microsoft Defender SmartScreen](https://clashnyanpasu.org/wp-content/uploads/2024/11/1730617372-Microsoft-Defender-SmartScreen-02.jpg)

点击仍要运行，然后安装安装向导进行安装。

## 导入订阅

先进行 [订阅购买](https://github.com/proxyguide/jichang-recommend) ，获取到订阅链接。订阅链接位于：仪表盘 > 一键订阅 , 然后复制订阅地址。

然后点击界面左侧菜单 `配置`，在顶部输入框填入刚才复制的 URL 连接地址并点击 `下载图标` 即可，下载完成后点击对应的配置文件即可添加配置文件，如下图所示。

![Clash Nyanpasu 远程订阅地址](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731224657-ClashNyanpasu-Profiles-Download.jpg)

点击“更新订阅”，系统将自动加载所有节点。

## 选择配置

成功导入节点配置文件后如下图所示，然后**点击配置**选中该配置。在只有一套配置的情况下，即使您不选中一套配置，在代理选项卡是不会出现任何代理， 这是clash nyanpasu设计不人性化或不智能的方面。

![选择Clash配置](https://hysteria350.github.io/images/clash-nyanpasu/clash_nyanpasu_select_config.png)

## 选择代理节点

在添加完订阅地址之后，需要选择一个代理节点使用，点击软件主界面左侧的 代理 选项卡，软件右上角代理规则处默认保持 规则 即可，代理模式主要有以下三种：

* 规则：所有请求根据配置文件规则进行分流
* 全局：所有请求直接发往代理服务器
* 直连：所有请求直接发往目的地，即不使用代理

全局模式可能会导致国内流量也走代理访问，除了网络会变慢外，还会消耗套餐流量。规则模式的好处就是区分国内国外的流量只有在规则内的国外网站才会走代理，这样即不影响国内访问速度，又节省套餐流量，所以如果没有什么特别的需求，一般选择 规则 即可。

然后在展开的节点组之中任意单击鼠标左键选择一个节点即可，如下图所示。

![Clash Nyanpasu 选择代理节点](https://hysteria350.github.io/images/clash-nyanpasu/select-proxy.png)

选择代理节点

上图中界面右小角的图标为延迟测试，在出来的结果当中，数字越小则表明速度越快。

## 启用代理

启用系统代理，需要点击界面左侧菜单 概览 选项卡，找到 代理接管状态 并单击 系统代理 即可，开启状态下代理接管状态字样旁边会出现 Success 字样，如下图所示。

![Clash Nyanpasu 启用代理](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731230431-ClashNyanpasu-Dashboard-System-Proxy.jpg)

启用代理

启动代理后系统托盘的图标会变成红色猫咪，以下是系统托盘图标颜色说明。

| **图标** | **说明** |
| --- | --- |
| ![Clash Nyanpasu 代理关闭状态](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731231202-clashnyanpasu-icon-white.png) | 代理关闭状态 |
| ![Clash Nyanpasu 代理开启状态](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731231194-clashnyanpasu-icon-pink.png) | 代理开启状态 |
| ![Clash Nyanpasu TUN模式开启状态](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731231210-clashnyanpasu-icon-blue.png) | TUN模式开启状态 |

系统托盘图标说明

### 设置开机自动启动

设置开机自启动，需要点击界面左侧菜单 `设置` 选项卡，找到 `开机自启` 并单击 `开机自启` 即可，开启状态底色为蓝色，如下图所示为开启状态。

![Clash Nyanpasu 开机自动启动](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731231810-ClashNyanpasu-Settings-Start-with-Windows.jpg)

开机自动启动

### 更新配置文件

点击界面左侧菜单 `配置`，点击 `更新图标` 即可更新所有配置文件，如下图所示。

![Clash Nyanpasu 更新配置文件](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731232089-ClashNyanpasu-Profiles-Update.jpg)

更新配置文件
