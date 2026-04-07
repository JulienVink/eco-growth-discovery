## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-15 - Optimal <head> Order and Font Loading
**Learning:** For Jekyll sites using third-party fonts, the <head> order significantly impacts FCP/LCP. Moving the viewport meta to the top, followed by resource hints and a high-priority preload for fonts, while making the actual font stylesheet non-blocking, provides the best balance between performance and layout stability.
**Action:** Always prioritize charset and viewport first, then use fetchpriority="high" for critical assets like the main CSS and font preloads, and ensure third-party CSS is loaded asynchronously.
