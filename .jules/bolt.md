## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-22 - Non-blocking Google Fonts and Head Reordering
**Learning:** Moving `meta charset` and `viewport` to the top of the `<head>` ensures faster layout initialization. Implementing a non-blocking font loading pattern (media="print" with onload) significantly reduces render-blocking resources while maintaining font availability.
**Action:** Always prioritize charset and viewport first in the head. Use the preload + async stylesheet pattern for external CSS like Google Fonts to improve First Contentful Paint.
