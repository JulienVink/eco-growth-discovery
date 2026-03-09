## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimized Head Order and Resource Hints
**Learning:** Organizing the `<head>` with charset and viewport first, followed by resource hints (preconnect, dns-prefetch, preload) before SEO tags and stylesheets, improves FCP/LCP by enabling the speculative parser to discover critical assets earlier. Also, preloading Google Fonts CSS with `crossorigin` can cause double-downloads as the browser treats it as a different request than the actual stylesheet fetch.
**Action:** Always place resource hints as high as possible in the `<head>` and verify `crossorigin` attributes on preloads against the actual resource fetch mode.
