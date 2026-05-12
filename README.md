# Terba Consulting Website

A professional, multidisciplinary consulting firm website built with modern web technologies.

## Features

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Modern Aesthetics**: Minimalist design system with custom color palette
- **Multiple Pages**:
  - Home (hero, services overview, metrics)
  - About Us (team leadership, company mission)
  - Services (practice areas, methodology)
  - Contact (consultation request form)
- **Interactive Elements**:
  - Mobile-responsive navigation menu
  - Form validation
  - Smooth scrolling animations
  - Dark mode support
- **Professional Typography**: EB Garamond for headlines, Inter for body text
- **Material Design Icons**: Integrated Material Symbols

## Tech Stack

- **HTML5**: Semantic markup
- **Tailwind CSS**: Utility-first CSS framework (via CDN)
- **JavaScript**: Vanilla JS for interactivity
- **Responsive**: Mobile, tablet, and desktop viewports

## Project Structure

```
terba-consulting/
├── index.html              # Home page
├── about.html             # About Us page
├── services.html          # Services page
├── contact.html           # Contact Us page
├── assets/
│   ├── images/           # Logo and media files
│   │   ├── logo.png     # Main logo (transparent bg)
│   │   └── logo-white.png
│   ├── css/             # Custom CSS (if needed)
│   └── js/
│       └── main.js      # JavaScript functionality
└── README.md
```

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Optional: A local development server (Python, Node.js, or any HTTP server)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/terba-consulting.git
cd terba-consulting
```

2. Open in browser (two options):

**Option A: Direct Open**
```bash
open index.html
```

**Option B: With Local Server (Recommended)**
```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (with http-server)
npx http-server
```

Then navigate to `http://localhost:8000`

## Features Details

### Navigation
- Sticky header with logo and navigation links
- Mobile hamburger menu that toggles on small screens
- Active page indicator in navigation

### Forms
- Contact form with validation
- Email validation
- Required field checking
- Success message on submission

### Responsive Breakpoints
- Mobile: < 768px (md breakpoint)
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Color System
- Primary: #051b12 (Forest Green)
- Secondary: #33666a (Teal)
- Tertiary: #00192a (Navy)
- Neutral grays and surfaces for contrast

## Customization

### Colors
Edit the Tailwind config in `<script id="tailwind-config">` in any HTML file:
```javascript
"primary": "#051b12",    // Change green
"secondary": "#33666a",  // Change teal
```

### Logo
Replace images in `assets/images/`:
- `logo.png` - Main logo (used in light backgrounds)
- `logo-white.png` - Inverted logo (used in dark backgrounds)

### Content
Update text directly in HTML files. All pages use semantic HTML with class names indicating purpose.

### Typography
Font families are imported from Google Fonts:
- **Headlines**: EB Garamond (serif)
- **Body**: Inter (sans-serif)

Change in the `<link>` tags in the HTML head.

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Lightweight: No heavy frameworks, optimized CSS
- Fast load times: CDN-hosted Tailwind
- Optimized images: SVG logos, lightweight PNGs
- No JavaScript dependencies: Vanilla JS only

## Deployment

### GitHub Pages
1. Push to GitHub
2. Enable GitHub Pages in repository settings
3. Select main branch as source
4. Site will be live at `https://yourusername.github.io/terba-consulting`

### Other Hosting
- Netlify: Drag and drop, auto-deploys on git push
- Vercel: Similar to Netlify, optimized for modern web
- Traditional hosting: Upload files via FTP/SSH

## Contributing

1. Create a feature branch (`git checkout -b feature/improvement`)
2. Make your changes
3. Commit with clear messages (`git commit -m 'Add feature'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

## License

This project is proprietary to Terba Consulting. All rights reserved.

## Contact

For inquiries about the website or services:
- Email: advisory@terbaconsulting.com
- Phone: +1 (800) 555-0199
- Location: Pompano Beach, FL 33062

## Maintenance

### Regular Updates
- Update team member information in About Us
- Add case studies or testimonials to Services
- Update contact information as needed
- Monitor form submissions

### Security
- Keep links and CTAs functional
- Validate form submissions server-side (when backend is added)
- Regularly check for broken links

---

Built with ❤️ for Terba Consulting | Last updated: May 2024
