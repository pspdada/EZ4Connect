# HITsz Connect for Windows

![Action](https://github.com/chenx-dust/HITsz-Connect-for-Windows/actions/workflows/build.yml/badge.svg)
![Release](https://img.shields.io/github/v/release/chenx-dust/HITsz-Connect-for-Windows)
![Downloads](https://img.shields.io/github/downloads/chenx-dust/HITsz-Connect-for-Windows/total)
![License](https://img.shields.io/github/license/chenx-dust/HITsz-Connect-for-Windows)

专注于 ZJU-Connect 的 ZJU-Connect-for-Windows （HITsz 版）

欢迎加入 HITSZ 开源技术协会 [@hitszosa](https://github.com/hitszosa)

## 使用方式

1. 在本项目的 [Releases](https://github.com/chenx-dust/HITsz-Connect-for-Windows/releases) 页面下载最新版本，将所有文件解压至同一目录下，运行 `HITszConnectForWindows.exe` ；

<div align="center">
<img src="docs/main.png" width="600px">
</div>

2. 在 “功能”-“设置”-“通用” 页面中输入账号（一般为学号）和密码，点击 OK 保存登录信息；

<div align="center">
<img src="docs/config.png" width="400px">
</div>

3. 在主界面中点击“连接服务器”。在默认配置下，若连接正常，软件中日志会显示 `KeepAlive: OK` ；

4. 如果只需进行校园网页浏览，则选择“设置系统代理”后即可使用。

如果需要配合 Clash / Mihomo 进行高级的分流操作，可以参见： [高级使用方式](docs/ADVANCED_USAGE.md)

## 适配指南

本项目为了便于个性化，也为了方便地适配其他可以使用 ZJU-Connect 的学校（如：HITSZ）。

- 程序中引用的应用名称均来自头文件 `utils/utils.h` 中的 `Utils::APP_NAME` ，仓库由同个头文件中的 `Utils::REPO_NAME` 定义；
- CI 配置 `build.yml` 中，`env.TARGET_NAME` 应当与 CMake 项目名称一致，`env.DISPLAY_NAME` 定义了编译结果的文件夹 / 应用名称；
- 默认配置则规定于 `zjuconnectmode.cpp` 和 `settingwindow.cpp` 中。

如有需要，可以自行修改适配。

## 路线图

如有更多好的建议，可以在 Issue 中或是 OSA 群里提出！

- [X] 简化更名流程
- [X] 支持 macOS 系统
- [ ] 支持 Linux 系统
- [ ] 支持手动设置 Proxy Bypass

## 致谢

- [Mythologyli/ZJU-Connect-for-Windows](https://github.com/Mythologyli/ZJU-Connect-for-Windows)
- [Mythologyli/zju-connect](https://github.com/Mythologyli/zju-connect)
