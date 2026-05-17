## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimal <head> Order and Non-blocking Fonts
**Learning:** The order of tags in `<head>` significantly impacts the Critical Rendering Path. Placing the viewport meta immediately after charset allows earlier layout calculations. Combining `preload` with `fetchpriority="high"` for fonts ensures they are discovered early, while the `media="print" onload="this.media='all'"` pattern prevents them from blocking the initial paint.
**Action:** Always prioritize charset, viewport, and critical resource hints/preloads in the `<head>` before any blocking stylesheets or scripts. Use the non-blocking pattern for non-critical or external CSS.
