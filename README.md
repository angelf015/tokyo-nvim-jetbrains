# Tokyo Night - Nvim Edition

A clean, dark and light theme suite for JetBrains IDEs, faithfully ported from [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim).

## 🎨 Themes

This plugin includes **4 beautiful variants**:

### 🌙 Tokyo Night (Darkest)
The original, darkest variant with deep blues and vibrant syntax colors.
- **Background:** `#1a1b26`
- **Best for:** Night coding sessions, reduced eye strain

### ⛈️ Tokyo Storm (Medium Dark)  
A medium-dark variant with slightly lighter background.
- **Background:** `#24283b`
- **Best for:** Balanced contrast, all-day coding

### 🌕 Tokyo Moon (Blue-tinted)
A unique blue-tinted dark theme with a distinctive atmosphere.
- **Background:** `#222436`
- **Best for:** Those who prefer cooler color temperatures

### ☀️ Tokyo Day (Light)
A light theme for daytime coding with excellent readability.
- **Background:** `#e1e2e7`
- **Best for:** Bright environments, daytime work

## ✨ Features

- 🎯 **Authentic Colors** - Faithful port of the original tokyonight.nvim color palette
- 🔤 **Enhanced Typography** - Bold styling for interfaces, enums, constants, and types
- 📦 **Multi-Language Support** - Optimized syntax highlighting for:
  - Java, Kotlin, Scala, Groovy
  - JavaScript, TypeScript
  - Python, Ruby, PHP
  - Go, Rust, Dart
  - HTML, CSS, JSON, YAML, XML
  - Markdown, Bash, SQL
  - And many more...
- 🎨 **Complete UI Integration** - Editor, tool windows, panels, dialogs
- 🔍 **Visual Indent Guides** - Subtle but visible indentation lines
- 📊 **Git/VCS Integration** - Clear diff colors and change markers
- 🐛 **Debugger Support** - Distinct breakpoint and execution colors

## 📦 Installation

### From JetBrains Marketplace (Recommended)

1. Open your JetBrains IDE (IntelliJ IDEA, PyCharm, WebStorm, etc.)
2. Go to `Settings/Preferences` → `Plugins` → `Marketplace`
3. Search for **"Tokyo Night - Nvim Edition"**
4. Click `Install`
5. Restart your IDE
6. Go to `Settings/Preferences` → `Appearance & Behavior` → `Appearance`
7. Select your preferred theme from the **Theme** dropdown

### Manual Installation

1. Download the latest release from the [Releases](../../releases) page
2. Open your IDE
3. Go to `Settings/Preferences` → `Plugins` → ⚙️ → `Install Plugin from Disk...`
4. Select the downloaded `.jar` file
5. Restart your IDE
6. Activate the theme in `Settings/Preferences` → `Appearance & Behavior` → `Appearance`

### From Source

```bash
git clone https://github.com/angelf015/tokyo-nvim-jetbrains.git
cd tokyo-nvim-jetbrains
./gradlew buildPlugin
```

The plugin will be built in `build/distributions/`.

## 🛠️ Build Commands

```bash
# Build the plugin
./gradlew buildPlugin

# Run IDE with the plugin for testing
./gradlew runIde

# Verify plugin
./gradlew verifyPlugin

# Run tests
./gradlew test
```

## 🎯 Supported IDEs

All JetBrains IDEs version **2023.3+**:

- IntelliJ IDEA (Community & Ultimate)
- PyCharm (Community & Professional)
- WebStorm
- PhpStorm
- RubyMine
- GoLand
- CLion
- Rider
- Android Studio
- DataGrip
- AppCode

## 🎨 Color Palette Reference

### Tokyo Night (Dark Variants)
```
Background:  #1a1b26 (Night) / #24283b (Storm) / #222436 (Moon)
Foreground:  #c0caf5 (Night/Storm) / #c8d3f5 (Moon)
Comment:     #565f89 (Night/Storm) / #636da6 (Moon)
Functions:   #7aa2f7 (Night/Storm) / #82aaff (Moon)
Keywords:    #bb9af7 (Night/Storm) / #c099ff (Moon)
Strings:     #9ece6a (Night/Storm) / #c3e88d (Moon)
Numbers:     #ff9e64 (Night/Storm) / #ff966c (Moon)
Classes:     #89ddff
```

### Tokyo Day (Light Variant)
```
Background:  #e1e2e7
Foreground:  #3760bf
Comment:     #9699a3
Functions:   #2e7de9
Keywords:    #9854f1
Strings:     #33635c
Numbers:     #b15c00
Classes:     #006a83
```

## 💡 Typography Features

The theme includes **bold styling** for better code readability:

- **Interfaces** - Easily distinguish interfaces from classes
- **Type Aliases** - Clear identification in TypeScript/Kotlin
- **Enum Constants** - Stand out from regular variables
- **Doc Comment Tags** - JavaDoc/KDoc parameters are bold
- **Markdown Headers** - H1, H2, H3 headers in bold
- **Constants** - Package and global constants
- **Smart Highlighting** - Language-specific optimizations

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development Setup

1. Clone the repository
2. Open in IntelliJ IDEA
3. The project uses Gradle with the IntelliJ Platform Plugin
4. Run `./gradlew runIde` to test your changes
5. Make your changes in `/resources/theme/` directory
6. Test in different IDEs if possible

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

## 🙏 Credits

- Original theme: [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim) by Folke Lemaitre
- Inspired by the Tokyo cityscape at night
- Color palette based on the original Tokyo Night theme

## 🔗 Links

- [Original Neovim Theme](https://github.com/folke/tokyonight.nvim)
- [JetBrains Plugin Documentation](https://plugins.jetbrains.com/docs/intellij/)
- [Report Issues](../../issues)
- [Changelog](CHANGELOG.md)

## 📸 Screenshots

> **Note:** Add screenshots of each theme variant here after building

## ⭐ Show Your Support

If you like this theme, please consider:
- ⭐ Starring this repository
- 🐛 Reporting issues and bugs
- 💡 Suggesting new features
- 🔄 Sharing with others

---

**Enjoy coding with Tokyo Night!** 🌃
