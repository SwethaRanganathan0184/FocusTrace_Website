# About Us Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add an About Us section to the FocusTrace website between "How It Works" and "Download" sections, showcasing the two developers behind the app.

**Architecture:** Single HTML file modification. Add CSS styles for the new section and insert HTML between existing sections. Add navigation and footer links.

**Tech Stack:** Plain HTML/CSS (no frameworks), existing CSS variables for theming

---

## File Structure

**Files:**
- Modify: `index.html` — add CSS styles, new HTML section, update nav and footer

---

## Global Constraints

- Use existing CSS variables (--purple, --text, --bg-card, --text-muted, etc.)
- Match existing section styling (.section-label, .section-title)
- Use .reveal animation class for scroll animations
- Support dark/light mode using existing CSS variables
- Responsive: stack vertically on mobile (< 768px)

---

### Task 1: Add About Us CSS Styles

**Files:**
- Modify: `index.html:578` — add styles before closing `</style>` tag

**Interfaces:**
- Produces: CSS class `.about` with styles for the new section

- [ ] **Step 1: Add CSS styles for About Us section**

Add this CSS before the `</style>` tag at line 578:

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

- [ ] **Step 2: Commit CSS changes**

```bash
git add index.html
git commit -m "feat: add About Us section CSS styles"
```

---

### Task 2: Add About Us HTML Section

**Files:**
- Modify: `index.html:757` — insert About Us section between "How It Works" and "Download"

**Interfaces:**
- Consumes: CSS from Task 1
- Produces: HTML section with developer bios

- [ ] **Step 1: Add About Us HTML section**

Insert this HTML after the closing `</div>` of "How It Works" section (line 727, after `</div></section>`) and before the Download section (line 730, `<section class="download" id="download">`):

```html
  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="about-content">
      <p class="section-label reveal">Who built this</p>
      <h2 class="section-title reveal" style="margin-bottom: 0;">Meet the Makers</h2>
      <div class="maker reveal">
        <div class="maker-name">Swetha Ranganathan</div>
        <div class="maker-tagline">Building the future at KPMG · PES University CSE</div>
        <p class="maker-bio">A researcher and builder with publications in quantum security, Swetha brings deep expertise in Quantum Computing, CyberSecurity, and GenAI. When not exploring the frontiers of tech, she's building tools like FocusTrace to help people understand their time.</p>
      </div>
      <div class="maker reveal">
        <div class="maker-name">Rytham Saini</div>
        <div class="maker-tagline">Code for a cause · SRM University CSE</div>
        <p class="maker-bio">Passionate about building software that actually matters, Rytham combines her CSE background with a drive to create meaningful solutions. She's the other half of FocusTrace, crafting the features that make time tracking feel effortless.</p>
      </div>
    </div>
  </section>
```

- [ ] **Step 2: Commit HTML changes**

```bash
git add index.html
git commit -m "feat: add About Us section with developer bios"
```

---

### Task 3: Add Nav and Footer Links

**Files:**
- Modify: `index.html:585-592` — add nav link
- Modify: `index.html:762-766` — add footer link

**Interfaces:**
- Produces: Navigation and footer links pointing to #about

- [ ] **Step 1: Add nav link**

Find the nav-links list (around line 585-592) and add a new list item after the "Download" link:

```html
<li><a href="#about">About</a></li>
```

Add it after this line (line 588):
```html
<li><a href="#download">Download</a></li>
```

- [ ] **Step 2: Add footer link**

Find the footer-links list (around line 762-766) and add a new list item before the closing `</ul>`:

```html
<li><a href="#about">About</a></li>
```

Add it after the last link (after line 765):
```html
<li><a href="https://console.groq.com" target="_blank">Get Groq API Key</a></li>
```

- [ ] **Step 3: Commit link changes**

```bash
git add index.html
git commit -m "feat: add About links to nav and footer"
```

---

### Task 4: Verify and Test

**Files:**
- Test: `index.html` — verify in browser

- [ ] **Step 1: Verify file structure**

Open `index.html` in a browser or preview. Check:
- About section appears between "How It Works" and "Download"
- Both developer bios are visible
- Dark/light mode toggle works in the new section
- Nav shows "About" link
- Footer shows "About" link

- [ ] **Step 2: Final commit**

```bash
git add index.html
git commit -m "feat: complete About Us page implementation"
```

---

## Verification Checklist

- [ ] About section displays between "How It Works" and "Download"
- [ ] Both developer names visible with bios
- [ ] Purple accent color applied correctly
- [ ] Dark/light mode works in About section
- [ ] Nav link scrolls to About section
- [ ] Footer link scrolls to About section
- [ ] Responsive: stacks vertically on mobile

---

**Plan complete and saved to `docs/superpowers/plans/2026-06-19-about-us-page-implementation.md`. Two execution options:**

**1. Subagent-Driven (recommended)** - I dispatch a fresh subagent per task, review between tasks, fast iteration

**2. Inline Execution** - Execute tasks in this session using executing-plans, batch execution with checkpoints

**Which approach?**