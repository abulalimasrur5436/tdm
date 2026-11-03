<p align="center">
  <img src="assets/logo.png" width="96" height="96" alt="Turbo Download Manager Logo" />
</p>

<h1 align="center">⚡ Turbo Download Manager (TDM)</h1>

<p align="center">
  <strong>Next-Generation High-Performance Download Manager for Windows</strong><br>
  <em>Built with Python 3.14, Microsoft Edge WebView2, SQLite & High-Concurrency Multi-Thread Engines.</em>
</p>

<p align="center">
  <a href="https://github.com/abulalimasrur5436/tdm/releases/latest"><img src="https://img.shields.io/github/v/release/abulalimasrur5436/tdm?style=for-the-badge&logo=github&color=7B6EDF&label=Latest%20Version" alt="Latest Release" /></a>
  <a href="https://github.com/abulalimasrur5436/tdm/releases"><img src="https://img.shields.io/github/downloads/abulalimasrur5436/tdm/total?style=for-the-badge&logo=windows&color=33C27A&label=Downloads" alt="Total Downloads" /></a>
  <img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows" alt="Platform Windows" />
  <img src="https://img.shields.io/badge/Python-3.14-3776AB?style=for-the-badge&logo=python" alt="Python 3.14" />
  <img src="https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge" alt="License MIT" />
</p>

---

## 🌟 Overview

**Turbo Download Manager (TDM)** is an open-source, ultra-fast, and modern download accelerator designed to replace legacy, trial-restricted software like Internet Download Manager (IDM). 

Combining an ultra-modern Fluent Dark/Light web interface with low-level multithreaded networking, **Turbo Download Manager (TDM)** dynamically breaks files into up to **32 parallel segments**, utilizes dynamic segment stealing to saturate your bandwidth, seamlessly grabs video/audio streams from web browsers, and provides **1-click silent background updates**.

---

## 🚀 Key Features

### ⚡ 1. Hyper-Speed Multi-Segment Engine
* **Up to 32 Parallel Connections:** Splits downloads across multiple concurrent TCP streams with HTTP `Range` requests.
* **Dynamic Segment Stealing:** Prevents stalled chunks by allowing active threads to claim and divide unfinished portions from lagging connections.
* **BDIX & Local ISP Server Turbo:** Optimized buffering (256 KB – 2 MB dynamic chunks) ensuring maximum speeds on local gigabit networks and high-latency international mirrors.

### 🎥 2. Smart Video Sniffer & Quality Selector
* **Browser Extension Support (Chrome / Edge / Brave / Opera):** Automatically detects video streams and audio media as you browse.
* **Interactive Quality Chooser:** Choose your preferred format directly from the download modal — **4K, 1440p, 1080p, 720p, 480p**, or extract **Audio-Only (MP3/M4A)** with full FFmpeg merging.
* **Streaming Platform Ready:** Native support for YouTube, Facebook Reels/Videos, TikTok, Vimeo, and direct ISP FTP portals (CircleFTP, SamOnline, etc.).

### ⏱️ 3. Total Time Taken & Real-Time Stopwatch
* **Live Duration Tracking:** Real-time elapsed duration display (`45s`, `02m 14s`, `01h 05m`) during active downloads.
* **Pause / Resume Memory:** Accurately retains spent duration across pause and resume cycles.
* **Interactive Header Sorting:** Sort your download history instantly by **Time Taken**, **File Name**, **Size**, **Speed**, **Status**, or **Added Date** with one-click toggles (`▲` / `▼`).

### 🔄 4. Zero-Friction In-App Auto-Updater
* **IDM-Style Background Updates:** App automatically checks GitHub Releases for new updates without interrupting your workflow.
* **1-Click Self Installation:** Downloads the latest update silently in the background, updates files cleanly, and restarts seamlessly.

### 🎨 5. Modern Glassmorphic Dashboard
* **Native WebView2 UI:** Zero-lag UI rendered via Chromium Edge WebView2 with CustomTkinter desktop fallback.
* **Dark & Light Mode:** Tailored design system with high-contrast readable typography, subtle gradients, and customizable theme settings.
* **System Tray & Daemon Mode:** Minimizes unobtrusively to the system tray (`--daemon`) to capture downloads silently on Windows boot.

### 🛡️ 6. Built-in Security & Storage Cleaner
* **Antivirus Integration:** Automatic background verification with Windows Defender or ClamAV upon download completion.
* **Disk Cleaner:** Built-in scanner to identify, preview, and wipe leftover temporary download fragments with one click.

---

## 📊 Feature Comparison

| Feature | Turbo Download Manager (TDM) | Internet Download Manager (IDM) | Free Download Manager (FDM) | Browser Default |
| :--- | :---: | :---: | :---: | :---: |
| **Price & License** | **100% Free & Open Source (MIT)** | Paid License (30-day trial nag) | Free (Closed source components) | Free |
| **Max Connections** | **32 Parallel Streams** | 32 Parallel Streams | 10 Parallel Streams | 1 Stream |
| **Dynamic Chunk Stealing** | ✅ **Yes** | ✅ Yes | ❌ Limited | ❌ No |
| **Video Quality Selection Modal** | ✅ **Yes (4K/1080p/Audio-only)** | ❌ Fixed link grabber | ⚠️ Partial | ❌ No |
| **Total Download Duration Column** | ✅ **Yes (Sortable Live Stopwatch)**| ❌ No | ❌ No | ❌ No |
| **Modern Fluent UI (Light/Dark)** | ✅ **Yes (WebView2)** | ❌ Windows 98 / XP UI | ⚠️ Basic Dark Mode | ❌ Minimal |
| **In-App Silent Updater** | ✅ **Yes (GitHub Releases CDN)** | ⚠️ Manual dialog | ⚠️ Periodic prompt | ⚠️ Browser update |
| **Local ISP / BDIX Filename Auto-Detection** | ✅ **Yes** | ⚠️ Often blank/raw script name | ⚠️ Basic | ❌ No |

