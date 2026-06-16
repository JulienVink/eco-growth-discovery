## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-10 - Comprehensive Google Fonts Optimization
**Learning:** For optimal font loading, use a `preload` with `fetchpriority="high"` (without `crossorigin` for googleapis.com), combined with a non-blocking stylesheet using `media="print" onload="this.media='all'"` and a `noscript` fallback. This maximizes parallelization and prevents render-blocking.
**Action:** Apply this multi-layered pattern when optimizing web fonts to balance performance and compatibility.
