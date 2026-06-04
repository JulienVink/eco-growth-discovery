## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-14 - Optimized Head Ordering and Non-Blocking Fonts
**Learning:** Placing the viewport meta tag immediately after the charset and before any external resources allows the browser to establish the layout viewport earlier, reducing reflows. Combining this with a non-blocking font loading pattern (preload + media="print" switch) significantly improves FCP by removing fonts from the critical path while still ensuring they are available quickly.
**Action:** Always prioritize the viewport meta tag placement and use the non-blocking pattern for external stylesheets like Google Fonts to minimize render-blocking.
