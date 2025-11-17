+++
title = "Verification"
description = ""
date = 2021-05-01T18:20:00+00:00
updated = 2021-05-01T18:20:00+00:00
draft = false
weight = 60
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false

prev = "docs/getting-started/troubleshooting.md"
next = "docs/getting-started/contact.md"
+++

To confirm the plugin is working correctly:

### 1. Install Visual Studio Code
Download and install **VSCode** from the official website: [Visual Studio Code](https://code.visualstudio.com/ "Visual Studio Code"). 

### 2. Install the AI Toolkit extension
Open **VSCode** and add the **AI Toolkit extension**. For detailed instructions, visit: [AI Toolkit for Visual Studio Code](https://code.visualstudio.com/docs/intelligentapps/overview "AI Toolkit for Visual Studio Code").

### 3. Connect to MCP Integrate
Follow the instructions in the [Connect to MCP Server](https://code.visualstudio.com/docs/intelligentapps/agentbuilder "Connect to MCP Server") section to link your **AI Toolkit** with **MCP Integrate.**
### 4. Verify your mcp.json
Your configuration file should look like this:
```json
{
  "servers": {
    "mcp-integrate": {
      "type": "http",
      "url": "http://<your-site-domain>/wp-json/mcp-integrate/entrypoint"
    }
  }
}
```

### 5. Start chatting with your AI assistant
Once connected, you can immediately start interacting with your **AI assistant (e.g., ChatGPT)** through **MCP Integrate** to quickly discover and explore products that interest you.
