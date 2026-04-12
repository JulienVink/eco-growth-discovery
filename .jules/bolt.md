## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Head Ordering and Non-blocking Fonts
**Learning:** Placing the viewport meta tag immediately after the charset and using a non-blocking pattern for fonts (media="print" onload="this.media='all'") significantly improves FCP and LCP by ensuring early layout determination and preventing render-blocking CSS.
**Action:** Always prioritize viewport and charset order and use non-blocking patterns for non-critical external resources.
