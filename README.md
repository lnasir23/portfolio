# Laiba Nasir's Personal Portfolio

A multi-page personal portfolio site built for CS313: Web Engineering, Lab 3
(HTML Advanced - Personal Portfolio II).

## Pages
- `index.html` - Home / introduction
- `hobbies.html` - Hobbies
- `skills.html` - Personal skills
- `gallery.html` - Image gallery
- `contact.html` - Contact details

## Structure
```
Laiba-portfolio/
├── index.html
├── hobbies.html
├── contact.html
├── gallery.html
├── skills.html
├── css/
│   └── style.css
├── images/
│   ├── bg-hearts.jpg
│   ├── image-1.jpeg
│   ├── image-2.jpeg
│   ├── image-3.jpeg
│   ├── image-4.jpeg
│   └── image-5.jpeg
└── README.md
```

## Implementation notes
- All styling lives in a single external stylesheet, `css/style.css`,
  linked from every page (no inline `<style>` blocks, no JavaScript, no
  CSS frameworks).
- **Float + clear layouts:**
  - The nav menu is a horizontal row of floated `<a>` links (previously
    `display:flex`); `nav` carries a `.clearfix` class so it doesn't
    collapse to zero height around its floated children.
  - The image gallery arranges its figures with `float: left` (two per
    row) instead of CSS Grid; `.gallery-grid` also uses `.clearfix`.
  - On the Hobbies page, a photo floats beside the hobby list, with
    `.clearfix` on the panel so the card's border wraps the floated image
    correctly instead of collapsing around it.
- `.clearfix::after { content: ""; display: table; clear: both; }` is the
  one reusable clearfix rule used everywhere floats need containing.

## Live site
- GitHub repository: https://github.com/lnasir23/portfolio
- GitHub Pages: https://lnasir23.github.io/portfolio/ (Index/Home) · 
