+++
title = "Troubleshooting"
description = ""
date = 2021-05-01T18:20:00+00:00
updated = 2021-05-01T18:20:00+00:00
draft = false
weight = 50
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false

prev = "docs/getting-started/initial-configuration.md"
next = "docs/getting-started/verification.md"
+++

### Common Issues

* **Plugin won’t activate:**
    * Verify PHP version (must be **8.0+**).

    * Check WordPress version (must be **6.4+**).

* **Permission errors:**

    * Check file permissions on the plugin directory.

    * Ensure your web server can read/write plugin files.

* **UI errors or missing interface elements:**

    * Run ```npm install``` and then ```npm run build``` inside the plugin directory to rebuild assets.

