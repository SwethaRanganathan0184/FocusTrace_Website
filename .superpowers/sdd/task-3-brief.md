# Task 3 Brief: Add Nav and Footer Links

**Task:** Add "About" links to the navigation bar and footer

**Location in plan:** Task 3 of 4

**Files:**
- Modify: `index.html` — add nav link in header nav-links list
- Modify: `index.html` — add footer link in footer-links list

**Changes:**

**1. Nav link:**
- Add after the "Download" link (line 588): `<li><a href="#about">About</a></li>`
- Location: in the `<ul class="nav-links">` list

**2. Footer link:**
- Add after the last link (after line 765): `<li><a href="#about">About</a></li>`
- Location: in the `<ul class="footer-links">` list

**Requirements:**
- Both links point to `#about` (anchor to the new section)
- Use same styling as existing nav/footer links

**Report to:** `.superpowers/sdd/task-3-report.md`
**Commit message:** `feat: add About links to nav and footer`