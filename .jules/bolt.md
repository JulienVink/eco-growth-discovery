## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-08 - Optimal <head> structure and Font Loading
**Learning:** Placing the `viewport` meta tag immediately after `charset` and using non-blocking font loading (media="print" swap) significantly improves FCP by prioritizing layout calculation and removing render-blocking CSS. Preloading fonts without `crossorigin` avoids double-downloads for Google Fonts CSS.
**Action:** Always audit <head> element order and font loading strategy for quick, high-impact performance wins.
