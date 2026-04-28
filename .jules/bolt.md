## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-04-28 - Optimized <head> Order and Non-blocking Fonts
**Learning:** Placing the viewport meta tag immediately after the charset and using a non-blocking pattern for Google Fonts () significantly improves the browser's ability to start rendering and reduces FCP. Removing redundant attributes like 'type' and 'crossorigin' from CSS links also cleans up the HTML and avoids potential fetch issues.
**Action:** Always prioritize the viewport meta tag and implement non-blocking font loading with a noscript fallback for any web project to ensure faster perceived performance.
