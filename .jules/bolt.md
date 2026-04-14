## 2025-03-07 - Critical CSS for Cayman Theme
**Learning:** Overriding `_includes/head-custom.html` allows injecting styles directly into the `<head>` of the Cayman theme without modifying the theme's core layouts. This is effective for adding critical CSS to improve FCP/LCP.
**Action:** Use this pattern for performance optimizations in other Jekyll themes by identifying the appropriate extension points in their layouts.

## 2025-03-07 - Tool Output Truncation Limit
**Learning:** The 1000-character environment limit for tool output applies to the aggregate output of a single tool call, even if it contains multiple commands (like several `sed` or `cat` commands). Truncated output can appear complete if it happens to end with a newline or common closing tag, leading to incomplete codebase understanding.
**Action:** Use separate tool calls for each command or small line range to ensure full content retrieval. Always verify file completeness using `wc -l` or `wc -c` before assuming the output is complete.
