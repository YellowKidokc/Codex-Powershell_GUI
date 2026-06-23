# Codex Script Hub

A dark-themed PySide6 launcher for PowerShell, Python, and batch scripts.

![PySide6](https://img.shields.io/badge/PySide6-6.7+-blue)
![Python](https://img.shields.io/badge/Python-3.8+-green)

## Features

- **Root-based discovery**: Add any folder that contains scripts and the hub scans it recursively
- **Folder tree navigation**: Keep the real folder structure instead of flattening everything into one list
- **Quick filters**: Search by name, folder, root, or extension
- **One-click execution**: Launch `.ps1`, `.py`, `.bat`, and `.cmd` scripts
- **Console output**: See stdout and stderr inside the app
- **Pin favorites**: Mark your most-used scripts for quick access

## Installation

### Prerequisites

- Python 3.8 or higher
- PowerShell 5.1+ on Windows, or PowerShell Core if you want `pwsh`

### Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the application:
   ```bash
   python powershell_commander.py
   ```

### Windows Auto-Start

To make Codex Script Hub start with Windows:

1. Run `install_startup.bat`
2. Done! The app will now launch when Windows starts

To remove from startup:
- Run `uninstall_startup.bat`

## Usage

### Categories

- **Files**: File and folder operations (create, delete, zip, convert)
- **Computer**: System monitoring (CPU, RAM, drives, processes)
- **Network**: Network tools (DNS, ping, VPN, WiFi)
- **Audio**: Sound controls (volume, text-to-speech, play audio)
- **Apps**: Application management (open, close, install)
- **Dev**: Development tools (Git operations, build, clean)
- **Utils**: Utilities (weather, news, hash, screenshot)
- **Custom**: Your personal scripts

### Using the Hub

1. Click **Add Root** and choose a folder full of scripts.
2. The app scans that folder recursively and shows anything ending in `.ps1`, `.py`, `.bat`, or `.cmd`.
3. Use the search bar or the extension filters to narrow the list.
4. Click a script, then use **Run**, **Open Folder**, **Open File**, **Copy Path**, or **Pin / Unpin**.

### Configuration

The hub stores roots and favorites in `config/script_hub.json`. You can edit that file later if you want to pre-seed a set of folders.

## Configuration

The main configuration file is `config/script_hub.json`. You can:

- Add/remove roots
- Rename root labels
- Pin favorite scripts
- Adjust the saved window size

## File Structure

```
gui/
├── powershell_commander.py   # Compatibility entrypoint
├── script_hub.py             # PySide6 app
├── requirements.txt          # Python dependencies
├── start_commander.bat       # Windows launcher
├── install_startup.bat       # Add to Windows startup
├── uninstall_startup.bat     # Remove from startup
├── config/
│   └── script_hub.json       # Root/script configuration
└── script_dump/              # Default script folder
```

## Keyboard Shortcuts

- **Enter**: Submit input dialogs
- **Escape**: Cancel input dialogs

## Troubleshooting

### "Python not found"
Install Python from https://python.org and ensure it's added to PATH.

### "PySide6 not found"
Run: `pip install -r requirements.txt`

### Scripts not running
- Ensure PowerShell execution policy allows scripts
- Run: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

## License

CC0 - Public Domain
