## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-03-27 - Optimal <head> order and non-blocking fonts
**Learning:** Placing the viewport meta tag immediately after charset and reordering resource hints to precede preloads can slightly improve render start times. More importantly, using a non-blocking font loading pattern (media="print" onload="this.media='all'") prevents external CSS from blocking FCP.
**Action:** Always prioritize charset and viewport first, followed by resource hints, then non-blocking external assets.
