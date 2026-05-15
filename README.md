<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:A8E55C,100:2DC94E&height=200&section=header&text=NetLeafy&fontSize=62&fontColor=ffffff&fontAlignY=38&desc=VLESS%20Config%20Generator%20%E2%80%A2%20Web%20App&descSize=20&descAlignY=60&descColor=efffef" alt="NetLeafy" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=800&color=2DC94E&center=true&vCenter=true&width=600&lines=Generate+VLESS+Configs+in+One+Click;Bypass+restrictions+with+ease!;IP+%2B+SNI+%7C+Direct+SNI+Modes;XHTTP+Parameter+Editor;20%2B+Community+Servers" alt="Typing animation" />

<br/>

[![Live Demo](https://img.shields.io/badge/Live%20Demo-NetLeafy-2DC94E?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=1a1a1a)](https://Code-Leafy.github.io/NetLeafy)
[![License](https://img.shields.io/badge/License-MIT-A8E55C?style=for-the-badge&labelColor=1a1a1a)](LICENSE)
[![Telegram](https://img.shields.io/badge/Channel-%40codeleafy-2DC94E?style=for-the-badge&logo=telegram&logoColor=white&labelColor=1a1a1a)](https://t.me/codeleafy)
[![GitHub](https://img.shields.io/badge/GitHub-Code--Leafy-A8E55C?style=for-the-badge&logo=github&logoColor=white&labelColor=1a1a1a)](https://github.com/Code-Leafy)

<br/>

> **A clean, fast, browser-based tool for generating VLESS XHTTP configs.**  
> Built specifically for Netlify routing. No install. No setup. Open it and go.

<br/>

</div>

---

## 🌐 Live App

### 👉 [Code-Leafy.github.io/NetLeafy](https://Code-Leafy.github.io/NetLeafy)

Works on any device — desktop, mobile. 100% client-side, no installation required.

---

<div align="center">

## 📚 Quick Start Guides

Need help getting started? We've prepared detailed, step-by-step tutorials on our Telegram channel to walk you through everything. Click below to read:

[![How to Connect](https://img.shields.io/badge/🚀_How_to_Connect-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white&labelColor=1a1a1a)](https://t.me/CodeLeafy/7)
[![Get Netlify Domain](https://img.shields.io/badge/🌐_Get_Netlify_Domain-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white&labelColor=1a1a1a)](https://t.me/CodeLeafy/8)
[![Setup Custom Server](https://img.shields.io/badge/🛠️_Setup_Custom_Server-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white&labelColor=1a1a1a)](https://t.me/CodeLeafy/10)

</div>

---

## ✨ Features

- ⚡ **Instant Config Generation** — Paste your SNIs and IPs, pick a server, and generate hundreds of VLESS configs in milliseconds.
- 🔀 **Two Generation Modes** — IP + SNI or Direct SNI.
- 🩺 **Live Domain Health Checker** — Validates your Netlify domain via API before generation, complete with green/red pulse animations.
- ✏️ **XHTTP Parameter Editor** — Modify existing VLESS configs in bulk: edit padding bytes, obfs mode, custom headers, and chunk sizes.
- 🖥️ **20+ Community Servers** — Pre-loaded, community-donated servers with live **Green (Working)** and **Red (Down)** visual pulse indicators.
- 📋 **Copy / Download / Import** — One-click copy, `.txt` download, or send generated configs directly to the built-in XHTTP editor.
- 📱 **Fully Responsive** — Slide-out sidebar, mobile topbar, and smooth layout transitions for modern phones.
- 🎨 **Polished UI** — Smooth animations, grid background, teal glow, and particle burst effects on successful actions.

---

## 🛠️ Tools Inside

### 1 · Config Generator

The main tool. Fill in your details and generate ready-to-import VLESS XHTTP configs.

| Field | Description |
|-------|-------------|
| **Netlify Domain** | Your CDN host used in the `host` parameter. Validated live with the built-in checker. |
| **SNI List** | One SNI per line. These become the TLS server name in each config. |
| **IP List** | *(IP + SNI mode only)* Clean IPs, one per line. Each IP is paired with every SNI. |
| **Server** | Choose from community servers or define your own (name, address, user UUID, path). |

**Generation Modes:**

| Mode | How it works |
|------|-------------|
| 🌐 **IP + SNI** | Pairs every IP with every SNI → maximum config count, best for finding clean routes. |
| 🔗 **Direct SNI** | Uses the SNI directly as the config address → fewer configs, simpler setup. |

<br/>

> [!IMPORTANT]
> ### ⚠️ Note on using the "IP + SNI" Method
> To use this method reliably, you will need to buy a plan from [shecan.ir/#plans](https://shecan.ir/#plans).
> 
> 📖 **For full instructions, head over to:** [**How to connect (Tutorial)**](https://t.me/CodeLeafy/1)
> 
> **Testing without a plan:** For some networks, it might actually work *without* buying Shecan! To test if your network supports it naturally, use our [**SNI/IP Scanner**](https://github.com/Code-Leafy/NetLeafyScanner).
> 
> 💡 **All of our tutorials, updates, and guides are posted on our Telegram Channel. Make sure to join! 👉 [t.me/CodeLeafy](https://t.me/CodeLeafy)**

<br/>

**Output Format Example:**
```text
vless://<uuid>@<ip_or_sni>:443?encryption=none&security=tls&sni=<sni>&fp=chrome
  &alpn=h2%2Chttp%2F1.1&insecure=1&allowInsecure=1&type=xhttp&host=<host>
  &path=<path>&mode=auto&extra=<url_encoded_xhttp_params>#🌐 @CodeLeafy | <sni> | <server>
```

---

### 2 · XHTTP Editor

Takes existing VLESS configs and safely rewrites the encoded `extra` parameter inside them. Useful for fine-tuning configs you already have without having to regenerate them from scratch.

| Parameter | What it does |
|-----------|-------------|
| `xPaddingBytes` | Range of padding bytes added to each packet (e.g. `1-1`). |
| `scMaxEachPostBytes` | Max bytes per POST chunk (e.g. `1000000`). |
| `xPaddingObfsMode` | Enables/disables obfuscation mode (`true` / `false`). |
| `xPaddingKey` | Key used for padding generation (e.g. `iran`). |
| `xPaddingHeader` | Header name for padding (e.g. `iran`). |
| `Custom Headers` | Inject arbitrary headers via JSON: `{"x-host": "http://cdn.example.com:444"}`. |

Paste your configs → adjust parameters → click **Update Configs** → copy or download.

---

### 3 · Community Servers

Pre-loaded servers contributed by the community. Each server features a real-time visual indicator in the UI:

| Status Dot | Meaning |
|------------|---------|
| 🟢 **Pulsing Green** | Server is active and accepting connections (`status: "working"`). |
| 🔴 **Pulsing Red** | Server is currently unreachable or down (`status: "down"`). |

You can also use your own server by switching to **Custom** and supplying:
- Server Name
- Address (host + port, e.g., `cdn.example.com:444`)
- User UUID
- Path (e.g., `/mypath`)

---

## 📤 Output Options

After generating configs, a sleek modal appears providing multiple export routes:

| Button | Action |
|--------|--------|
| **Click to see configs** | Un-blurs the secure output area to let you view the raw configs. |
| **Import to XHTTP Editor** | Sends the newly generated configs straight into the XHTTP Editor tab. |
| **Copy to Clipboard** | Copies all configs with a satisfying green particle burst animation ✨. |
| **Download .txt** | Downloads a timestamped `.txt` file containing your configs. |

---

## 📁 Repository Structure

```text
NetLeafy/
├── index.html        # The core app (HTML/CSS/JS all-in-one)
├── favicon.png       # app icon
├── README.md         # This documentation file
└── LICENSE           # MIT License
```

---

## 🤝 Contributing (Adding a Server)

Community servers are the heartbeat of this tool and what keep it so useful for everyone! Do you have a server you'd like to donate or share with the community? 

To easily get your server added to the built-in public list, just reach out to me directly on Telegram:

<br/>

<div align="center">

[![Add Your Server](https://img.shields.io/badge/💬_Contact_to_Add_Server-%40CodeLeafy-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white&labelColor=1a1a1a)](https://t.me/CodeLeafy?direct)

</div>

<br/>

---

## 📣 Channel & Support

<div align="center">

[![Telegram](https://img.shields.io/badge/Join%20Channel-%40codeleafy-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/codeleafy)

**Get the latest info on Telegram.**

</div>

---

## ⚖️ License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
<div align="center">

Made with ❤️ by [Code-Leafy](https://github.com/Code-Leafy)
<br/>
Inspired by IR-Netlify

[![GitHub stars](https://img.shields.io/github/stars/Code-Leafy/NetLeafy?style=social)](https://github.com/Code-Leafy/NetLeafy/stargazers)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:A8E55C,100:2DC94E&height=100&section=footer" width="100%"/>

</div>
