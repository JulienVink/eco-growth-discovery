## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-05-14 - Optimal Font Preload Attributes
**Learning:** Including `crossorigin` on a Google Fonts CSS preload when the corresponding stylesheet does NOT use it causes the browser to ignore the preload. Also, `type="text/css"` is redundant in modern HTML.
**Action:** Always match CORS attributes between preload and stylesheet, and omit redundant type attributes for cleaner, faster-parsing HTML.
