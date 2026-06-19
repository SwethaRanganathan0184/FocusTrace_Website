# Task 2 Brief: Add About Us HTML Section

**Task:** Insert About Us section HTML between "How It Works" and "Download" sections

**Location in plan:** Task 2 of 4

**Files:**
- Modify: `index.html` — insert HTML after "How It Works" section, before "Download" section

**Exact HTML to add:**

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

**Requirements:**
- Insert AFTER the "How It Works" section (which ends with `</section>` around line 727)
- Insert BEFORE the "Download" section (which starts with `<section class="download" id="download">` around line 730)
- Use `.reveal` animation class for scroll animations
- Include `id="about"` for anchor linking

**Report to:** `.superpowers/sdd/task-2-report.md`
**Commit message:** `feat: add About Us section with developer bios`