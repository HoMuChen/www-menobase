# Favicon Guide for Meno

The `favicon.svg` file has been created with a white "M" on a slate-900 background.

## Current Files

- ✅ `favicon.svg` - SVG favicon (created)
- ⏳ `favicon.png` - 32x32 PNG (needs generation)
- ⏳ `apple-touch-icon.png` - 180x180 PNG for iOS (needs generation)

## How to Generate PNG Files

### Option 1: Using Online Tool (Easiest)

1. Visit [RealFaviconGenerator](https://realfavicongenerator.net/)
2. Upload `favicon.svg`
3. Download the generated package
4. Extract and place files in the root directory

### Option 2: Using Figma/Sketch/Illustrator

1. Open `favicon.svg` in your design tool
2. Export as PNG with these sizes:
   - `favicon.png` - 32x32px or 64x64px
   - `apple-touch-icon.png` - 180x180px

### Option 3: Using ImageMagick (CLI)

If you have ImageMagick installed:

```bash
# Generate 32x32 favicon
convert -background none -resize 32x32 favicon.svg favicon.png

# Generate 180x180 Apple touch icon
convert -background none -resize 180x180 favicon.svg apple-touch-icon.png
```

### Option 4: Using Node.js Script

Install sharp:
```bash
npm install sharp
```

Create `generate-favicons.js`:
```javascript
const sharp = require('sharp');
const fs = require('fs');

const svg = fs.readFileSync('favicon.svg');

// Generate 32x32 favicon
sharp(svg)
  .resize(32, 32)
  .png()
  .toFile('favicon.png')
  .then(() => console.log('favicon.png created'));

// Generate 180x180 Apple touch icon
sharp(svg)
  .resize(180, 180)
  .png()
  .toFile('apple-touch-icon.png')
  .then(() => console.log('apple-touch-icon.png created'));
```

Run:
```bash
node generate-favicons.js
```

## Customization

To customize the favicon, edit `favicon.svg`:

### Change Background Color
```svg
<rect width="100" height="100" fill="#0f172a" rx="20"/>
```
- Current: `#0f172a` (slate-950)
- Try: `#1e293b` (slate-900), `#334155` (slate-700), or any hex color

### Change Letter Color
```svg
<text ... fill="#ffffff" ...>M</text>
```
- Current: `#ffffff` (white)
- Try: `#e2e8f0` (slate-200), `#cbd5e1` (slate-300)

### Change Border Radius
```svg
<rect ... rx="20"/>
```
- Current: `20` (rounded)
- Try: `0` (square), `50` (circle), `10` (slightly rounded)

### Change Letter
```svg
<text ...>M</text>
```
- Replace `M` with any letter or character

## File Structure

```
/
├── favicon.svg (✅ created)
├── favicon.png (⏳ generate this)
├── apple-touch-icon.png (⏳ generate this)
└── index.html
```

## Browser Support

- **Modern Browsers**: Use `favicon.svg` (Chrome, Firefox, Safari, Edge)
- **Legacy Browsers**: Fallback to `favicon.png`
- **iOS/Safari**: Use `apple-touch-icon.png`

## Testing

After generating PNG files:

1. Open `index.html` in browser
2. Check browser tab for favicon
3. Bookmark the page and verify favicon appears
4. On iOS, add to home screen and verify icon

## Notes

- SVG favicon is scalable and looks sharp on all displays
- PNG fallbacks ensure compatibility with older browsers
- Apple touch icon shows when users add site to iOS home screen
