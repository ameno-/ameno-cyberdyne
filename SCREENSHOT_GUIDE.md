# 📸 Theme Screenshot Guide

Pi has been opened in a new Terminal window. Here's how to capture the different rendering styles:

## Quick Capture Script

Run this in a separate terminal:

```bash
/tmp/capture-themes.sh
```

This interactive script will guide you through capturing each theme.

## Manual Screenshot Process

### 1. Open Pi Settings
In the Pi terminal:
```
/settings
```

### 2. Switch to Each Theme

#### Theme 1: `ameno-cyberdyne` (Original)
- **Primary:** Electric Cyan `#00f5ff`
- **Look for:** Bright cyan keywords, hot pink variables, acid green strings
- **What to capture:** 
  - Settings panel showing theme dropdown
  - A code block with syntax highlighting
  - A tool success message (green bg, amber title)
  - A diff view (dark green added, dark red removed)

#### Theme 2: `ameno-cyberdyne-teal`
- **Primary:** Deep Teal `#00d4aa`
- **Look for:** Softer teal keywords, easier on the eyes
- **What to capture:**
  - Same views as above, note the reduced eye strain
  - Selected line background (`#1a1a2e`)

#### Theme 3: `ameno-cyberdyne-blue`
- **Primary:** Electric Blue `#0080ff`
- **Look for:** Classic terminal blue feel
- **What to capture:**
  - Syntax highlighting with blue keywords
  - Thinking level indicators

#### Theme 4: `ameno-cyberdyne-soft`
- **Primary:** Soft Cyan `#4dd0e1`
- **Look for:** Modern, Material Design aesthetic
- **What to capture:**
  - Subtle elegance, softer contrasts

### 3. Key UI Elements to Capture

| Element | Where to Find | What to Show |
|---------|---------------|--------------|
| **Syntax Highlighting** | Any code block | Keywords, strings, functions, variables |
| **Tool Success** | After file edit | Green-tinted background, amber title |
| **Tool Error** | Failed command | Red-tinted background |
| **Diff View** | File changes | Dark green (added), dark red (removed) |
| **Settings Panel** | `/settings` | Theme dropdown, selected theme |
| **Thinking Block** | Long responses | Cyan border, minimal thinking state |
| **User Message** | Your inputs | Void black background `#0f0f17` |
| **Selected Line** | Navigation | Slate purple background `#1a1a2e` |

### 4. Screenshot Shortcuts (macOS)

- **Cmd + Shift + 3**: Full screen
- **Cmd + Shift + 4**: Select area
- **Cmd + Shift + 4 + Space**: Click window to capture
- **Cmd + Shift + 5**: Screen recording + options

### 5. Comparison Layout

Suggested side-by-side comparison:

```
┌─────────────────────┬─────────────────────┐
│  Original (Cyan)    │  Teal Variant       │
│  [Screenshot]       │  [Screenshot]       │
│  Bright, electric   │  Balanced, readable │
├─────────────────────┼─────────────────────┤
│  Blue Variant       │  Soft Variant       │
│  [Screenshot]       │  [Screenshot]       │
│  Classic terminal   │  Modern, subtle     │
└─────────────────────┴─────────────────────┘
```

## Demo Content for Screenshots

To see all colors in action, ask Pi:

```
Create a simple React component with:
- A useState hook
- A useEffect that fetches data
- Error handling
- Styled with Tailwind
```

This will generate:
- Keywords (cyan/teal/blue)
- Functions (amber)
- Strings (acid green)
- Variables (pink)
- Types (purple)
- Tool outputs (various backgrounds)

## Saving Screenshots

Screenshots will be saved to:
- Manual: `~/Desktop/`
- Script: `~/Desktop/pi-theme-screenshots/`

## Tips

1. **Clean Terminal**: Clear scrollback (Cmd + K) before screenshots
2. **Window Size**: Resize to ~800x600 for consistent captures
3. **Font Size**: Ensure text is readable (Cmd + +/- to adjust)
4. **Multiple Angles**: Capture both light-on-dark and the various tool states
