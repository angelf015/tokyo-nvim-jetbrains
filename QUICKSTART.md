# Quick Start Guide

## 🚀 For Users

### Installation
1. Download from JetBrains Marketplace or from releases
2. Install in your IDE: `Settings` → `Plugins` → `Install Plugin from Disk`
3. Restart IDE
4. Activate theme: `Settings` → `Appearance & Behavior` → `Appearance` → Select theme

### Switching Themes
All 4 variants are available in the theme dropdown:
- **Tokyo Night - Nvim Edition** - Darkest variant
- **Tokyo Storm - Nvim Edition** - Medium dark
- **Tokyo Moon - Nvim Edition** - Blue-tinted dark
- **Tokyo Day - Nvim Edition** - Light theme

## 🛠️ For Developers

### First Time Setup
```bash
# Clone the repository
git clone https://github.com/angelf015/tokyo-nvim-jetbrains.git
cd tokyo-nvim-jetbrains

# Verify Gradle works
./gradlew --version

# Build the plugin
./gradlew buildPlugin
```

### Common Tasks

#### Build Plugin
```bash
./gradlew buildPlugin
```
Output: `build/distributions/tokyo-nvim-jetbrains-2.0.0.zip`

#### Run IDE with Plugin (for testing)
```bash
./gradlew runIde
```
This launches a new IDE instance with your plugin installed.

#### Verify Plugin
```bash
./gradlew verifyPlugin
```
Checks plugin structure and compatibility.

#### Clean Build
```bash
./gradlew clean buildPlugin
```

### Making Changes

#### Modifying Colors
1. Edit files in `resources/theme/`:
   - `*.theme.json` - UI colors
   - `*.xml` - Syntax highlighting colors

2. Test changes:
   ```bash
   ./gradlew runIde
   ```

3. Build for distribution:
   ```bash
   ./gradlew buildPlugin
   ```

#### Adding New Syntax Elements
1. Identify the element name (check JetBrains docs)
2. Add to **all 4 XML files** (night, storm, moon, day)
3. Use appropriate colors for each variant
4. Test in multiple languages

### Project Structure
```
tokyo-nvim-jetbrains/
├── resources/
│   ├── META-INF/
│   │   ├── plugin.xml          # Plugin configuration
│   │   └── pluginIcon.svg      # Plugin icon
│   └── theme/
│       ├── tokyo-night.theme.json  # Night UI colors
│       ├── night.xml               # Night syntax colors
│       ├── tokyo-storm.theme.json  # Storm UI colors
│       ├── storm.xml               # Storm syntax colors
│       ├── tokyo-moon.theme.json   # Moon UI colors
│       ├── moon.xml                # Moon syntax colors
│       ├── tokyo-day.theme.json    # Day UI colors
│       └── day.xml                 # Day syntax colors
├── build.gradle.kts            # Gradle build configuration
├── settings.gradle.kts         # Gradle settings
├── gradle.properties           # Build properties
└── gradlew                     # Gradle wrapper script
```

### Debugging

#### Plugin Not Loading
- Check `build/distributions/` for the JAR
- Verify plugin.xml is valid XML
- Check IDE logs: `Help` → `Show Log in Finder/Explorer`

#### Colors Not Showing
- Ensure both `.theme.json` and `.xml` files are present
- Verify color values are valid hex codes
- Check if theme is actually activated in IDE settings

#### Build Failures
```bash
# Clean and rebuild
./gradlew clean
./gradlew buildPlugin

# Check with verbose output
./gradlew buildPlugin --stacktrace
```

### Testing Checklist
Before submitting changes:
- [ ] Build succeeds: `./gradlew buildPlugin`
- [ ] Plugin verifies: `./gradlew verifyPlugin`
- [ ] XML validates: `xmllint --noout resources/theme/*.xml`
- [ ] Tested in IDE: `./gradlew runIde`
- [ ] All 4 themes work
- [ ] Changes consistent across all variants
- [ ] Documentation updated

### Publishing (Maintainers Only)
```bash
# Set environment variables
export PUBLISH_TOKEN=your_token

# Publish to marketplace
./gradlew publishPlugin
```

## 📚 Resources

- [IntelliJ Platform SDK](https://plugins.jetbrains.com/docs/intellij/)
- [Theme Structure](https://plugins.jetbrains.com/docs/intellij/themes.html)
- [Color Schemes](https://plugins.jetbrains.com/docs/intellij/color-scheme-management.html)
- [Gradle IntelliJ Plugin](https://github.com/JetBrains/gradle-intellij-plugin)

## 🆘 Getting Help

- Check [CONTRIBUTING.md](CONTRIBUTING.md)
- Review [existing issues](../../issues)
- Read [documentation](README.md)
- Open a [discussion](../../discussions)

## 🎯 Quick Commands Reference

| Command | Description |
|---------|-------------|
| `./gradlew tasks` | List all available tasks |
| `./gradlew buildPlugin` | Build the plugin JAR |
| `./gradlew runIde` | Run test IDE with plugin |
| `./gradlew verifyPlugin` | Verify plugin structure |
| `./gradlew clean` | Clean build artifacts |
| `./gradlew publishPlugin` | Publish to marketplace |

---

Happy coding! 🌃
