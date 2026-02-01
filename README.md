# 🔮 Ameno Cyberdyne

A high-contrast cyberpunk theme for [Pi](https://github.com/badlogic/pi) — the AI coding agent harness.

Inspired by synthwave aesthetics and neon-drenched code editors, this theme transforms your terminal into a futuristic coding environment with electric cyan, hot pink, acid green, and golden amber.

![Theme Preview](https://raw.githubusercontent.com/ameno-/ameno-cyberdyne/main/preview.png)

## ✨ Features

- **High Contrast**: Vibrant neon colors pop against deep void black
- **Semantic Coloring**: Each syntax element has distinct personality
- **Thinking Level Indicators**: Visual hierarchy from cyan (minimal) → magenta (extreme)
- **Tool State Feedback**: Success glows green, errors pulse magenta
- **Hot Reload Compatible**: Edit the theme and see changes instantly

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| **Electric Cyan** | `#00f5ff` | Keywords, accent, primary actions |
| **Hot Pink** | `#ff2a6d` | Variables, links |
| **Acid Green** | `#39ff14` | Strings, success states |
| **Golden Amber** | `#ffb800` | Functions, warnings |
| **Violet** | `#bd00ff` | Types, numbers |
| **Magenta** | `#ff0080` | Errors, extreme thinking |
| **Void Black** | `#0a0a0f` | Background base |

### 🔄 Variations

Having trouble with the bright cyan on certain backgrounds? Try these alternatives:

| Variant | Primary Color | Best For | File |
|---------|--------------|----------|------|
| **Teal** (`#00d4aa`) | Deep teal | Reduced eye strain, all backgrounds | `ameno-cyberdyne-teal.json` |
| **Blue** (`#0080ff`) | Electric blue | Classic terminal look | `ameno-cyberdyne-blue.json` |
| **Soft** (`#4dd0e1`) | Soft cyan | Modern, subtle elegance | `ameno-cyberdyne-soft.json` |

See [COLOR_VARIATIONS.md](./COLOR_VARIATIONS.md) for detailed comparison and background compatibility matrix.

## 📦 Installation

### Option 1: Global Installation (Recommended)

Install once, use everywhere:

```bash
# Clone the repository
git clone https://github.com/ameno-/ameno-cyberdyne.git

# Copy to Pi's global themes directory
mkdir -p ~/.pi/agent/themes
cp ameno-cyberdyne/themes/ameno-cyberdyne.json ~/.pi/agent/themes/
```

Or use npm:

```bash
npm install -g ameno-cyberdyne
# The theme will be automatically discovered via pi.themes
```

### Option 2: Project-Local Installation

Add to a specific project:

```bash
# Copy to your project's .pi directory
mkdir -p .pi/themes
cp ameno-cyberdyne/themes/ameno-cyberdyne.json .pi/themes/
```

### Option 3: Manual Download

```bash
# Direct download
curl -o ~/.pi/agent/themes/ameno-cyberdyne.json \
  https://raw.githubusercontent.com/ameno-/ameno-cyberdyne/main/themes/ameno-cyberdyne.json
```

## 🚀 Activation

1. In Pi, type `/settings`
2. Change the **Theme** dropdown to `ameno-cyberdyne`
3. The theme applies immediately

Or edit your Pi settings directly:

```json
{
  "theme": "ameno-cyberdyne"
}
```

## 🔧 Customization

The theme supports hot reloading. Edit `~/.pi/agent/themes/ameno-cyberdyne.json` while Pi is running to see changes instantly.

### Customizing Colors

The theme uses CSS variables in the `vars` section:

```json
{
  "vars": {
    "cyan": "#00f5ff",
    "pink": "#ff2a6d",
    "acid": "#39ff14"
  }
}
```

Reference these variables in the `colors` section:

```json
{
  "colors": {
    "accent": "cyan",
    "syntaxKeyword": "pink"
  }
}
```

## 📋 Requirements

- [Pi](https://github.com/badlogic/pi) v0.1.0 or higher
- A terminal with truecolor support (iTerm2, Kitty, WezTerm, Windows Terminal, VS Code)

## 📝 License

MIT © [ameno-](https://github.com/ameno-)

## 🙏 Credits

- Color palette inspired by synthwave themes and cyberpunk aesthetics
- Built for the [Pi coding agent](https://github.com/badlogic/pi) by [Mario Zechner](https://github.com/badlogic)

---

<div align="center">

Made with 💜 and neon lights

</div>
