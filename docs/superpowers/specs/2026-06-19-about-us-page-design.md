# About Us Page Design — FocusTrace Website

**Date:** 2026-06-19  
**Status:** Approved

## Overview

Add an "About Us" page/section to the FocusTrace website to introduce the two developers behind the app.

## Placement

**Location:** Between "How It Works" section and "Download" section.

**Rationale:** Maintains natural user flow: product features → team → call-to-action (download).

## Layout

- Centered heading: "Meet the Makers"
- Names stacked vertically (not side-by-side)
- Each name in large, bold font (Syne font family)
- Tagline under each name (e.g., "KPMG Intern · PES University CSE")
- 2-3 sentence bio below each name
- Follows existing visual styling: purple accent, cards aesthetic, dark/light mode support

## Content

### Swetha Ranganathan

- **Tagline:** Building the future at KPMG · PES University CSE
- **Bio:** A researcher and builder with publications in quantum security, Swetha brings deep expertise in Quantum Computing, CyberSecurity, and GenAI. When not exploring the frontiers of tech, she's building tools like FocusTrace to help people understand their time.

### Rytham Saini

- **Tagline:** Code for a cause · SRM University CSE
- **Bio:** Passionate about building software that actually matters, Rytham combines her CSE background with a drive to create meaningful solutions. She's the other half of FocusTrace, crafting the features that make time tracking feel effortless.

## Visual Style

- Use existing CSS variables for colors (--purple, --text, --bg-card, etc.)
- Match section styling: .section-label, .section-title classes
- Add dedicated .about section with appropriate padding
- Developer cards with subtle hover effects matching .feature-card
- Ensure responsive layout (stack vertically on mobile)

## Implementation Notes

- Add nav link to About section
- Add footer link to About section
- Match existing animation classes (.reveal) for scroll animations