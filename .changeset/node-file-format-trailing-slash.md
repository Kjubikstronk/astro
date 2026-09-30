---
'@astrojs/node': patch
---

Fixes prerendered pages returning a 404 in standalone mode when `build.format` is `'file'` or `'preserve'` and the URL has a trailing slash, such as `/about/`. With `trailingSlash: 'always'`, the server redirected `/about` to `/about/` and then could not serve it.
