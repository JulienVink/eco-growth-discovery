## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-05-19 - Preserving CSS Cascade in Cayman Theme Overrides
**Learning:** In the Cayman theme, `_includes/head-custom.html` is placed after the main stylesheet to allow user-defined overrides. Moving it earlier in the `<head>` for performance (e.g., to prioritize critical CSS) can break the intended CSS cascade and cause regressions in styling.
**Action:** Always place custom head includes after the main theme stylesheet unless there is a specific reason to do otherwise, and verify that style overrides still work as expected.
