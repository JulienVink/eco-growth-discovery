## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimized Head Order and Font Loading
**Learning:** Placing the viewport meta tag immediately after the charset meta ensures the browser can determine the page scale before parsing the rest of the head. Combined with a non-blocking font loading pattern (media="print" onload="this.media='all'"), this minimizes render-blocking resources and improves First Contentful Paint.
**Action:** Always prioritize critical meta tags at the very beginning of the `<head>` and use asynchronous loading for external stylesheets that aren't required for the initial paint.
