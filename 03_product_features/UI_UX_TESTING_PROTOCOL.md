# UI/UX Testing Protocol

## Overview

This document outlines the testing protocol for the Lawyers Hub UI/UX
components, ensuring consistency, accessibility, and performance across the
application.

## 1. Automated Visual Regression Testing

**Goal:** Detect unintended visual changes in UI components. **Tools:**
Playwright / Storybook Test

- **Scope:**
  - Core components (Buttons, Cards, Inputs).
  - Layout structures (Sidebar, Headers).
  - Motion states (Hover, Focus, Active).

**Procedure:**

1. Run `npm run test:visual` to capture screenshots of critical pages.
2. Compare against baseline snapshots.
3. Review and approve intentional changes.

## 2. Manual Interaction Testing Checklist

**Goal:** Verify the "feel" and logic of interactions.

**Navigation:**

- [ ] Page transitions occur smoothly (fade/slide).
- [ ] Browser back/forward buttons handle transitions correctly.
- [ ] Active states in Sidebar/Navbar reflect current route.

**Micro-interactions:**

- [ ] Buttons scale/highlight on hover.
- [ ] Lists stagger in on load.
- [ ] Modals animate in/out (opacity + scale).
- [ ] Toast notifications appear/disappear smoothly.

**Forms:**

- [ ] Input fields focus states are visible.
- [ ] Validation errors appear with animation (shake/fade).
- [ ] Submit buttons show loading state (spinner/pulse).

## 3. Accessibility Testing

**Goal:** Ensure WCAG 2.1 AA compliance.

**Automated:**

- [ ] Run Lighthouse Accessibility audit (Target: 100).
- [ ] Run `axe-core` checks in CI/CD.

**Manual:**

- [ ] **Keyboard Navigation:** Tab through all interactive elements. Ensure
      focus indicators are visible.
- [ ] **Screen Reader:** Verify ARIA labels on icon-only buttons.
- [ ] **Reduced Motion:** Enable "Reduce Motion" in OS settings. Verify that:
  - Page transitions become simple fades or instant.
  - Parallax/scaling effects are disabled.

## 4. Performance Testing

**Goal:** Maintain high responsiveness. **Metrics (Lighthouse Mobile):**

- **LCP (Largest Contentful Paint):** < 2.5s
- **FID (First Input Delay):** < 100ms (or INP < 200ms)
- **CLS (Cumulative Layout Shift):** < 0.1

**Motion Impact:**

- Monitor `requestAnimationFrame` usage.
- Ensure animations use `transform` and `opacity` only (avoid `width`, `height`,
  `top`, `left`).

## 5. Motion Component Verification

**Specific Checks for Framer Motion:**

- **AnimatePresence:** Verify exit animations play fully before component
  unmounts.
- **Layout Animations:** Check for layout thrashing when lists reorder.
- **Memory Leaks:** Monitor heap usage during repeated page navigations.
