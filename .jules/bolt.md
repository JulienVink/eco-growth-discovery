## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-14 - Optimized Head Tag Order and Non-blocking Fonts
**Learning:** Reordering the `<head>` section to place the viewport meta tag immediately after charset and using the `media="print" onload="this.media='all'"` pattern for fonts significantly improves browser parsing and rendering performance. Combining this with `fetchpriority="high"` on preloads ensures critical resources are prioritized without blocking the initial paint.
**Action:** Always prioritize viewport meta placement and implement non-blocking loading for external stylesheets like Google Fonts in future projects.
