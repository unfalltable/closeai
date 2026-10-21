# CloseAI in VS Code and IntelliJ IDEA

Use CloseAI from the VS Code sidebar or IntelliJ IDEA tool window, alongside web, desktop and mobile. The same account shares model profiles, quotas, project conversations and Skills. IDE tasks use the explicitly authorized current local project.

| Editor                         | Installation and status                                                                                                                                                                                                                                                                                    |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| VS Code 1.99+                  | [Install from Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=unfalltable.closeai-workbench). Extension ID: `unfalltable.closeai-workbench`; public version **0.2.1**.                                                                                                      |
| IntelliJ IDEA 2026.1 with JCEF | [JetBrains listing](https://plugins.jetbrains.com/plugin/35310-closeai-assistant). The plugin is implemented, but **0.2.0 remains under review and is not publicly installable from the marketplace yet**. If you already have the official ZIP, use Settings → Plugins → gear → Install Plugin from Disk. |

Status checked on 2026-10-21; consult the marketplaces for updates. The client has no separate download license fee. Platform services and model accounts follow the [website prices and order terms](https://closeai.shop/pricing).

## Start a conversation

1. Open your local project and the CloseAI sidebar/tool window.
2. Select browser sign-in, register or sign in on the official CloseAI site, confirm the authorization, then return to the IDE.
3. Choose “Connect and start chatting” and verify the full local project path in the IDE confirmation.
4. If you have no usable model account, follow “Add account or purchase” to the website, then refresh the plugin after completing setup.
5. Choose the model account, model, reasoning effort and task permissions. Remaining quota is shown in the composer.

Registration, purchases, subscriptions and full device management happen in the system browser. The plugins provide project chat and task controls, not inline code completion. Keep the IDE and authorized execution device online for file access.

## Large files and whole projects

Attach files or drag a folder into the composer. A single file can be up to **5 GiB**, subject to remaining account storage. In-browser folder packaging is limited to **256 MiB and 10,000 entries**; create a ZIP locally for larger projects and upload it as a file.

Use an authorized online execution device to unpack and analyze the project as needed. Uploading a project does not put every file into the model context at once. For an existing IDE project or Git repository, connecting the project or cloning it on the authorized device avoids repeated archive uploads.

Review archives before uploading. Remove secrets, private keys and personal files you do not intend to share; exclude dependencies, build output and Git history when unnecessary. Uploads do not automatically exclude these files.

Attachments use private object storage and authenticated downloads. If direct upload is unreachable, CloseAI automatically relays same-origin chunks of at most 8 MiB. Retries resume from the received offset; files become available only after size and SHA-256 verification.

[Open CloseAI](https://closeai.shop) · [中文](IDE_PLUGINS.md)
