## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-14 - Optimal Head Structure for Cayman
**Learning:** For the Cayman theme, placing the viewport meta tag immediately after charset and before SEO tags/resource hints maximizes the browser's ability to begin layout calculations. Combining `fetchpriority="high"` on preloads with the `media="print" onload="this.media='all'"` pattern for fonts effectively eliminates render-blocking without sacrificing LCP.
**Action:** Apply this specific head ordering and non-blocking font pattern whenever modifying layouts to ensure peak performance.
