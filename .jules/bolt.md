## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Non-blocking Font Loading and Head Order
**Learning:** Implementing the `media="print" onload="this.media='all'"` pattern for Google Fonts CSS, along with moving the `viewport` meta tag immediately after `charset`, significantly improves First Contentful Paint. Removing `crossorigin` from the CSS link itself (while keeping it for `fonts.gstatic.com` preconnect) prevents potential double-downloads.
**Action:** Always prioritize the order of `<head>` elements (charset, viewport, resource hints) and use non-blocking patterns for external styles that aren't critical for initial layout.
