# Task 1 Brief: Add About Us CSS Styles

**Task:** Add CSS styles for the About Us section to index.html

**Location in plan:** Task 1 of 4

**Files:**
- Modify: `index.html` — add styles before closing `</style>` tag (around line 578)

**Exact CSS to add:**

```css
    /* ── ABOUT ── */
    .about {
      padding: 100px 60px;
      max-width: 900px;
      margin: 0 auto;
      text-align: center;
    }
    .about-content {
      max-width: 700px;
      margin: 0 auto;
    }
    .maker {
      margin-top: 48px;
      padding: 40px;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 20px;
      transition: all 0.3s;
    }
    .maker:first-child { margin-top: 36px; }
    .maker:hover {
      border-color: rgba(91, 71, 224, 0.3);
      box-shadow: 0 8px 32px rgba(91, 71, 224, 0.08);
      transform: translateY(-2px);
    }
    [data-theme="dark"] .maker:hover {
      box-shadow: 0 8px 32px rgba(124, 106, 247, 0.12);
    }
    .maker-name {
      font-family: 'Syne', sans-serif;
      font-size: 1.6rem;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 4px;
    }
    .maker-tagline {
      font-size: 0.85rem;
      color: var(--purple);
      margin-bottom: 16px;
      font-weight: 500;
    }
    .maker-bio {
      font-size: 0.92rem;
      color: var(--text-muted);
      line-height: 1.7;
      max-width: 560px;
      margin: 0 auto;
    }
```

**Requirements:**
- Use existing CSS variables (--purple, --text, --bg-card, --text-muted, --border)
- Add styles before the closing `</style>` tag
- Include responsive styles for mobile (under 768px)
- Use same visual style as existing sections (purple accent, cards, dark/light mode)

**Report to:** `.superpowers/sdd/task-1-report.md`
**Commit message:** `feat: add About Us section CSS styles`