# CloseAI 助手安装指南

先到[官网下载页](https://closeai.shop)选择设备。当前 Windows / Mac 推荐版为 **0.1.0-beta.17**；[GitHub beta.2](https://github.com/unfalltable/closeai/releases/tag/v0.1.0-beta.2) 保留 Linux、Android 等早期测试包。核对日期：**2026-10-19**。

## 先选对文件

| 设备 | 选择 | 注意 |
| --- | --- | --- |
| Windows 10/11，Intel / AMD 64 位 | `*-Windows-x64.exe` | Windows 版暂未代码签名 |
| Apple M 系列 Mac | `*-macOS-arm64.dmg` | 当前版要求 macOS 13.5+，已签名、公证 |
| Intel Mac | `*-macOS-x64.dmg` | 当前版要求 macOS 13.5+，已签名、公证 |
| Debian / Ubuntu x64 | `*-Linux-amd64.deb` | beta.2 历史测试版 |
| 其他 Linux x64 | `*-Linux-x86_64.tar.gz` | beta.2 便携测试版，仍依赖系统桌面运行库 |
| Android 7+ | `*-Android-debug.apk` | beta.2 侧载测试版，不是 Google Play 正式包 |
| iPhone / iPad | Safari 打开 `closeai.shop` | 原生版目前仅限已获邀请的 TestFlight 测试者，App Store 尚未公开上架 |

`x64`、`amd64`、`x86_64` 都指 Intel / AMD 的 64 位架构；Apple 芯片请选择 `arm64`。这里没有提供 Windows ARM 或 Linux ARM 原生安装包。

## 核对下载

从安装包地址后加 `.sha256` 下载同名校验文件；Linux 包则使用同一个 GitHub Release 中的 `SHA256SUMS-closeai-linux.txt`。不要使用其他版本的校验值。

Windows 在文件所在目录打开 PowerShell，输入 `Get-FileHash ` 后把下载的 `.exe` 拖入终端，再补上 ` -Algorithm SHA256` 回车。对比输出 Hash 与 `.sha256` 的第一段内容，大小写不影响结果。

macOS / Linux 在终端切换到下载目录，使用文件的实际名称（有空格时保留引号）：

```bash
# macOS 示例
shasum -a 256 "CloseAI 助手-0.1.0-beta.17-macOS-arm64.dmg"

# Linux beta.2：两个安装包都已下载时，可一起核对
sha256sum -c SHA256SUMS-closeai-linux.txt
```

Linux 只下载其中一个包时，另一个会提示不存在；确认已下载的文件显示 `OK` 即可。校验不一致时停止安装，重新从官方渠道下载。

## Windows

1. 下载推荐的 `.exe` 并核对校验值，双击安装。
2. 当前 Beta 未接入 Windows 代码签名，可能出现 SmartScreen 提示。先核对官方来源和校验值；不确定时取消安装并联系支持，无需关闭系统安全防护。
3. 启动「CloseAI 助手」并登录原有平台账号。
4. 需要操作当前电脑的项目时，进入「我的设备 → 连接当前电脑」，授权工作空间目录。

旧版本可能显示 `CloseAI` 或 `LoopPu`；官网更新源仍保留 `LoopPu-*.exe` 兼容文件名，同版本安装包与「CloseAI 助手」下载名称对应同一文件内容。升级时先退出旧客户端，再运行官方新安装包；无需先清除账号和项目数据。

## macOS

1. 打开 ** → 关于本机**，确认是 Apple 芯片还是 Intel，并确认系统为 **macOS 13.5 或更高**。
2. 下载对应的当前 `.dmg`，核对校验值后打开。
3. 将「CloseAI 助手」拖到「应用程序」，从「应用程序」启动，而不是长期从 DMG 内运行。
4. 在「我的设备」连接当前 Mac，并按系统提示授予所选目录必要的访问权限。

当前 beta.17 的 Apple 芯片与 Intel 版均已完成 Developer ID 签名、Apple 公证、票据装订与 Gatekeeper 校验。**不需要执行旧教程里的 `xattr -cr`，也无需关闭 Gatekeeper。** 若系统仍提示文件损坏或无法验证，请核对下载来源、系统版本与校验值后联系支持。

Mac `.zip` 主要供应用更新使用；普通安装优先选 `.dmg`。GitHub beta.2 的 `.app.zip` 是未签名旧测试包，不再推荐作为新安装入口。

## Linux

当前公开 Linux 客户端为 **beta.2 历史测试版**，未与 Windows / Mac beta.17 同步发包。

Debian / Ubuntu，在下载目录执行：

```bash
sudo apt install ./CloseAI-0.1.0-beta.2-Linux-amd64.deb
```

便携包，在下载目录执行：

```bash
tar -xzf CloseAI-0.1.0-beta.2-Linux-x86_64.tar.gz
```

进入解压目录后启动其中的 `CloseAI` 程序。便携包仍需要系统桌面运行库；如果缺少依赖或无法启动，可以先用[网页版](https://closeai.shop)。beta.1 的 AppImage 仅保留作历史存档，不是当前推荐包。

## Android

1. 下载 beta.2 的 `.apk`，同时下载同名 `.sha256` 核对。
2. 仅对用于安装的文件管理器临时允许「安装未知应用」。
3. 安装完成后关闭该临时权限，打开应用并登录。

此 APK 使用调试签名，仅供侧载测试；没有作为 Google Play 正式版发布。Android 客户端用于发送任务、查看进度和回复问题，项目文件与命令由已连接的电脑或服务器处理。

## iPhone / iPad

普通用户用 Safari 打开 [closeai.shop](https://closeai.shop)，也可以通过「分享 → 添加到主屏幕」使用。

原生 **1.0.0（120）** 已在 TestFlight 内测中验证冷启动与本地通知，当前仅限已获邀请的测试者。**尚未公开上架 App Store，也没有面向普通用户的直接安装 IPA。** 网页/PWA、TestFlight 内测与 App Store 上架是不同渠道，不能相互代替。

若在其他归档中看到 `iOS-simulator` 或模拟器 `.app.zip`，它只能用于 Mac 上的 iOS 模拟器，不能安装到 iPhone / iPad。

## 网页、PWA 和服务器连接器

打开[在线工作台](https://closeai.shop)即可登录。浏览器登录并不会自动授权读取电脑目录；操作本地文件需要连接电脑，操作服务器项目需要该服务器的连接器在线。

Linux 服务器无需安装桌面客户端：在「我的设备 → 连接自己的服务器」中先连接并检查环境，再选择工作空间目录，按向导完成连接器安装。连接器是设备接入组件，不是另一个桌面安装包。

## 不用手动安装的文件

- `.sha256`、`SHA256SUMS-*.txt`：校验值。
- `latest-*.json`、`.squirrel.json` 等：客户端更新元数据。
- GitHub 自动生成的 **Source code (zip / tar.gz)**：本公开文档仓库的快照，既不是安装程序，也不包含闭源产品源码。

遇到问题，可提交[公开 Issue](https://github.com/unfalltable/closeai/issues)并附上系统、架构、安装包版本及错误提示；不要上传密码、设备令牌、Cookie 或其他私密资料。
