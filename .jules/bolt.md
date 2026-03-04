## 2024-05-22 - [Font Preconnect Optimization]
**Learning:** The default Cayman theme (and many others) includes a `preconnect` to `fonts.gstatic.com` but misses the `crossorigin` attribute. Since fonts are fetched using CORS, a preconnect without `crossorigin` cannot be reused, forcing the browser to perform a new handshake and wasting one Round Trip Time (RTT).
**Action:** Always include `crossorigin` when preconnecting to font domains like `fonts.gstatic.com`. Also, preconnect to the CSS domain (`fonts.googleapis.com`) and remove unnecessary `crossorigin` from the CSS `preload`.
