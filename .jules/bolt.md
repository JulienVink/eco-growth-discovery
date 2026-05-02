## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-05-02 - Optimal <head> Ordering and Font Loading
**Learning:** Ordering the `<head>` section by placing the viewport meta tag immediately after charset, followed by SEO tags and then resource hints/preloads, ensures the browser can start layout and high-priority resource fetching as early as possible. Using the `media="print" onload="this.media='all'"` pattern for Google Fonts prevents them from being render-blocking.
**Action:** Apply this specific ordering and the non-blocking font pattern in all HTML/Liquid layouts to improve FCP and LCP.
