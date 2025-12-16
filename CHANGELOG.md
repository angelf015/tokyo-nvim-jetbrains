# Changelog

All notable changes to the Tokyo Night - Nvim Edition theme for JetBrains IDEs will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2024-12-14

### Added
- **Complete theme collection** with 4 beautiful variants:
  - Tokyo Night (darkest variant with `#1a1b26` background)
  - Tokyo Storm (medium dark with `#24283b` background)
  - Tokyo Moon (blue-tinted dark with `#222436` background)
  - Tokyo Day (light theme with `#e1e2e7` background)
- **Bold typography** for enhanced code readability:
  - Interface names and attributes
  - JavaDoc/KDoc comment tag values
  - Enum constants across multiple languages
  - Type aliases in TypeScript and JavaScript
  - Markdown headers (H1, H2, H3)
  - Package constants in Go
  - Global variables in Ruby
  - Gherkin/Cucumber table cells and parameters
- **Multi-language support** with bold styling for:
  - Kotlin (enums, traits, smart constants)
  - Dart (enum constants)
  - PHP (interfaces, constants)
  - Go (exported interfaces, constants)
  - JavaScript/TypeScript (interfaces, type aliases)
  - Bash/Shell (shebangs, here-docs)
  - Ruby (global variables)
- **Visible indent guides** with properly contrasted colors
- Complete syntax highlighting for 20+ programming languages
- Enhanced UI components (dialogs, panels, tool windows)
- Git/VCS integration with clear diff colors
- Debugger support with distinct breakpoint colors

### Fixed
- **Indent guides visibility** - Changed from background color to visible subtle tones:
  - Night: `#292e42` (was `#1a1b26`)
  - Storm: `#292e42` (was `#24283b`)
  - Moon: `#2f334d` (was `#222436`)
  - Day: `#c4c8da` (was `#e1e2e7`)
- Color accuracy to match original tokyonight.nvim theme

### Changed
- Plugin version bumped to 2.0.0 for major feature release
- Improved theme descriptions and metadata
- Updated plugin configuration for JetBrains 2023.3+
- Merged bold typography directly into main themes (removed separate bold variants)

### Technical Details
- Theme files expanded from ~398 to ~567 lines each
- Added 27 bold elements (`FONT_TYPE="1"`) per theme
- All XML theme files validated successfully
- Gradle build system configured with IntelliJ Platform Plugin 1.17.2
- Compatible with IDE builds 233+ (no upper limit)

## [1.0.0] - Initial Release (Previous)

### Added
- Initial Tokyo Night theme port for JetBrains IDEs
- Basic syntax highlighting
- Dark theme support

---

## Future Considerations

### Possible Future Enhancements
- [ ] Additional language-specific optimizations
- [ ] Custom scope colors for advanced search/replace
- [ ] Enhanced console/terminal colors
- [ ] Theme-specific UI icons (optional)
- [ ] Editor scheme export/import functionality
- [ ] Community-requested color adjustments

### Feedback Welcome
Have suggestions or found issues? Please [open an issue](../../issues) on GitHub!

---

**Thank you for using Tokyo Night!** 🌃
