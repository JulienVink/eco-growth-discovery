## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-08 - Non-blocking Font Loading & Head Order
**Learning:** Moving the `viewport` meta tag immediately after `charset` ensures earlier layout processing. Using `media="print" onload="this.media='all'"` for external stylesheets (like Google Fonts) prevents them from being render-blocking, significantly improving First Contentful Paint. Removing `crossorigin` from CSS preloads avoids redundant double-downloads when CORS isn't required.
**Action:** Prioritize early `viewport` placement and non-blocking loading for all non-critical third-party CSS.
