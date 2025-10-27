# Screenshots Folder

Place your Meno app screenshots here.

## Required Screenshots

Replace the placeholder images with your actual app screenshots:

1. **screenshot-transcription.png** - AI transcription and summary interface
   - Recommended size: 1200x800px or similar aspect ratio
   - Shows: Meeting transcription, AI summary, audio player

2. **screenshot-customers.png** - Customer profile and meeting history
   - Recommended size: 1200x800px or similar aspect ratio
   - Shows: Customer profiles, meeting assignments, interaction history

3. **screenshot-tasks.png** - Smart action tracking and todo management
   - Recommended size: 1200x800px or similar aspect ratio
   - Shows: Task list, action items, what/who/when details

## Image Guidelines

### Format
- **Format**: PNG or JPG
- **Quality**: High resolution for retina displays
- **Aspect Ratio**: 3:2 or 4:3 works best
- **File Size**: Optimize to <500KB per image for fast loading

### Content Tips
- Use clean, uncluttered screenshots
- Show real (or realistic) data, not lorem ipsum
- Highlight key features in each screenshot
- Ensure text is readable at smaller sizes
- Consider adding subtle device frames for polish

### Optimization
After adding your screenshots, optimize them:

```bash
# Using ImageOptim (macOS)
# Drag and drop images into ImageOptim app

# Using online tools
# TinyPNG: https://tinypng.com
# Squoosh: https://squoosh.app

# Using CLI tools
# Install: npm install -g sharp-cli
sharp -i screenshot-transcription.png -o screenshot-transcription.png resize 1200
```

## Alternative: Use Placeholder Service

If you don't have screenshots yet, you can temporarily use placeholder images:

```html
<!-- Temporary placeholder example -->
<img src="https://via.placeholder.com/1200x800/1e293b/ffffff?text=Transcription+Interface"
     alt="Meno AI transcription interface">
```

## Current Status

- [ ] screenshot-transcription.png - Add your transcription interface screenshot
- [ ] screenshot-customers.png - Add your customer management screenshot
- [ ] screenshot-tasks.png - Add your action tracking screenshot

Once added, your screenshots will automatically appear in the "See Meno in Action" section of the landing page.
