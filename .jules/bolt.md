## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-22 - Optimized Head Section and Font Loading
**Learning:** In Jekyll sites using the Cayman theme, the `<head>` section often contains sub-optimally ordered tags. Correctly ordering the `viewport` meta tag immediately after `charset`, placing SEO tags after `viewport`, and using non-blocking patterns for Google Fonts (via `media="print" onload="this.media='all'"` with `fetchpriority="high"` on preloads) significantly improves FCP and LCP without visual regressions.
**Action:** Always verify the `<head>` order and font loading strategy in static sites to ensure critical resources are prioritized and non-critical ones don't block rendering.
