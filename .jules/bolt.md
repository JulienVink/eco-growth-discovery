## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-22 - Holistic <head> Optimization
**Learning:** Optimizing the `<head>` section requires a holistic approach: ordering the viewport meta immediately after charset, removing redundant resource hints (like dns-prefetch when preconnect exists), and using non-blocking patterns for external CSS (like Google Fonts) with `fetchpriority="high"` on critical preloads. Correcting `crossorigin` on CSS preloads (removing it for Google Fonts CSS) avoids browser warnings and double-fetching.
**Action:** Always audit the `<head>` for tag order and resource hint redundancy, and use the `media="print" onload="this.media='all'"` pattern for non-critical or external stylesheets.
