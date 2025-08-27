# Linux 平台 Clash nyanpasu 安装与使用教程

## Clash Nyanpasu 简介

Clash Nyanpasu 是基于 Tauri 的 Clash GUI 软件实现，利用 Tauri 的特性实现了跨平台的支持。 它能在 Windows、Linux 和 macOS 系统上提供代理服务，并支持 TUN 网卡模式。

软件原生支持多种内核，包括 Clash Premium、Mihomo 和 Clash Rust，用户可以根据个人喜好选择使用。 此外，该软件内置强大的脚本处理功能，为用户提供了更灵活的使用体验。 设计上，完全符合 Google Material You 的设计理念，为用户带来视觉上的愉悦感受。

- Clasg Nyanpasu 官网：<https://nyanpasu.elaina.moe/>
- Clasg Nyanpasu Github: <https://github.com/LibNyanpasu/clash-nyanpasu>

## **界面预览**

![Clash Nyanpasu 主界面](https://clashnyanpasu.org/wp-content/uploads/2024/10/1730106861-Clash-Nyanpasu-interface-cn.jpg)

## **下载与安装**

### 官网地址

**Clash Nyanpasu官网**下载地址：<https://github.com/LibNyanpasu/clash-nyanpasu/releases> 新手使用建议下载稳定版本，即版本号后标记为 `Latest` 的版本。

### 如何选择版本？

在官网下载地址中，有众多版本可供下载，如下表所示，其中文件名当中的数字为版本号，版本号之后跟着的是平台名称及包名称。

| package | description |
| --- | --- |
| clash-nyanpasu-1.6.1-1.x86_64.rpm | Linux Redhat 系列安装包 |
| clash-nyanpasu_1.6.1_amd64.AppImage | Linux 跨发行版免安装软件 |
| clash-nyanpasu_1.6.1_amd64.AppImage.tar.gz | Linux 跨发行版免安装软件 压缩包|
| clash-nyanpasu_1.6.1_amd64.deb | Linux Debian 系列安装包 |
| Clash.Nyanpasu.aarch64.app.tar.gz | Linux Debian 系列安装包 |
| Clash.Nyanpasu_1.6.1_aarch64.dmg | Macos ARM64位（M1,M2,M3）系列安装包|
| Clash.Nyanpasu_1.6.1_x64-setup.exe | Windows 64位系统 exe 安装包|
| Clash.Nyanpasu_1.6.1_x64-setup.nsis.zip | Windows 64位系统 exe 安装包 压缩包|
| Clash.Nyanpasu_1.6.1_x64.dmg | Macos 64位系统安装包 |
| Clash.Nyanpasu_1.6.1_x64_portable.zip | Windows 64位系统 绿色 免安装版|
| Clash.Nyanpasu_x64.app.tar.gz | Macos 64位系统安装包 |

### 如何安装Clash Nyanpasu？

针对不同的操作系统，请参考不同的安装步骤。

#### Debian 系列 Linux 系统下载并安装 Clash Nyanpasu

对于 debian 系列发行版（Debian、Ubuntu、 Mint、 MX、 Kubuntu、Zorin 等等）

使用命令行安装：

```bash

# 这里使用ghfast代理下载，避免github下载超时或被阻碍的情况
wget -O /tmp/clash-nyanpasu_1.6.1_amd64.deb https://ghfast.top/https://github.com/libnyanpasu/clash-nyanpasu/releases/download/v1.6.1/clash-nyanpasu_1.6.1_amd64.deb

# 安装Clash nyanpasu
sudo apt install /tmp/clash-nyanpasu_1.6.1_amd64.deb

```

#### Redhat 系列 Linux 系统下载并安装 v2rayA

对于 Redhat 系列发行版（RHEL、 Centos、 Fedora、 AlmaLinux、Rocky Linux 等等）

```bash

# 这里使用ghfast代理下载，避免github下载超时或被阻碍的情况
wget -O /tmp/clash-nyanpasu-1.6.1-1.x86_64.rpm https://ghfast.top/https://github.com/libnyanpasu/clash-nyanpasu/releases/download/v1.6.1/clash-nyanpasu-1.6.1-1.x86_64.rpm


# # 安装Clash nyanpasu
sudo dnf install /tmp/clash-nyanpasu-1.6.1-1.x86_64.rpm

```

## 导入订阅

先进行 [订阅购买](https://shortlink.20250812.xyz/1) ，获取到订阅链接。订阅链接位于：仪表盘 > 一键订阅 , 然后复制订阅地址。

然后点击界面左侧菜单 `配置`，在顶部输入框填入刚才复制的 URL 连接地址并点击 `下载图标` 即可，下载完成后点击对应的配置文件即可添加配置文件，如下图所示。

![Clash Nyanpasu 远程订阅地址](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731224657-ClashNyanpasu-Profiles-Download.jpg)

点击“更新订阅”，系统将自动加载所有节点。

## 选择代理节点

在添加完订阅地址之后，需要选择一个代理节点使用，点击软件主界面左侧的 代理 选项卡，软件右上角代理规则处默认保持 规则 即可，代理模式主要有以下三种：

* 规则：所有请求根据配置文件规则进行分流
* 全局：所有请求直接发往代理服务器
* 直连：所有请求直接发往目的地，即不使用代理

全局模式可能会导致国内流量也走代理访问，除了网络会变慢外，还会消耗套餐流量。规则模式的好处就是区分国内国外的流量只有在规则内的国外网站才会走代理，这样即不影响国内访问速度，又节省套餐流量，所以如果没有什么特别的需求，一般选择 规则 即可。

然后在展开的节点组之中任意单击鼠标左键选择一个节点即可，如下图所示。

![Clash Nyanpasu 选择代理节点](https://clashnyanpasu.org/wp-content/uploads/2024/11/1731227658-ClashNyanpasu-Proxies-Choose.jpg)

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

## Troubleshooting

**issue 1**: 在fedora上安装clash nyanpasu 时报错 “依赖检测失败：libwebkit2gtk-4.0 被 clash-nyanpasu-0:1.6.1-1.x86_64 需要”

```bash
$sudo rpm -i /tmp/clash-nyanpasu-1.6.1-1.x86_64.rpm
错误：依赖检测失败：
        libwebkit2gtk-4.0.so.37()(64bit) 被 clash-nyanpasu-0:1.6.1-1.x86_64 需要

```

原因分析：

1. Fedora Workstation 自带 GNOME 桌面，浏览器一般用 WebKitGTK 内嵌较少，大部分桌面环境不会预装 webkit2gtk（体积大、依赖重），所以新装系统上默认缺少。同时 RPM 包写的依赖名和 Fedora 的包名不完全一致

解决办法：

```bash
sudo dnf install webkit2gtk4.0
```

安装完成后，再执行：

```bash

sudo dnf install clash-nyanpasu-1.6.1-1.x86_64.rpm

```
**issue 2**: 在Fedora 40 上运行clash-nyanpasu时报错 `clash-nyanpasu: symbol lookup error: /lib64/libwebkit2gtk-4.0.so.37: undefined symbol: gst_video_is_dma_drm_caps`
现象：在Fedora 40上点击clash-nyanpasu运行，意外退出，使用命令行打开clash-nyanpasu，在控制台发现如上错误。

原因分析：

- Clash Nyanpasu 的 WebKitGTK 前端依赖 GStreamer。gst_video_is_dma_drm_caps 这个函数在 GStreamer 1.24 新引入（见 upstream commit），而 Fedora 40 默认仓库可能只提供 GStreamer 1.22.x。
 也就是说，你的 webkit2gtk 是用 GStreamer 1.24 构建的，但系统里还是旧的 GStreamer 1.22 → ABI 不兼容。
 所以问题根源是 WebKitGTK 和 GStreamer 版本不匹配。 而fedora 40 系统里 gstreamer1-plugins-base 版本太旧，缺少 gst_video_is_dma_drm_caps 符号。

> - GStreamer 是 Linux 上常用的 多媒体框架，提供音视频的解码、播放、流式处理功能。类似于 Windows 上的 DirectShow / Media Foundation。
> - 它由多个模块组成：gstreamer → 核心框架（pipeline、插件机制），不含具体编解码器; gstreamer1-plugins-base → 常用基础插件（音视频格式、视频缩放、转换等）; gstreamer1-plugins-good / bad / ugly → 额外的插件集（按版权/质量分级）; gstreamer1-libav → FFmpeg 后端插件。
> GNOME 桌面、Firefox、WebKitGTK、OBS、媒体播放器（如 Totem）都会用到 GStreamer，所以 Fedora 默认就会带上 核心 gstreamer 包。

解决办法： 

在不升级全系统的情况下，有四种解决办法：

> 备注：我不想用 dnf upgrade --refresh 全量升级，Fedora 一旦全量升级，内核 / Mesa / 驱动都会跟着动，我已经尝试多次升级内核后出现驱动兼容性问题了。

- 方案 1：手动更新单个 GStreamer 相关包
  只更新 gstreamer1 和 gstreamer1-plugins-base，不动核心和驱动。
  ```bash
   sudo dnf update gstreamer1 gstreamer1-plugins-base 
  ```
  碰巧Fedora40的官方库中gstreamer已经升级到了1.24, 解决了问题。

- 方案 2：启用 Fedora Updates-testing 仓库（仅 GStreamer）

  Fedora 的更新分支 updates-testing 里一般会有更新版本的 GStreamer：

  ```bash
   sudo dnf --enablerepo=updates-testing install gstreamer1 gstreamer1-plugins-base
  ```

- 方案 3：自己编译/安装新版 GStreamer

如果你愿意动手，可以单独下载 GStreamer 1.24 的源码，放到 /opt/gstreamer，然后用环境变量让 Clash Nyanpasu 运行时加载：

```bash
export LD_LIBRARY_PATH=/opt/gstreamer/lib64:$LD_LIBRARY_PATH
clash-nyanpasu
```

这样不影响系统自带的旧版本，但 Clash Nyanpasu 可以用新版本。
  
## 参考文档

[clashnyanpasu 官网](https://clashnyanpasu.xyz/)

[最新 Clash Nyanpasu 使用教程快速入门篇](https://clashnyanpasu.org/)
