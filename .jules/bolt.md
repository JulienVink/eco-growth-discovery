## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Non-blocking Google Fonts with Fetch Priority
**Learning:** Combining `<link rel="preload" as="style" fetchpriority="high">` with `<link rel="stylesheet" media="print" onload="this.media='all'">` provides an optimal balance between early discovery and non-blocking rendering for Google Fonts.
**Action:** Apply this pattern to mission-critical external stylesheets to improve LCP and FCP simultaneously.
