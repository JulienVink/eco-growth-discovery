## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-12 - Google Fonts Optimization and Head Order
**Learning:** For optimal performance, the viewport meta tag should immediately follow the charset to allow the browser to establish the layout viewport early. For Google Fonts, omitting the `crossorigin` attribute on the CSS preload/stylesheet (but keeping it for the `fonts.gstatic.com` preconnect) prevents double-fetching issues in some browsers. Combining `preload` with `fetchpriority="high"` and a non-blocking stylesheet (`media="print"`) provides the best balance of speed and progressive rendering.
**Action:** Always place viewport meta after charset and use the non-blocking pattern for external CSS with appropriate resource hints.
