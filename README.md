# Sam Showalter - Portfolio Website

Professional portfolio website showcasing research, experience, education, and projects in Machine Learning and Computer Science.

## Project Structure

```
SamShowalter.github.io/
├── index.html              # Main single-page application
├── css/
│   ├── bootstrap.min.css   # Bootstrap 5 framework
│   └── styles.css          # Compiled custom styles
├── scss/
│   └── styles.scss         # Source SCSS for custom styles
├── js/
│   ├── scripts.js          # Main application logic (source)
│   ├── scripts.min.js      # Minified version
│   ├── to.top.js           # Scroll-to-top functionality
│   ├── three.r95.min.js    # Three.js 3D library (r95)
│   ├── vanta.birds.min.js  # Vanta.js animated background
│   ├── dat.gui.min.js      # GUI controls for 3D
│   ├── p5.min.js           # Creative coding library
│   ├── gallery.min.js      # Image gallery functionality
│   └── rison.js            # URL parameter encoding
├── images/                 # Images and logos (30MB)
├── docs/                   # PDF documents and CVs (20MB)
└── README.md              # This file
```

## Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Custom styling with SCSS preprocessing
- **Bootstrap 5** - Responsive grid and components
- **jQuery 1.12.4** - DOM manipulation
- **Three.js r95** - 3D graphics for background animation
- **Vanta.js** - Animated background effects
- **Font Awesome Kit** - Icon library
- **Google Fonts (Lato)** - Typography

## Recent Code Quality Improvements

### 1. Dependency Consolidation
- Removed duplicate Font-Awesome loads (3 → 1)
- Removed duplicate Three.js versions (kept r95)
- Removed duplicate Vanta.js files (kept minified)
- Removed duplicate jQuery loads (2 → 1)
- Removed 145KB unminified jQuery file

**Impact**: ~1.2MB reduction in JavaScript payload

### 2. HTML Modernization
- Extracted 60+ inline styles to CSS classes
- Removed all deprecated `align` attributes
- Removed all deprecated `<font>` tags
- Removed deprecated `width`/`height` attributes from images
- Replaced excessive `<br>` tags with proper CSS spacing
- Moved inline `onclick` handlers to event listeners

**Impact**: Cleaner, more maintainable HTML following modern standards

### 3. CSS Architecture
Added new utility classes for consistency:
- `.social-links-table` - Consistent table spacing
- `.figure-center` - Centered figures
- `.text-left/.text-center` - Text alignment
- `.large-text` - Consistent large text sizing
- `.profile-image` - Standardized profile image sizing
- `.company-logo` - Responsive company logos
- `.research-thumbnail` - Consistent research images

### 4. Accessibility Improvements
- Added descriptive `alt` attributes to all images
- Improved semantic HTML structure
- Proper heading hierarchy maintained
- ARIA labels on icon links

### 5. JavaScript Quality
- Fixed variable declarations (`var $this` instead of global `$this`)
- Corrected minification artifacts (`n` → `$`)
- Fixed malformed function syntax
- Added proper event listeners
- Consistent jQuery usage throughout

### 6. File Cleanup
Removed unused files:
- `js/three.r92.min.js` (old Three.js version)
- `js/vanta.birds.js` (unminified duplicate)
- `js/jquery.js` (145KB unminified)

## Development

### CSS Compilation
The project uses SCSS for styles. To compile:
```bash
sass scss/styles.scss css/styles.css
```

### Testing Locally
Serve the site locally:
```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

### Making Changes
1. Edit `scss/styles.scss` for styling changes
2. Edit `js/scripts.js` for functionality changes
3. Compile SCSS to CSS after style changes
4. Test locally before deploying

## Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Considerations
- Total page weight: ~52MB (images: 30MB, PDFs: 20MB)
- Consider implementing lazy loading for images
- Consider WebP format for images
- Consider CDN for large PDF files

## Credits
- Template: [DevPortfolio](https://github.com/RyanFitzgerald/devportfolio-template) by Ryan Fitzgerald
- Icons: Font Awesome
- Fonts: Google Fonts (Lato)
- 3D Animation: Three.js + Vanta.js

## License
© 2025 Samuel Showalter. All rights reserved.