---

## 📥 Installation

### Option 1: Official Windows Installer (Recommended)
1. Download the latest installer from [Releases](https://github.com/abulalimasrur5436/tdm/releases/latest):
   ```
   TurboDownloader-Setup.exe
   ```
2. Run the installer and follow the quick setup wizard.
3. The installer automatically:
   - Configures application shortcuts on your Desktop and Start Menu.
   - Registers Windows startup daemon for background download interception.
   - Pairs with Chromium browsers (Chrome, Edge, Brave).

### Option 2: Running from Source
Requires **Python 3.10+** (Tested on Python 3.14):

```bash
# 1. Clone the repository
git clone https://github.com/abulalimasrur5436/tdm.git
cd tdm

# 2. Install required dependencies
pip install -r requirements.txt

# 3. Launch the application
python main.py
```

---

## 🌐 Browser Extension Setup

**Turbo Download Manager (TDM)** includes a high-performance Chrome/Edge Manifest V3 extension for automated link interception and video detection.

```
┌────────────────────────┐         WebSocket / HTTP          ┌────────────────────────┐
│  Chrome / Edge Browser │ ────────────────────────────────> │      TDM App Engine    │
│  (Video Sniffer Ext)   │ <──────────────────────────────── │   (Port: 48921)        │
└────────────────────────┘          Auto-Grab Event          └────────────────────────┘
```

### Quick Install:
1. Open your browser and navigate to:
   - Chrome: `chrome://extensions/`
   - Edge: `edge://extensions/`
2. Enable **"Developer mode"** (top right toggle).
3. Click **"Load unpacked"** and select the `browser_extension` folder inside your Turbo Download Manager directory.
4. Pin the **Turbo Download Manager (TDM)** icon to your toolbar. Video capture buttons will now appear on video streaming sites automatically!

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>N</kbd> | Open **Add Download** Modal |
| <kbd>Ctrl</kbd> + <kbd>,</kbd> | Open **Application Settings** |
| <kbd>F5</kbd> | Refresh Downloads List from SQLite Database |
| <kbd>Delete</kbd> | Delete Selected Downloads (with optional disk file removal) |
| <kbd>Space</kbd> | Pause / Resume Selected Download Task |

---

## 🏗️ Architecture & Tech Stack

```
tdm/
├── assets/                 # App icons, branding logos, visual assets
├── bin/                    # Embedded high-throughput binaries (aria2c.exe, ffmpeg.exe)
├── browser_extension/      # Chrome/Edge Manifest V3 Native Video Sniffer
├── src/
│   ├── core/               # Concurrency engine, segment downloader, database, auto-updater
│   │   ├── database.py     # High-speed SQLite database with WAL & auto-migration
│   │   ├── task_manager.py # State machine & event dispatcher (pause, resume, chunk allocation)
│   │   ├── downloader.py   # Multi-part chunk downloader & dynamic segment stealer
│   │   └── updater.py      # GitHub Releases in-app background auto-updater
│   ├── integrations/       # Local loopback server (port 48921) for browser extension bridge
│   ├── security/           # Virus scanner (Windows Defender / ClamAV) & integrity checkers
│   ├── utils/              # Helper functions, speed testers, duration/byte formatters
│   ├── ui/                 # CustomTkinter fallback GUI & IDM-style native dialogs
│   └── web_ui/             # Modern HTML5/CSS3/ES6 responsive dashboard (Edge WebView2)
│       ├── index.html      # 9-column grid table with interactive sortable headers
│       ├── style.css       # Theme variables, responsive layouts, glassmorphic cards
│       └── app.js          # Reactive controller, live WebSocket progress listeners
├── installer.iss           # Inno Setup 6 enterprise deployment script
├── TurboDownloader.spec    # PyInstaller production build manifest
└── main.py                 # Application bootstrapper & single-instance orchestrator
```

* **Core Language:** Python 3.14 (Optimized for multi-threaded socket I/O).
* **Database:** SQLite 3 with Write-Ahead Logging (`WAL`) for instant concurrent task queries.
* **Frontend UI:** Microsoft Edge WebView2 via `pywebview` with zero-overhead DOM rendering.
* **Streaming Engine:** Integrated `yt-dlp` and `FFmpeg` for pristine video stream multiplexing.
* **Packaging:** PyInstaller + Inno Setup 6 with ultra-compressed LZMA2 packaging.

---

## 🛠️ Building Executable from Source

To compile the standalone Windows executable and installer yourself:

```powershell
# 1. Compile with PyInstaller
python -m PyInstaller TurboDownloader.spec --noconfirm

# 2. Build Inno Setup Installer
& "C:\Program Files (x86)\Inno Setup 6\ISCC.exe" installer.iss
```
The compiled installer `TurboDownloader-Setup.exe` will be generated in the `dist/` directory.

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project (`https://github.com/abulalimasrur5436/tdm/fork`)
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/abulalimasrur5436"><strong>Abul Ali Masrur</strong></a> & Open-Source Contributors.<br>
  <em>If you find Turbo Download Manager (TDM) helpful, please give this repository a ⭐ on GitHub!</em>
</p>
