# CSSor

A guide to maintainable UI architecture and user experience design patterns. Focus on clarity, consistency, and avoiding complex nesting or poor interaction patterns.

---

## 🧩 Component Nesting & Structure

- **Avoid dialogs inside dialogs:** Nested modals confuse focus management and users.
- **Avoid panels inside panels:** Reduces clarity and increases cognitive load.
- **Avoid accordions inside accordions:** Nested toggles make content harder to navigate.
- **Avoid tabs inside tabs:** Deeply nested tab structures are hard to understand and maintain.
- **Avoid carousels inside carousels:** Users lose orientation quickly.
- **Avoid scrollable containers inside other scrollable containers:** This often leads to confusing or broken scrolling behavior.
- **Avoid sticky elements inside another sticky container:** Overlapping behavior is unpredictable across browsers.
- **Avoid tooltips inside tooltips:** Confusing, obscures information.
- **Avoid dropdowns inside dropdowns (unless explicitly for multi-level navigation):** Can lead to complex, unwieldy menus.
- **Avoid double scrollbars unless absolutely necessary for a distinct content block:** Double scrollbars are a UX nightmare.

---

## 🧠 Interaction Rules

- **Always provide an exit:** Never trap users in an interaction flow without a clear way to cancel or go back.
- **Don’t rely solely on hover:** Mobile users can’t hover.
- **Avoid animating layout-impacting properties:** Don’t animate `width`, `height`, or `top`; use transforms for better performance.
- **Ensure visible click targets:** All interactive areas should be visually clear and at least 44×44px for accessibility.
- **Don’t show hover states on active or disabled elements:** Visual redundancy or misleading cues can confuse users.
- **Avoid placing unrelated clickable elements too close together:** Prevents accidental clicks, especially on touch devices.
- **Ensure loading indicators are visible long enough to be noticed:** Otherwise, they undermine their purpose.

---

## 🧹 Content & Layout

- **Indicate text overflow clearly (e.g., ellipsis, scrollbar):** Prevent information loss.
- **Limit the number of primary navigation items:** Avoid overwhelming users.
- **Avoid redundant information in multiple places:** Clutters the interface.
- **Don’t hide essential actions behind long scrolls:** Makes key functionality hard to find.
- **Avoid excessive whitespace that pushes crucial content off-screen:** Prevents unnecessary scrolling.

---

## 🧹 Style & Consistency

- **Use z-index deliberately:** Avoid excessive use; layering should be easy to follow.
- **Don’t mix fixed and relative positioning arbitrarily:** This can cause layout conflicts.
- **Don’t color-code without text labels:** Colorblind users may not understand the meaning.
- **Don’t override system scrollbars or interaction patterns without purpose:** Custom behaviors often degrade usability.
- **Maintain consistent styles for interactive elements (e.g., buttons):** Consistency aids usability and learning.
- **Avoid unexpected layout or element position changes upon interaction:** Disorienting for the user.
- **Don’t use visual cues that imply interactivity when there is none:** Misleads the user.

---

## ♿ Accessibility & Responsiveness

- **Ensure keyboard navigation for all interactive elements.**
- **Keep focus outlines visible or provide a visible alternative.**
- **Support both touch and mouse input.**
- **Use relative units for layout:** Avoid hardcoded pixel values in responsive designs.
- **Maintain sufficient color contrast for text:** Crucial for accessibility.
- **Don’t rely solely on color to convey information:** Excludes color-blind users.

---

## 🔧 Maintainability & Dev-Friendliness

- **Style with semantic classes or utilities:** Don’t style based on DOM depth or implicit structure.
- **Keep CSS selectors flat:** Avoid deeply nested selectors; keep specificity low for easier overrides.
- **Avoid `!important` unless necessary:** It makes styles harder to debug and maintain.

---
