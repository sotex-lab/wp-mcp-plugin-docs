+++
title = "Initial Configuration"
description = ""
date = 2021-05-01T18:20:00+00:00
updated = 2021-05-01T18:20:00+00:00
draft = false
weight = 40
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false

prev = "docs/getting-started/get-started.md"
next = "docs/getting-started/troubleshooting.md"
+++

After activation, configure the plugin:
<br>
Go to **Settings > MCP Integrate** in your WordPress admin panel.

At the top of the page you will see Plugin Settings.
<img src="/images/plugin_settings.png" alt="Plugin Settings" style="margin: 1rem auto;" />

Here’s what each option does:

* **Keep data on uninstall** – Enable this if you want to preserve all MCP Integrate data after the plugin is uninstalled.

* **Enable MCP** – Turns on the MCP REST API endpoint required for communication with your AI assistant.

* **Enable ACP** – Activates integration with the Agentic Commerce Protocol (ACP), adding all ACP-compatible product fields automatically.

* **Enable ACP Debug** – Enables a REST API endpoint for products that are not fully ACP-compatible, listing all missing fields for easier debugging.

Make sure to save your changes by clicking **Save Changes** at the bottom of the page.
