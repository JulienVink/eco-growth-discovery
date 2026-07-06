## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Google Fonts Preload and CORS
**Learning:** Google Fonts CSS files (fonts.googleapis.com/css2) are typically not served with CORS headers. Using the `crossorigin` attribute on a `<link rel="preload" as="style">` tag for these resources will cause the browser to use a CORS request, which won't match the subsequent non-CORS stylesheet request, leading to a double-fetch performance regression.
**Action:** Do not use `crossorigin` when preloading Google Fonts CSS unless the stylesheet link itself also uses it.
