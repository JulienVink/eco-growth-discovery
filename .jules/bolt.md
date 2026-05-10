## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-08 - Optimized Head Structure and Font Loading
**Learning:** The previous layout used `preload` for Google Fonts but missed the actual `stylesheet` link, and the `viewport` meta was below SEO tags. Reordering the `<head>` to place the viewport immediately after charset and using a non-blocking media-switch pattern for fonts ensures faster layout calculation and prevents external CSS from blocking FCP.
**Action:** Always verify that `preload` links are followed by their functional counterparts (like `stylesheet`) and maintain the optimal `<head>` order: charset, viewport, SEO, hints, preloads, non-blocking styles, main stylesheet.
