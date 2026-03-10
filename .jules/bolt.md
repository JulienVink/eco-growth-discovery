## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-10 - Optimal Head Ordering and Font Loading
**Learning:** Correct <head> tag ordering (charset, viewport, resource hints, SEO, then stylesheets) improves FCP/LCP. Preloading Google Fonts CSS with 'crossorigin' can cause double-downloads as the CSS file itself is typically requested without credentials.
**Action:** Always place viewport meta early, group resource hints before external assets, and ensure preloaded stylesheets are actually linked in the HTML.
