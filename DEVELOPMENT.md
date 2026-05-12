# Development Guide - Terba Consulting Website

## Local Development Setup

### Quick Start

```bash
cd ~/Desktop/terba-consulting

# Option 1: Python 3 (recommended)
python -m http.server 8000

# Option 2: Python 2
python -m SimpleHTTPServer 8000

# Option 3: Node.js
npx http-server

# Option 4: PHP
php -S localhost:8000
```

Then open: **http://localhost:8000**

## Project Structure

```
terba-consulting/
├── index.html           # Home page
├── about.html          # About Us page  
├── services.html       # Services page
├── contact.html        # Contact Us page
├── assets/
│   ├── images/        # Logos and media
│   │   ├── logo.png
│   │   └── logo-white.png
│   ├── css/           # Custom CSS (if needed)
│   └── js/
│       └── main.js    # JavaScript functionality
├── README.md          # Project documentation
├── DEVELOPMENT.md     # This file
└── GITHUB_SETUP.md    # GitHub setup instructions
```

## Making Changes

### Editing Pages

All pages are HTML with inline Tailwind CSS via CDN. To edit:

1. Open any `.html` file in your editor
2. Find the section you want to modify
3. Edit the content or styling
4. Save and refresh browser (or F5)

### Common Customizations

#### Change Logo
Replace files in `assets/images/`:
```html
<img src="assets/images/logo.png" alt="Terba Consulting Logo" />
```

#### Change Colors
Edit Tailwind config in the `<script id="tailwind-config">` section:
```javascript
"primary": "#051b12",      // Green
"secondary": "#33666a",    // Teal
"tertiary": "#00192a",     // Navy
```

#### Change Fonts
Modify Google Fonts link in `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=..." rel="stylesheet" />
```

#### Add New Section
Copy existing section HTML and modify. Example:
```html
<section class="py-section-padding bg-surface">
  <div class="max-w-container-max mx-auto px-margin-mobile md:px-margin-desktop">
    <!-- Your content here -->
  </div>
</section>
```

## JavaScript Functionality

File: `assets/js/main.js`

### Features:
- **Mobile Menu**: Toggle on small screens
- **Form Validation**: Contact form validation
- **Smooth Scroll**: Anchor link animations
- **Scroll Animations**: Fade-in on scroll

### Adding New Features:

```javascript
// Example: Add click handler
document.getElementById('myButton').addEventListener('click', () => {
  console.log('Button clicked!');
});

// Example: Add to form submission
contactForm.addEventListener('submit', (e) => {
  e.preventDefault();
  // Your code here
});
```

## Tailwind CSS Classes

Common utility classes used:

- **Layout**: `flex`, `grid`, `gap-gutter`
- **Text**: `font-headline-md`, `text-on-surface`, `font-body-md`
- **Colors**: `bg-primary`, `text-secondary`, `border-outline-variant`
- **Spacing**: `px-margin-desktop`, `py-section-padding`, `m-unit`
- **Responsive**: `md:flex-row`, `lg:col-span-6`, `hidden md:block`

Reference: [Tailwind CSS Docs](https://tailwindcss.com/docs)

## Browser DevTools Tips

### Testing Responsive Design
1. Open DevTools (F12)
2. Click device toggle (Ctrl+Shift+M)
3. Select different device sizes
4. Test all breakpoints

### Debugging JavaScript
1. Open Console tab
2. Look for errors in red
3. Use `console.log()` for debugging
4. Set breakpoints in Sources tab

### Inspecting Styles
1. Right-click element → Inspect
2. See all Tailwind classes applied
3. Toggle classes to test changes

## Git Workflow

### Making Changes

```bash
# 1. Make edits to files
# (edit index.html, etc.)

# 2. Check status
git status

# 3. Stage changes
git add .

# 4. Commit with message
git commit -m "Update: Add new feature"

# 5. Push to GitHub
git push
```

### Branch Workflow (Optional)

```bash
# Create feature branch
git checkout -b feature/new-feature

# Make changes and commit
git add .
git commit -m "Add new feature"

# Push branch
git push -u origin feature/new-feature

# Create Pull Request on GitHub
# Review → Merge
```

## Performance Tips

1. **Images**: Use optimized PNGs/SVGs
2. **CSS**: Tailwind is minified via CDN
3. **JavaScript**: Keep vanilla JS lightweight
4. **Fonts**: Only load necessary weights/styles
5. **Caching**: Let browser cache CSS/JS

## Deployment

### GitHub Pages (Free)

```bash
# Already configured in README.md
# Your site: https://[username].github.io/terba-consulting
```

### Custom Domain

1. Buy domain (GoDaddy, Namecheap, etc.)
2. Add CNAME file to repo:
   ```
   terbaconsulting.com
   ```
3. Configure DNS at registrar
4. Update GitHub Pages settings

### Other Hosting

- **Netlify**: Drag & drop deploy
- **Vercel**: Auto-deploy on git push
- **Traditional**: FTP upload files

## Troubleshooting

### Styles not showing
- Clear browser cache (Ctrl+Shift+Del)
- Hard refresh (Ctrl+Shift+R)
- Check if Tailwind CDN is loading

### Forms not working
- Check browser console for errors
- Verify form `id` matches JavaScript
- Test with simple data first

### Mobile menu not toggling
- Check if JavaScript file is loading
- Verify element IDs exist in HTML
- Test in console: `document.getElementById('mobileMenuBtn')`

## Resources

- [Tailwind CSS Docs](https://tailwindcss.com)
- [MDN Web Docs](https://developer.mozilla.org)
- [Material Design Icons](https://fonts.google.com/icons)
- [Google Fonts](https://fonts.google.com)

## Support

For questions about the website:
- Email: advisory@terbaconsulting.com
- Documentation: See README.md

---

Happy coding! 🚀
