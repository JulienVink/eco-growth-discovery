## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Optimal <head> Order and Non-blocking Fonts
**Learning:** Moving the viewport meta tag to the very top (right after charset) ensures the browser starts layout calculations correctly as soon as possible. Using the `media="print" onload="this.media='all'"` pattern for Google Fonts prevents them from blocking the initial render, improving FCP/LCP.
**Action:** Always prioritize viewport meta and use non-blocking patterns for external CSS that isn't critical for the initial paint.
