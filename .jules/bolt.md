## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-14 - Optimized <head> Order and Resource Prioritization
**Learning:** Placing the viewport meta tag immediately after the charset meta tag and before any CSS or JS allows the browser to begin layout calculations sooner. Using `fetchpriority="high"` on critical preloads like fonts can measurably improve LCP. Removing `crossorigin` from Google Fonts CSS preloads prevents potential double-downloads.
**Action:** Always prioritize viewport and charset tags, and use `fetchpriority="high"` for critical path assets in the `<head>`.
