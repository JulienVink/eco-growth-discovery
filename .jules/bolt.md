## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2026-08-08 - Jekyll Sass Minification Configuration
**Learning:** Enabling Sass style compression directly in `_config.yml` via the `sass: style: compressed` configuration instructs Jekyll's Sass compilation pipeline to automatically minify CSS output. This reduces CSS asset transfer sizes by ~45% without requiring external NPM packages or custom build steps, ensuring compliance with GitHub Pages environment restrictions.
**Action:** Always verify if a static site builder has built-in compression capabilities before introducing external dependencies.
