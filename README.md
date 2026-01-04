# Project Gallery

A simple, elegant gallery for showcasing your projects from Lovable, Replit, v0, and other platforms.

## Setup on Render

1. Push this folder to a GitHub repository
2. Go to [render.com](https://render.com) → New → Static Site
3. Connect your GitHub repo
4. Settings:
   - **Name**: your-gallery-name
   - **Branch**: main
   - **Build Command**: (leave blank)
   - **Publish Directory**: `.` or leave blank
5. Click "Create Static Site"

Your gallery will be live at `your-gallery-name.onrender.com`

## Adding Projects

### 1. Take a screenshot
Capture your project at roughly 1600x1000px (16:10 ratio works best). Save it in the `images/` folder.

### 2. Add a card
Open `index.html` and copy this block into the `<main class="gallery">` section:

```html
<article class="card">
    <a href="YOUR_PROJECT_URL" target="_blank" rel="noopener">
        <div class="card-image">
            <img src="images/YOUR_IMAGE.png" alt="Project name screenshot">
        </div>
        <div class="card-content">
            <div class="card-tags">
                <span class="tag">Platform</span>
                <span class="tag">Tech</span>
            </div>
            <h2>Project Name</h2>
            <p>Brief description of what this project does.</p>
        </div>
    </a>
</article>
```

### 3. Commit and push
Render auto-deploys from your main branch within ~60 seconds.

## Customization

### Colors
Edit the CSS variables at the top of `style.css`:

```css
:root {
    --bg-primary: #0f0f0f;      /* Page background */
    --bg-card: #1a1a1a;          /* Card background */
    --text-primary: #f5f0e8;     /* Main text */
    --text-secondary: #a39e93;   /* Muted text */
    --accent: #e8d5b5;           /* Tag text, highlights */
}
```

### Fonts
Replace the Google Fonts link in `index.html` head. Update the `font-family` values in `style.css` to match.

### Header
Edit the `<h1>` and `.subtitle` in `index.html`.

## File Structure

```
gallery/
├── index.html          # Main page (edit to add projects)
├── style.css           # Styles (edit for colors/fonts)
├── README.md           # This file
└── images/
    ├── placeholder.svg # Default placeholder
    ├── project1.png    # Your screenshots
    └── ...
```

## Tips

- Use consistent screenshot sizes for a cleaner grid
- Keep descriptions to 1-2 sentences
- Update the footer date when you add projects
- PNG or WebP format recommended for screenshots
