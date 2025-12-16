# Contributing to Tokyo Night - Nvim Edition

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## 🚀 Getting Started

### Prerequisites

- JDK 17 or higher
- IntelliJ IDEA (recommended) or any JetBrains IDE
- Git

### Setup Development Environment

1. **Fork and Clone**
   ```bash
   git clone https://github.com/angelf015/tokyo-nvim-jetbrains.git
   cd tokyo-nvim-jetbrains
   ```

2. **Open in IntelliJ IDEA**
   - File → Open → Select the project directory
   - IDEA will automatically detect it as a Gradle project

3. **Run the Plugin**
   ```bash
   ./gradlew runIde
   ```
   This will launch a new IDE instance with your plugin loaded.

## 🎨 Theme Development

### File Structure

```
resources/theme/
├── tokyo-night.theme.json    # Theme metadata for Night variant
├── night.xml                 # Color scheme XML for Night variant
├── tokyo-storm.theme.json    # Theme metadata for Storm variant
├── storm.xml                 # Color scheme XML for Storm variant
├── tokyo-moon.theme.json     # Theme metadata for Moon variant
├── moon.xml                  # Color scheme XML for Moon variant
├── tokyo-day.theme.json      # Theme metadata for Day variant
└── day.xml                   # Color scheme XML for Day variant
```

### Making Theme Changes

#### Changing Colors

1. **For UI Elements** - Edit the `.theme.json` files
   ```json
   {
     "colors": {
       "button": "#7aa2f7",
       "border": "#292e42"
     }
   }
   ```

2. **For Syntax Highlighting** - Edit the `.xml` files
   ```xml
   <option name="DEFAULT_KEYWORD">
       <value>
           <option name="FOREGROUND" value="bb9af7"/>
           <option name="FONT_TYPE" value="2"/>
       </value>
   </option>
   ```

#### Font Type Values
- `0` = Normal
- `1` = Bold
- `2` = Italic
- `3` = Bold + Italic

#### Adding New Syntax Elements

When adding a new syntax element with bold styling:

1. Add to **all 4 XML files** for consistency
2. Use appropriate colors for each theme variant
3. Follow existing naming conventions
4. Test in multiple languages

Example:
```xml
<option name="NEW_ELEMENT_NAME">
    <value>
        <option name="FOREGROUND" value="89ddff"/>
        <option name="FONT_TYPE" value="1"/>
    </value>
</option>
```

### Testing Your Changes

1. **Build the plugin**
   ```bash
   ./gradlew buildPlugin
   ```

2. **Run in test IDE**
   ```bash
   ./gradlew runIde
   ```

3. **Verify across languages**
   - Test with Java, Kotlin, Python, JavaScript, etc.
   - Check UI elements (buttons, borders, etc.)
   - Verify indent guides are visible
   - Test in both light and dark OS themes

4. **Validate XML**
   ```bash
   xmllint --noout resources/theme/*.xml
   ```

## 📝 Coding Standards

### XML Files
- Use 4 spaces for indentation
- Keep elements alphabetically sorted where possible
- Include comments for major sections
- Maintain consistent color values across similar elements

### JSON Files
- Use 2 spaces for indentation
- Follow the existing structure
- Keep theme metadata accurate

### Commit Messages
Use conventional commit format:
```
feat: add bold styling for TypeScript decorators
fix: correct indent guide colors in day theme
docs: update README with new screenshots
chore: update Gradle dependencies
```

## 🐛 Reporting Bugs

### Before Submitting

1. Check if the issue already exists
2. Verify you're using the latest version
3. Test in a clean IDE installation if possible

### Bug Report Template

```markdown
**Theme Variant:** Tokyo Night / Storm / Moon / Day
**IDE:** IntelliJ IDEA 2024.1
**OS:** macOS / Windows / Linux

**Description:**
Clear description of the issue

**Steps to Reproduce:**
1. Step one
2. Step two
3. ...

**Expected Behavior:**
What should happen

**Actual Behavior:**
What actually happens

**Screenshots:**
If applicable
```

## 💡 Feature Requests

We welcome feature requests! Please:

1. Check existing issues/PRs first
2. Explain the use case
3. Provide examples if possible
4. Consider the scope (should it apply to all themes?)

## 🔍 Pull Request Process

1. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Follow coding standards
   - Test thoroughly
   - Update documentation if needed

3. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: your descriptive message"
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Open a Pull Request**
   - Use a clear title
   - Describe what changed and why
   - Reference any related issues
   - Include before/after screenshots for visual changes

6. **Wait for review**
   - Address any feedback
   - Keep the PR updated with main branch

## 📋 Checklist for Theme PRs

- [ ] Changes applied to all 4 theme variants consistently
- [ ] XML files validated successfully
- [ ] Tested in at least 2 different languages
- [ ] Indent guides are visible
- [ ] Colors maintain contrast and readability
- [ ] Documentation updated (if applicable)
- [ ] CHANGELOG.md updated (for significant changes)
- [ ] No sensitive information committed

## 🎯 Color Guidelines

When choosing colors:

1. **Maintain consistency** - Similar elements should have similar colors
2. **Ensure contrast** - Text must be readable (WCAG AA minimum)
3. **Stay true to theme** - Colors should match the Tokyo Night aesthetic
4. **Test in context** - Colors look different in actual code vs. isolated

### Color Palette Reference

Stick to these base colors for consistency:

**Dark Themes:**
- Blue: `#7aa2f7`, `#82aaff`, `#89ddff`
- Purple: `#bb9af7`, `#c099ff`
- Green: `#9ece6a`, `#c3e88d`
- Orange: `#ff9e64`, `#ff966c`
- Red: `#f7768e`, `#ff757f`
- Cyan: `#73daca`, `#4fd6be`

**Light Theme (Day):**
- Blue: `#2e7de9`, `#006a83`
- Purple: `#9854f1`
- Green: `#33635c`
- Orange: `#b15c00`
- Red: `#f52a65`
- Cyan: `#387068`

## 🤝 Code of Conduct

- Be respectful and constructive
- Welcome newcomers
- Focus on the issue, not the person
- Accept constructive criticism gracefully

## 📞 Questions?

- Open a [Discussion](../../discussions)
- Check existing [Issues](../../issues)
- Review [Documentation](README.md)

---

Thank you for contributing to Tokyo Night! 🌃
