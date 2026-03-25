## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-08 - Optimal <head> Order and Non-blocking Font Loading
**Learning:** Reordering `<head>` tags (placing `charset` and `viewport` first) and using a non-blocking Google Fonts loading pattern (`media="print" onload="this.media='all'"`) significantly improves early rendering and reduces FCP. Additionally, removing `crossorigin` from the Google Fonts CSS preload prevents potential double-download issues as the CSS itself is typically fetched without credentials.
**Action:** Always prioritize `charset` and `viewport` in the `<head>` and use non-blocking patterns for external resources like fonts that are not strictly required for the initial paint but benefit from early discovery via `preload` with `fetchpriority="high"`.
