## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-04-15 - Optimal <head> Order and Non-blocking Fonts
**Learning:** For optimal First Contentful Paint, the <head> should follow a strict order: charset, viewport, SEO tags, then resource hints/preloads. Loading Google Fonts via a non-blocking "print" media query pattern significantly improves FCP by removing the CSS from the critical rendering path while maintaining FOIT/FOUT control via font-display: swap.
**Action:** Always prioritize charset and viewport as the first two tags in the <head>. Use high fetchpriority for font preloads but ensure the actual stylesheet link is non-blocking.
