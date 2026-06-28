## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-06-28 - Consistent Crossorigin for Google Fonts
**Learning:** Google Fonts CSS resources must have matching 'crossorigin' attributes across 'preload', 'stylesheet', and 'noscript' links. Mismatched attributes cause browsers to treat them as separate resources, leading to redundant network requests and double-loading.
**Action:** Always verify that 'crossorigin' presence is consistent for all link tags referencing the same Google Fonts URL.
