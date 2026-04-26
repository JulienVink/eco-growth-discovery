## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimizing Head Order and Font Loading
**Learning:** Reordering the `<meta name="viewport">` tag to immediately follow the charset, and implementing a non-blocking font loading pattern (`media="print"`) with `fetchpriority="high"`, significantly improves First Contentful Paint (FCP) and ensures the browser starts layout calculations as early as possible.
**Action:** Prioritize the viewport meta tag placement and use asynchronous resource loading for non-critical CSS while maintaining a `<noscript>` fallback.
