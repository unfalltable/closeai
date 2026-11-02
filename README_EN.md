<div align="center">
  <img src="assets/icon.png" width="112" alt="CloseAI Logo" />
  <h1>CloseAI 助手</h1>
  <p><strong>Your computer keeps working while you can be anywhere.</strong></p>
  <p>Direct AI work on your own development environment from desktop, web, mobile, VS Code or IntelliJ IDEA.</p>

[中文](README.md) · **English** · [Open CloseAI](https://closeai.shop)

</div>

> CloseAI is proprietary subscription software. This public distribution repository contains product documentation and official binary packages only. It does not contain CloseAI source code.

## IDE plugins and project uploads

**Use CloseAI in VS Code and IntelliJ IDEA** to continue current-project conversations, choose models and reasoning effort, view quota and control task permissions with the same account used on web, desktop and mobile.

| Entry                                                                                                  | Current status                                                                              |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| VS Code 1.99+ | [GitHub 0.2.2 VSIX](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/closeai-workbench-0.2.2.vsix) · [Marketplace](https://marketplace.visualstudio.com/items?itemName=unfalltable.closeai-workbench) |
| IntelliJ IDEA 2026.1 / JCEF | [GitHub 0.2.2 ZIP](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/closeai-workbench-0.2.2-jetbrains.zip) · [Marketplace](https://plugins.jetbrains.com/plugin/35310-closeai-assistant) |
| [Web workspace](https://closeai.shop)                                                                  | File and project ZIP uploads up to **5 GiB per file**, subject to remaining account storage |

Open a local project → authorize sign-in in your browser → confirm the project directory → choose a model and permissions. Add or purchase a model account on the website when needed, then refresh the plugin. ZIP large folders locally, or connect existing code through the IDE or Git.

[Plugin setup, large-file uploads and project analysis](docs/IDE_PLUGINS_EN.md)

## Downloads: which package should I choose?

Current GitHub release: **[0.1.0-beta.19](https://github.com/unfalltable/closeai/releases/tag/v0.1.0-beta.19)**, updated **2026-11-03**. Desktop, Android and iOS Simulator artifacts have been rebuilt; offline IDE plugins are **0.2.2**. Previous releases remain archived.

| Device | Download | Version and status |
| --- | --- | --- |
| Windows 10/11, Intel / AMD 64-bit | [Windows `.exe`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-Windows-x64.exe) | **0.1.0-beta.19**; unsigned, so SmartScreen may show a prompt |
| Mac, Apple silicon | [`.dmg`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-macOS-arm64.dmg) / [`.zip`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-macOS-arm64.zip) | **0.1.0-beta.19**, macOS **13.5+**; signed, notarized, stapled and Gatekeeper-verified |
| Mac, Intel | [`.dmg`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-macOS-x64.dmg) / [`.zip`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-macOS-x64.zip) | **0.1.0-beta.19**, macOS **13.5+**; signed, notarized, stapled and Gatekeeper-verified |
| Linux, Intel / AMD 64-bit | [`.deb`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-Linux-amd64.deb) / [`.AppImage`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-Linux-x86_64.AppImage) / [portable `.tar.gz`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-Linux-x86_64.tar.gz) | **0.1.0-beta.19**; requires system desktop libraries |
| Android | [Test `.apk`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-Android-debug.apk) | **0.1.0-beta.19**; debug-signed for sideload testing, not a Google Play release |
| iPhone / iPad | [Safari web app / Add to Home Screen](https://closeai.shop) | Formal iOS publishing remains paused; no IPA, TestFlight or App Store upload in this release |
| iOS developers on Mac | [iOS Simulator `.app.zip`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/CloseAI-0.1.0-beta.19-iOS-Simulator.app.zip) | Fresh simulator build; **not installable on iPhone / iPad**; native internal version 0.1.0 (2) |
| VS Code 1.99+ | [Offline `.vsix`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/closeai-workbench-0.2.2.vsix) | **0.2.2**; Extensions → Install from VSIX |
| IntelliJ IDEA 2026.1 with JCEF | [Offline plugin `.zip`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/closeai-workbench-0.2.2-jetbrains.zip) | **0.2.2**; Settings → Plugins → Install Plugin from Disk |
| Linux server | [Installer](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/install-closeai-server.sh) / [Connector](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/closeai-server-connector.cjs) | Current source; installer downloads this exact release's connector; Node.js 20+ |
| Browser / PWA | [Open CloseAI](https://closeai.shop) | No installer; the connected project computer or server must stay online |

Choose the Mac architecture in **Apple menu → About This Mac**. Prefer `.dmg` for normal installation. Marketplace releases are separate; this release updates offline IDE packages only.

Each package has a matching `.sha256`; [SHA256SUMS.txt](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/SHA256SUMS.txt) and [release-manifest.json](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.19/release-manifest.json) list checksums and provenance. See the [installation guide](docs/INSTALLATION.md). Desktop automatic updates use the separate website channel; this release provides manual downloads. GitHub's automatic **Source code (zip / tar.gz)** files contain this public documentation repository, **not installers or product source**.

## Getting started

1. Register and sign in to CloseAI.
2. Subscribe, then connect ChatGPT, Claude, or an OpenAI API key, or request an additional paid CloseAI-managed account.
3. Install CloseAI on the development computer, enter the one-time pairing code, and choose the project directory it may access.
4. In the workspace, choose a project, online computer, model account, and model before sending a task.
5. Approve file writes, commands, and Git operations before they run on the development computer.
6. Keep the development computer online to continue the same session from a phone, browser, or another computer.

CloseAI does not host complete source repositories by default. Your repositories remain on your computer or your own Git remote.

## Support and security

Use [GitHub Issues](https://github.com/unfalltable/closeai/issues) for ordinary feedback. Follow the [security policy](SECURITY.md) for sensitive reports. Never post passwords, cookies, API keys, server credentials, personal data, or user code in a public issue.

## License

CloseAI is proprietary commercial software. Download and use of the official client are governed by the [CloseAI Proprietary Software License](LICENSE) and applicable subscription or order terms.
