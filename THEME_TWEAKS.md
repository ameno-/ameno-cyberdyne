# Theme Tweaks Guide

## Tool Background Colors

The `toolSuccessBg`, `toolPendingBg`, and `toolErrorBg` control the backgrounds for agent tool outputs.

### Current Values

```json
{
  "toolPendingBg": "#0a0a12",   // Very dark blue-black
  "toolSuccessBg": "#0a1f0a",   // Dark forest green ← The one you asked about
  "toolErrorBg": "#1f0a12"      // Dark red-black
}
```

### Option 1: Subtle Tint (Recommended)

Instead of strong colored backgrounds, use subtle tints that suggest status without overwhelming:

```json
{
  "toolPendingBg": "#0f0f1a",   // Slight blue tint
  "toolSuccessBg": "#0a1510",   // Very subtle green tint
  "toolErrorBg": "#1a0a0f"      // Subtle red tint
}
```

**Effect:** Status is communicated through subtle hue, but text remains highly readable.

### Option 2: Uniform Dark (Minimal)

All tool backgrounds use the same dark color, rely on borders/icons for status:

```json
{
  "toolPendingBg": "#0f0f17",   // Same as userMessageBg
  "toolSuccessBg": "#0f0f17",   // Same as userMessageBg
  "toolErrorBg": "#0f0f17"      // Same as userMessageBg
}
```

**Effect:** Clean, minimal look. Status shown via border colors and icons only.

### Option 3: Purple Accent (Cyberpunk)

Match your theme's purple accent for a cohesive cyberpunk look:

```json
{
  "toolPendingBg": "#0a0a1f",   // Deep purple-blue
  "toolSuccessBg": "#0f0a1a",   // Deep purple
  "toolErrorBg": "#1f0a15"      // Purple-red
}
```

**Effect:** All tool boxes feel unified with the theme's purple elements.

### Option 4: High Contrast

Maximum separation between states:

```json
{
  "toolPendingBg": "#0a0a12",   // Near black
  "toolSuccessBg": "#1a2e1a",   // Brighter green (but not too bright)
  "toolErrorBg": "#2e1a1a"      // Brighter red
}
```

**Effect:** Clear visual distinction, but may be too colorful for some.

## Quick Test

To try any option, edit your local theme:

```bash
vim ~/.pi/agent/themes/ameno-cyberdyne.json
```

Change the `toolSuccessBg` value, save, and Pi will hot-reload instantly.

## My Recommendation

**Option 1 (Subtle Tint)** works best because:
- ✅ Maintains readability with cyan text
- ✅ Still communicates status through color
- ✅ Doesn't compete with syntax highlighting
- ✅ Professional, polished look

## Related Tokens

Also consider adjusting:

| Token | Purpose |
|-------|---------|
| `toolTitle` | The tool name (e.g., "file.write") |
| `toolOutput` | The actual output text |
| `success` | Success indicators (checkmarks, etc.) |

Current values:
- `toolTitle`: `cyan` ← May clash on green
- `toolOutput`: `""` (default text color)
- `success`: `acid` (bright green)

If you keep the green background, consider changing `toolTitle` to `amber` or `pink` for better contrast.
