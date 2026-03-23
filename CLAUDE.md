# Keel AI Landing — Project Instructions

## Blog Post Index Rule

Every time a new blog post HTML file is created in `blog/`:

1. **Add it to `blog/index.html`** — Insert a new post card at the TOP of `.posts-grid` (newest first).
   - Move the `featured` class from the previous top card to the new one.
   - Use `<!-- POST:START slug -->` and `<!-- POST:END slug -->` comment markers around each card.
   - Fill in: badge category, date, read time, title, excerpt (from `<meta name="description">`), and href.

2. **Card template:**
```html
<!-- POST:START {slug} -->
<a href="{slug}.html" class="post-card featured fade-in">
  <div class="post-card-body">
    <div class="post-card-meta">
      <span class="post-card-badge">{CATEGORY}</span>
      <span class="post-card-date">{Month DD, YYYY}</span>
      <span class="post-card-read">{N} min read</span>
    </div>
    <h2 class="post-card-title">{Title}</h2>
    <p class="post-card-excerpt">{Description from meta tag}</p>
    <div class="post-card-cta">
      Read article
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><polyline points="12 5 19 12 12 19"/></svg>
    </div>
  </div>
</a>
<!-- POST:END {slug} -->
```

3. **Only the first card** (newest post) gets the `featured` class. All others use `post-card fade-in`.

## Design System

All pages use the same design tokens, dot-grid background, glow overlays, fade-in animations,
nav, CTA section, and footer as the main `index.html`. Refer to existing blog posts for the
article page template.
