## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-05-01 - Non-blocking Font Loading and Head Order
**Learning:** Moving the viewport meta tag immediately after the charset meta tag and implementing non-blocking font loading via the 'print media' trick significantly improves initial rendering speed and prevents render-blocking CSS from delaying the first paint.
**Action:** Always prioritize viewport and charset tags at the very top of the <head> and use non-blocking patterns for third-party CSS like Google Fonts.
