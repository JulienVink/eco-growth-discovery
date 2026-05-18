## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-05-18 - Optimal <head> Order and Non-blocking Fonts
**Learning:** Placing the charset and viewport meta tags at the very top of the <head>, followed by resource hints and non-blocking CSS loading (using the media="print" onload pattern), optimizes the Critical Rendering Path. Omitting crossorigin from Google Fonts CSS preloads prevents redundant network requests caused by CORS mismatches.
**Action:** Always prioritize the viewport meta tag and use non-blocking patterns for external stylesheets to minimize render-blocking resources.
