## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-10 - Holistic <head> Optimization for Performance
**Learning:** For optimal browser parsing and rendering, the `<head>` order should be: 1. Charset, 2. Viewport (early layout), 3. Preconnect/Resource hints, 4. Font preloads with `fetchpriority="high"`, 5. Non-blocking font styles, 6. Main stylesheet with `fetchpriority="high"`. This combination minimizes FCP and LCP while ensuring early layout stability.
**Action:** Always prioritize charset and viewport at the top of the `<head>` and use non-blocking patterns for non-critical third-party CSS.
