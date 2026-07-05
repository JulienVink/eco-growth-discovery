## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-07-05 - Google Fonts CORS Mismatch Regression
**Learning:** Using `crossorigin` on a font `preload` link but omitting it on the corresponding `stylesheet` link causes the browser to download the resource twice (once for each CORS mode).
**Action:** Always ensure the `crossorigin` attribute matches across all `preload`, `stylesheet`, and `<noscript>` fallback links for the same font URL to prevent performance regressions.
