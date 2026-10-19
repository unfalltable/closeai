<div align="center">
  <img src="assets/icon.png" width="112" alt="CloseAI Logo" />
  <h1>CloseAI 助手</h1>
  <p><strong>Your computer keeps working while you can be anywhere.</strong></p>
  <p>Direct AI work on your own development environment from desktop, web, or mobile.</p>

[中文](README.md) · **English** · [Open CloseAI](https://closeai.shop)

</div>

> CloseAI is proprietary subscription software. This public distribution repository contains product documentation and official binary packages only. It does not contain CloseAI source code.

## Downloads: which package should I choose?

**Start with the [official download page](https://closeai.shop).** Current Windows and Mac packages are hosted on the official website. GitHub releases beta.1 and beta.2 are historical test builds, not the current website release.

Status checked on **2026-10-19**. Use the official download page for subsequent releases.

| Your device | Recommended package | Version and status |
| --- | --- | --- |
| Windows 10/11, Intel / AMD 64-bit | [Windows `.exe`](https://closeai.shop/desktop-releases/CloseAI%20%E5%8A%A9%E6%89%8B-0.1.0-beta.17-Windows-x64.exe) | **0.1.0-beta.17**; currently unsigned on Windows; SmartScreen may show a warning |
| Mac, Apple silicon (M series) | [Apple silicon `.dmg`](https://closeai.shop/desktop-releases/CloseAI%20%E5%8A%A9%E6%89%8B-0.1.0-beta.17-macOS-arm64.dmg) | **0.1.0-beta.17**; macOS **13.5+**; signed, notarized, stapled, and Gatekeeper-verified |
| Mac, Intel processor | [Intel `.dmg`](https://closeai.shop/desktop-releases/CloseAI%20%E5%8A%A9%E6%89%8B-0.1.0-beta.17-macOS-x64.dmg) | **0.1.0-beta.17**; macOS **13.5+**; signed, notarized, stapled, and Gatekeeper-verified |
| Linux, Intel / AMD 64-bit | [Debian / Ubuntu `.deb`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.2/CloseAI-0.1.0-beta.2-Linux-amd64.deb) / [Portable `.tar.gz`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.2/CloseAI-0.1.0-beta.2-Linux-x86_64.tar.gz) | Historical **0.1.0-beta.2** test build; package releases are not synchronized with Windows / Mac |
| Android 7+ | [Test `.apk`](https://github.com/unfalltable/closeai/releases/download/v0.1.0-beta.2/CloseAI-0.1.0-beta.2-Android-debug.apk) | Historical **0.1.0-beta.2** build; debug signed, for sideload testing; not a Google Play release |
| iPhone / iPad | [Safari web app / Add to Home Screen](https://closeai.shop) | Native **1.0.0 (120)** available to invited TestFlight testers only; **not publicly released on the App Store** |
| Browser / PWA | [Open the workspace](https://closeai.shop) | No installer needed; the connected computer or server must stay online to operate on projects |

On a Mac, open **Apple menu → About This Mac**: choose `arm64` for an Apple chip and `x64` for an Intel processor. Both provide the same application features.

### Other files in a release

| File | Purpose |
| --- | --- |
| `.exe`, `.dmg`, `.deb`, `.apk` | Installers; choose the one for your platform |
| Linux `.tar.gz` / historical `.AppImage` | Alternative Linux package formats; the old AppImage is an archive build |
| Mac `.zip` / historical `.app.zip` | Application archives; use the current `.dmg` for normal installation; the unsigned beta.2 archives are no longer recommended |
| `.sha256` / `SHA256SUMS-*.txt` | Download checksums, not installers |
| `latest-*.json` / `.squirrel.json` | Client update metadata; no manual installation needed |
| GitHub's automatic **Source code (zip / tar.gz)** | A snapshot of this public documentation repository, **not an installer or the product source code** |

Website Windows / Mac installers have matching `.sha256` files. For Linux, use `SHA256SUMS-closeai-linux.txt` from the same release. See the [installation guide](docs/INSTALLATION.md) for verification, installation, and updates.

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
