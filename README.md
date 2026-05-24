<div align="center">

<!-- HERO -->
<img src="https://raw.githubusercontent.com/Code-Leafy/NetLeafy/main/favicon.png" alt="NetLeafy Logo" width="80" height="80" />

# NetLeafy

Advanced VLESS-over-xHTTP configuration engine for Netlify infrastructure.

<p align="center">
  <img src="https://img.shields.io/badge/version-1.3-10B981?style=flat-square" />
  <img src="https://img.shields.io/badge/license-MIT-10B981?style=flat-square" />
  <img src="https://img.shields.io/badge/platform-Web-10B981?style=flat-square" />
</p>

### [🟢 Open Config Generator](https://Code-Leafy.github.io/NetLeafy)

</div>

---

<div align="center">

<!-- VISUAL PREVIEW -->
<img src="https://github.com/Code-Leafy/NetLeafy/blob/main/assets/image.png?raw=true" alt="NetLeafy Preview" width="720" style="border-radius: 12px; border: 1px solid rgba(0,0,0,0.05);">

</div>

<br>

## Overview

NetLeafy is a high-performance, client-side configuration generator designed to bypass network restrictions using the modern **xHTTP** protocol. By leveraging Netlify’s global edge network as a front-end relay, it enables highly resilient connections that are difficult to intercept or block.

> **Privacy First:** This tool is 100% serverless. All UUIDs, server addresses, and generated configs are processed locally in your browser. No data ever leaves your device.

---

### Core Features

#### ⚡ Hybrid Routing Engine
Toggle between **Direct SNI** for standard bypass and **IP + SNI (Shecan Mode)** for maximum reliability in highly censored environments.

#### 🧩 Intelligence Integration
Switch seamlessly between community-donated servers, custom private node inputs, or the **G2ray Extractor**, which automatically converts standard VLESS links into Netlify-ready xHTTP configs.

#### 🛠️ Precision XHTTP Editor
A dedicated workspace to batch-refine protocol parameters including `xPaddingBytes`, `scMaxEachPostBytes`, and custom JSON headers for advanced traffic obfuscation.

---

## Getting Started

> **Note:** NetLeafy is a monolithic web application. You can use the hosted version or run it locally.

### Option 1: Quick Access (Recommended)
Access the generator immediately at: **[Code-Leafy.github.io/NetLeafy](https://Code-Leafy.github.io/NetLeafy)**

### Option 2: Local Usage
1. [Download the latest release](https://github.com/Code-Leafy/NetLeafy/archive/refs/heads/main.zip) or clone the repo.
2. Locate the `index.html` file.
3. Open it in any modern web browser.

<details>
<summary><kbd>📁</kbd> Project Structure</summary>

```text
NetLeafy/
├── assets/           # Visual assets and previews
├── favicon.png       # App icon
├── index.html        # Core application (Logic + UI)
└── README.md         # Documentation
```

</details>

---

<details>
<summary><kbd>❓</kbd> FAQ & Troubleshooting</summary>

**What is the advantage of xHTTP?**
xHTTP mimics standard web traffic (POST/GET) more effectively than traditional WebSocket or gRPC, making it highly resistant to Deep Packet Inspection (DPI).

**Why use IP + SNI mode?**
Using a "Clean IP" alongside a valid SNI allows the connection to bypass DNS-based filtering and IP-based blacklisting of Netlify's common ranges.

</details>

<br>

<div align="center">

[MIT License](https://github.com/Code-Leafy/NetLeafy/blob/main/LICENSE) · Crafted by [Code-Leafy](https://github.com/Code-Leafy)

</div>
