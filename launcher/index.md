# Super Battle Golf Mod Launcher

Professional WPF launcher for the Super Battle Golf Mod Loader.

## Features

- 🎮 **One-Click Mod Management** - Install, enable, disable, and remove mods
- 🌐 **Built-in Mod Browser** - Browse and download mods from the official repository
- 🎨 **Dark Golf-Themed UI** - Professional interface matching the game aesthetic
- 🔍 **Auto-Detection** - Automatically finds your game installation
- 📊 **Mod Statistics** - See installed mods, enabled mods, and available updates
- ⚙️ **Settings Management** - Configure mod load order and game paths

## Installation

### Option 1: Installer (Recommended)

Download the latest installer from [Releases](https://github.com/sbgmodloader/launcher/releases).

**Note:** Windows SmartScreen will show a warning (this is normal for unsigned software). Click **"More info"** → **"Run anyway"**.

### Option 2: Portable ZIP

Download the portable ZIP, extract anywhere, and run `SBGModLauncher.exe`.

## Building from Source

### Prerequisites

- .NET 8.0 SDK
- Windows 10/11
- Visual Studio 2022 (optional, but recommended)

### Build Steps

```bash
cd GUILauncher
dotnet restore
dotnet build -c Release
```

Output: `GUILauncher\bin\Release\net8.0-windows\`

### Building Installer

Requires [Inno Setup 6.x](https://jrsoftware.org/isinfo.php)

```bash
cd Installer
iscc setup.iss
```

Output: `Installer\Output\SBGModLoaderSetup.exe`

## Documentation

- [Distribution Guide](DISTRIBUTION_GUIDE.md) - How to distribute unsigned software
- [Main Documentation](https://docs.sbgmodloader.com)

## Repository Structure

```
launcher/
├── GUILauncher/          # WPF application source
│   ├── Views/            # XAML UI files
│   ├── ViewModels/       # MVVM view models
│   ├── Services/         # Mod management services
│   └── Models/           # Data models
├── Installer/            # Inno Setup installer
│   ├── setup.iss         # Installer script
│   └── build-release.ps1 # Portable ZIP builder
└── DISTRIBUTION_GUIDE.md # Distribution best practices
```

## Related Repositories

- [mod-loader](https://github.com/sbgmodloader/mod-loader) - Core C++ mod loader DLL
- [sdk](https://github.com/sbgmodloader/sdk) - SDK for mod creators
- [map-maker](https://github.com/sbgmodloader/map-maker) - Unity Map Maker tool
- [mod-repo](https://github.com/sbgmodloader/mod-repo) - Official mod repository

## License

MIT License - See main [mod-loader](https://github.com/sbgmodloader/mod-loader) repository
