# 更新记录

## 0.1.0-beta.19 / IDE 0.2.2 - 2026-11-03

- 同步当前生产修复源码，重新构建 Windows、Mac（Apple 芯片 / Intel）、Linux、Android 和 iOS 模拟器包。
- Mac 两种架构均完成签名、公证、票据装订和 Gatekeeper 校验；Windows 仍未代码签名，Android 仍为调试签名测试包。
- 提供 VS Code / IntelliJ IDEA 0.2.2 离线插件；本次未发布插件市场。
- 同步服务器连接器；GitHub 安装脚本固定下载本 Release 对应版本。
- 更新中英文下载入口、SHA-256 校验表和包来源清单。iOS 正式发布保持暂停，模拟器包不能装到真机。
- 本次仅同步 GitHub 源码、文档和分发包；没有重启生产服务或用户容器。

## 安装包说明更新 - 2026-10-19

本次仅更新公开下载文档与历史 Release 提示，没有重新构建或上传安装包。

- Windows / Mac 推荐下载指向官网 0.1.0-beta.17，区分 Apple 芯片与 Intel。
- Mac 当前版要求 macOS 13.5+，已签名、公证、装订并通过 Gatekeeper 校验。
- 明确 Linux / Android 的 GitHub beta.2 为历史测试版，旧版 AppImage 与未签名 Mac 包仅作存档。
- iOS 1.0.0（120）仅限已获邀请的 TestFlight 测试者，尚未在 App Store 公开上架。
- 说明安装包、校验文件、更新元数据和 GitHub 自动生成的文档快照各自用途。

## 0.1.0-beta.1 - 2026-09-24

- 发布 CloseAI Web/PWA、Windows、Linux 和 Android Beta 客户端。
- 支持 ChatGPT 官方授权、Claude、OpenAI API Key 和托管账号申请。
- 支持本地文件、命令和 Git 操作审批。
- 支持多设备、统一会话以及用户与项目记忆。
- 生产环境为每个用户分配独立运行容器和数据卷。
