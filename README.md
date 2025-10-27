# Meno Landing Page

A modern, SEO-optimized static landing page for Meno - Turn Meetings into Meaning.

## Features

- **SEO Optimized**: Complete meta tags, Open Graph, Twitter Cards, JSON-LD schema markup
- **Responsive Design**: Mobile-first design using Tailwind CSS
- **Performance**: Static HTML with minimal dependencies
- **Accessibility**: Semantic HTML and ARIA labels
- **Modern UI**: Clean slate theme (black, white, grey) with smooth animations

## Technology Stack

- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript (mobile menu)
- Unsplash images (placeholder)

## Quick Start

### Option 1: Open Directly
Simply open `index.html` in your browser.

### Option 2: Local Server
For testing with a local server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js (install http-server globally first)
npx http-server -p 8000

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

## Deployment

### Deploy to Netlify
1. Create a Netlify account
2. Drag and drop the project folder
3. Set custom domain to `menobase.app`

### Deploy to Vercel
```bash
npm i -g vercel
vercel
```

### Deploy to GitHub Pages
1. Create GitHub repository
2. Push code
3. Enable GitHub Pages in settings
4. Set custom domain to `menobase.app`

## Customization

### Update Images
Replace Unsplash URLs in `index.html` with your own images:
- Hero image: Line 101
- Benefits section image: Line 250

### Update Colors
Modify Tailwind config in `<head>` section (lines 46-56) or use Tailwind's built-in slate colors.

### Add Favicon
Place your favicon files in the root directory:
- `favicon.svg` (recommended)
- `favicon.ico` (fallback)
- `apple-touch-icon.png` (for iOS)

### SEO Configuration
Update these files for production:
1. **Meta tags** (lines 8-30): Update title, description, keywords
2. **Open Graph images** (lines 19-20): Add actual OG image URLs
3. **Canonical URL** (line 28): Set to `https://menobase.app`
4. **JSON-LD Schema** (lines 54-66): Update as needed

## SEO Checklist

- [x] Title tag with keywords
- [x] Meta description
- [x] Open Graph tags for social sharing
- [x] Twitter Card tags
- [x] Canonical URL
- [x] JSON-LD structured data
- [x] Semantic HTML structure
- [x] Alt text for images
- [x] Mobile-responsive design
- [x] Fast loading time
- [ ] Add `robots.txt` file
- [ ] Add `sitemap.xml` file
- [ ] Set up Google Analytics
- [ ] Submit to Google Search Console

## Files to Add

### robots.txt
Create `robots.txt` in root:
```
User-agent: *
Allow: /
Sitemap: https://menobase.app/sitemap.xml
```

### sitemap.xml
Create `sitemap.xml` in root:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://menobase.app/</loc>
    <lastmod>2024-10-27</lastmod>
    <priority>1.0</priority>
  </url>
</urlset>
```

## Performance Optimization

The landing page is optimized for performance:
- Static HTML (no build step)
- Tailwind CSS via CDN (3.x)
- Lazy loading for images
- Minimal JavaScript
- CSS animations (GPU accelerated)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

All rights reserved - Meno 2024

## Contact

For questions or support, visit [menobase.app](https://menobase.app)
