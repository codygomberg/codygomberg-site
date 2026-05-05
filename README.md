# codygomberg.com

Personal portfolio and blog. Plain HTML, CSS, and vanilla JavaScript — no frameworks, no build tools.

---

## Structure

```
codygomberg-site/
├── index.html        # Home / About page
├── writing.html      # Writing (blog posts)
├── photos.html       # Photo gallery
├── misc.html         # Links, books, music
├── style.css         # All styles
├── photos/           # Photo files
└── README.md
```

---

## Design

- **Theme:** Catppuccin Mocha
- **Font:** JetBrains Mono (Google Fonts)
- **Layout:** Two-column — sidebar (name, nav, social icons) + main content
- **Link color:** `#cba6f7` (mauve)

---

## Hosting & Deployment

- **Host:** Netlify (project: `stalwart-cobbler-19bb5f`)
- **Domain:** codygomberg.com (registered at Squarespace)
- **Deploy:** Drag and drop the `codygomberg-site` folder onto Netlify → Deploys

**To update the site:**
1. Make changes to the files
2. Go to [app.netlify.com](https://app.netlify.com) → your project → Deploys
3. Drag the entire `codygomberg-site` folder into the deploy area

---

## How to Add Content

### New blog post
1. Create a new file: `posts/your-post-title.html`
2. Use the same HTML structure as the other pages (copy the sidebar from any page)
3. Add a link in `writing.html`:
```html
<ul class="writing-list">
  <li>
    <a class="title" href="posts/your-post-title.html">Post Title</a>
    <span class="date">May 2026</span>
  </li>
</ul>
```

### New photo section
1. Drop image files into the `photos/` folder
2. In `photos.html`, add a new section block:
```html
<div class="photo-section">
  <h3 class="photo-section-title">Location — Month Year</h3>
  <div class="photo-grid">
    <div class="photo-item" data-index="N">
      <img src="photos/filename.jpg" alt="Description">
    </div>
  </div>
</div>
```
3. Add the new section **above** older sections — photos are sorted most recent first
4. Make sure `data-index` values are sequential across all sections (0, 1, 2, 3...)

### New link (Misc page)
```html
<li><a href="https://example.com" target="_blank" rel="noopener">Title</a></li>
```

### New book (Misc page)
```html
<li><a href="https://goodreads.com/..." target="_blank" rel="noopener"><em>Book Title</em></a> — Author</li>
```

### New music (Misc page)
```html
<li><a href="https://open.spotify.com/album/..." target="_blank" rel="noopener">Album Title</a> — Artist <span class="meta">Year</span></li>
```

---

## Next Steps

- [ ] Set up GitHub repo and connect to Netlify for automatic deploys
- [ ] Write first blog post
- [ ] Add more photos
