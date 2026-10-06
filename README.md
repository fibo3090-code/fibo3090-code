# fibo3090

I build **local-first, security-minded** software in Rust and TypeScript — tools that run on your
own machine, with no account to create and no server holding your data. I try to actually finish
things: packaged installers for three platforms, a demo you can open in one click, and test suites
instead of hope.

### Try something, right now

|   |   |
|---|---|
| **[Open Transit Diagram Studio →](https://transit-diagram-studio.vercel.app)** | Runs entirely in your browser. Nothing to install, no sign-up. |
| **[Download P2PEM →](https://github.com/fibo3090-code/secure-p2p-chat/releases/latest)** | Windows, macOS and Linux installers, v1.16.2. |

---

## Featured

### [P2PEM](https://github.com/fibo3090-code/secure-p2p-chat) — encrypted peer-to-peer messenger

`Rust` · `Tauri` · `React`  —  [v1.16.2](https://github.com/fibo3090-code/secure-p2p-chat/releases/latest) · 593 Rust test functions · [threat model](https://github.com/fibo3090-code/secure-p2p-chat/blob/main/THREAT_MODEL.md)

<img src="https://raw.githubusercontent.com/fibo3090-code/secure-p2p-chat/main/docs/images/desktop-chat.png" width="820" alt="P2PEM desktop chat window">

Messages travel straight between the two peers. There is no account, and no server keeps your
history. X25519 provides forward secrecy, AES-256-GCM does the encryption, and short
authentication strings let two people detect a man-in-the-middle by reading four words aloud.
NAT hole punching with a relay fallback for networks that refuse to cooperate.

Ships as `.msi` and `.exe` for Windows, `.dmg` for both Intel and Apple-silicon Macs, and
`.deb`, `.rpm` and AppImage for Linux.

### [Transit Diagram Studio](https://github.com/fibo3090-code/transit-diagram-studio) — game maps into Beck-style metro diagrams

`TypeScript` · `React` · `Vite`  —  [live demo](https://transit-diagram-studio.vercel.app) · 121 domain checks + 9 visual regression checks

<img src="https://raw.githubusercontent.com/fibo3090-code/transit-diagram-studio/main/docs/images/editor.png" width="820" alt="Transit Diagram Studio editor">

Drop in a screenshot of a game map, trace the lines, and get a printable diagram in the London
Underground tradition. Everything happens in the browser: no account, no upload, no watermark.
The domain layer is deliberately pure — no DOM, no framework — so the awkward geometry gets
tested directly instead of clicked through: corridor offset signs, index stability through
offsetting, and the snap engine.

### [HIVE](https://github.com/fibo3090-code/hive) — local-first multi-agent platform · *paused*

`Rust` · `Axum` · `React`  —  11-crate Cargo workspace

A coordinator agent turns a brief into sprints and tasks, then dispatches sub-agents that edit
files, run shells and commit code inside a sandbox on your own machine. Four cloud model
providers — OpenAI, Anthropic, Gemini and DeepSeek — plus a local Ollama fallback, so it still
runs with no internet and no API key.

Paused, and shared as-is rather than pretending otherwise.

---

## Experiments

Explorations rather than products, and labelled that way on purpose.

| Project | What it is | Stack |
|---|---|---|
| [corebench](https://github.com/fibo3090-code/corebench) | LLM evaluation across independent capability axes instead of one blended score | Python · Inspect AI |
| [TerraForge](https://github.com/fibo3090-code/TerraForge) | Real-time terrain generator: GPU erosion, river hydrology, heightmap export | Rust · Bevy · WGSL |
| [paris-mobility](https://github.com/fibo3090-code/paris-mobility) | Mobility data lake for Île-de-France — ten years of transit validations, 18.4M rows | Python · DuckDB |
| [ChordGen-AI](https://github.com/fibo3090-code/ChordGen-AI) | Text prompt to MIDI, with a fine-tuned T5 model | Python · PyTorch |

---

**Rust** · **TypeScript** · **Python** — React · Tauri · Next.js · Bevy · Axum · SQLite · PostgreSQL · DuckDB

Found a bug or want to argue about a design decision? Open an issue on the project, or write to
fibo3090@gmail.com.
