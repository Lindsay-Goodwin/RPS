# Academic Website

Personal academic website with collapsible sections, photo carousel, and responsive design.

## Structure

### Core Files
- **`index.html`** - Main HTML file
- **`style.css`** - Primary stylesheet
- **`aurora.css`** - Alternative aurora theme
- **`script.js`** - JavaScript functionality
- **`flickity.css`** & **`flickity.pkgd.min.js`** - Carousel functionality

### Directories
- **`assets/`** - Images and media files
- **`isr-workshop-report/`** - Workshop content page
- **`isr-world-day/`** - World Day content page

## How to Modify

### Content Updates
- **Personal Info**: Edit header and contact sections in `index.html`
- **Photo Carousel**: Add new `<div class="carousel-cell">` blocks with images
- **Sections**: Use `<details>` elements for collapsible content
- **Team Members**: Update research team information in the Research section

### Styling
- **Colors**: Edit CSS custom properties in `:root` selector
- **Theme Switch**: Change stylesheet link from `style.css` to `aurora.css`
- **Layout**: Modify CSS classes for positioning and spacing

### Adding New Sections
```html
<details id="NEW-SECTION">
  <summary class="collapsible">Section Title</summary>
  <div class="content">
    <div class="LINKS-CONTENT">
      <!-- Your content here -->
    </div>
  </div>
</details>
```

### Images
- Place all images in `assets/` directory
- Add version parameters: `?v=timestamp` for cache busting
- Use consistent aspect ratios for carousel images

## Git Workflow

### Basic Commands
```bash
# Pull latest changes
git pull

# Stage changes (to add new files)
git add .

# Commit all changes with message
git commit -am "Update content"

# Push to deploy
git push
```

### Important Notes
- **Automatic Deployment**: Website updates automatically after pushing to main
- **No Manual Deployment**: Changes appear within minutes of pushing
- **Always Pull First**: Get latest changes before making modifications

### Common Issues
- **Images not loading**: Check file paths in `assets/` folder
- **Styling not applying**: Verify CSS file links and syntax
- **Carousel not working**: Ensure Flickity JavaScript is loaded
- **Mobile issues**: Test responsive design and adjust CSS

### Git Issues
```bash
# Undo last commit (before pushing)
git reset --soft HEAD~1

# Undo file changes
git checkout -- filename.html

# Check status
git status
git log --oneline
```