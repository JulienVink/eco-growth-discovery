## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-22 - Optimal <head> Order and Non-blocking Fonts
**Learning:** Placing the viewport meta tag immediately after the charset and using a non-blocking pattern for Google Fonts (media="print" onload="this.media='all'") with a high fetchpriority preload significantly improves rendering performance and FCP.
**Action:** Always prioritize the viewport meta tag and use non-blocking patterns for external CSS that isn't critical for the initial paint.
