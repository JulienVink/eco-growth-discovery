## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimal <head> Order and Non-blocking Fonts
**Learning:** The order of tags in the `<head>` significantly impacts rendering performance. Moving the viewport meta tag to the top (immediately after charset) and implementing non-blocking font loading (media="print" onload pattern) combined with `fetchpriority="high"` on preloads can measurably improve FCP and LCP.
**Action:** Always prioritize the viewport meta tag and use non-blocking patterns for external CSS like Google Fonts to prevent render-blocking.
