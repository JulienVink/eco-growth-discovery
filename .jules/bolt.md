## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-05-11 - Google Fonts Preload CORS Mismatch
**Learning:** Including the 'crossorigin' attribute in a Google Fonts CSS 'preload' link when the actual 'stylesheet' link lacks it causes the browser to ignore the preloaded resource and perform a redundant fetch. The Google Fonts CSS API (unlike the font files themselves) does not require 'crossorigin' by default.
**Action:** Ensure 'crossorigin' attributes match between 'preload' and 'stylesheet' links for the same resource. For Google Fonts CSS, omit 'crossorigin' from both to maximize cache hits and prevent double-loading.
