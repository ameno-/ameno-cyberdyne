# Color Variations for Ameno Cyberdyne

## Problem: Cyan Clash on Non-Black Backgrounds

The current cyan (`#00f5ff`) is very bright and can cause readability issues on Pi's various background surfaces:
- `selectedBg`: `#1a1a2e` (slate purple)
- `toolPendingBg`: `#0a0a12` (near black)
- `toolSuccessBg`: `#0a1f0a` (dark green)
- `toolErrorBg`: `#1f0a12` (dark red)
- `userMessageBg`: `#0f0f17` (void black)

## Proposed Solutions

### Option 1: Deep Teal (Recommended)
Replaces electric cyan with a deeper, more saturated teal that pops without glare.

| Element | Current | Proposed | Background Test |
|---------|---------|----------|-----------------|
| Primary accent | `#00f5ff` | `#00d4aa` | ✅ Readable on all surfaces |
| Keywords | `#00f5ff` | `#00d4aa` | ✅ Softer, professional |
| Border | `#00f5ff` | `#00d4aa` | ✅ Less eye strain |
| Links | `#00f5ff` | `#00d4aa` | ✅ Better contrast ratio |

**Preview:**
```
┌─────────────────────────────────────────┐
│ export function example() {      ← Teal │
│   const value = "test";                 │
│ }                                       │
└─────────────────────────────────────────┘
```

### Option 2: Electric Blue
Shifts from cyan to a vibrant electric blue — maintains energy, improves readability.

| Element | Current | Proposed | Background Test |
|---------|---------|----------|-----------------|
| Primary accent | `#00f5ff` | `#0080ff` | ✅ Strong on dark surfaces |
| Keywords | `#00f5ff` | `#0080ff` | ✅ Classic terminal blue |
| Border | `#00f5ff` | `#0080ff` | ✅ Professional feel |
| Links | `#00f5ff` | `#0080ff` | ✅ Web-standard friendly |

**Preview:**
```
┌─────────────────────────────────────────┐
│ export function example() {      ← Blue │
│   const value = "test";                 │
│ }                                       │
└─────────────────────────────────────────┘
```

### Option 3: Soft Cyan (Desaturated)
Keeps the cyan family but reduces brightness for better harmony.

| Element | Current | Proposed | Background Test |
|---------|---------|----------|-----------------|
| Primary accent | `#00f5ff` | `#4dd0e1` | ✅ Gentle, modern |
| Keywords | `#00f5ff` | `#4dd0e1` | ✅ Material Design feel |
| Border | `#00f5ff` | `#4dd0e1` | ✅ Subtle elegance |
| Links | `#00f5ff` | `#4dd0e1` | ✅ Accessible contrast |

**Preview:**
```
┌─────────────────────────────────────────┐
│ export function example() {  ← Soft Cyan│
│   const value = "test";                 │
│ }                                       │
└─────────────────────────────────────────┘
```

### Option 4: Coral/Pink Shift
Abandons cyan entirely for a warm coral that complements the hot pink.

| Element | Current | Proposed | Background Test |
|---------|---------|----------|-----------------|
| Primary accent | `#00f5ff` | `#ff6b6b` | ✅ Warm, energetic |
| Keywords | `#00f5ff` | `#ff6b6b` | ⚠️ May clash with pink |
| Border | `#00f5ff` | `#ff6b6b` | ✅ Visible on all |
| Links | `#00f5ff` | `#ff6b6b` | ✅ Distinct from magenta |

**Preview:**
```
┌─────────────────────────────────────────┐
│ export function example() {   ← Coral   │
│   const value = "test";                 │
│ }                                       │
└─────────────────────────────────────────┘
```

### Option 5: Goldenrod (Warm Yellow)
Embraces the gold/yellow direction fully — premium, luxurious feel.

| Element | Current | Proposed | Background Test |
|---------|---------|----------|-----------------|
| Primary accent | `#00f5ff` | `#ffd700` | ✅ Rich, metallic |
| Keywords | `#00f5ff` | `#ffd700` | ⚠️ May compete with amber |
| Border | `#00f5ff` | `#ffd700` | ✅ High visibility |
| Links | `#00f5ff` | `#ffd700` | ⚠️ Could feel like warnings |

**Preview:**
```
┌─────────────────────────────────────────┐
│ export function example() {     ← Gold  │
│   const value = "test";                 │
│ }                                       │
└─────────────────────────────────────────┘
```

## Background Compatibility Matrix

| Color | Void Black | Slate Purple | Dark Green | Dark Red | Overall |
|-------|------------|--------------|------------|----------|---------|
| `#00f5ff` (Current) | ⚠️ Harsh | ⚠️ Clash | ⚠️ Clash | ✅ OK | ⚠️ Poor |
| `#00d4aa` (Teal) | ✅ Good | ✅ Good | ✅ Good | ✅ Good | ✅ Best |
| `#0080ff` (Blue) | ✅ Good | ✅ Good | ✅ Good | ✅ Good | ✅ Good |
| `#4dd0e1` (Soft) | ✅ Good | ✅ Good | ✅ Good | ✅ Good | ✅ Good |
| `#ff6b6b` (Coral) | ✅ Good | ✅ Good | ✅ Good | ✅ Good | ⚠️ Warm |
| `#ffd700` (Gold) | ✅ Good | ✅ Good | ✅ Good | ✅ Good | ⚠️ Warm |

## Recommendations

### For Balance: **Deep Teal (`#00d4aa`)**
- Maintains cool temperature
- Reduces eye strain
- Works on ALL backgrounds
- Keeps cyberpunk vibe

### For Vibrancy: **Electric Blue (`#0080ff`)**
- Classic terminal aesthetic
- Maximum compatibility
- Strong brand recognition

### For Subtlety: **Soft Cyan (`#4dd0e1`)**
- Modern, approachable
- Material Design influence
- Easier on eyes for long sessions

## Implementation

To apply any variation, update these fields in `themes/ameno-cyberdyne.json`:

```json
{
  "vars": {
    "cyan": "#00d4aa"  // Change this
  }
}
```

The theme uses variable references, so changing `"cyan"` updates:
- `accent`
- `border`
- `syntaxKeyword`
- `syntaxOperator`
- `thinkingText`
- `mdLinkUrl`
- `customMessageLabel`
- `toolTitle`
- `mdListBullet`
- `thinkingMinimal`
- `thinkingLow`

All at once.
