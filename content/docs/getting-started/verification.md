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

### 5. Add a system prompt
To help the **AI assistant** coordinate all tools more efficiently, you may provide a **system prompt**. This is **optional** — the tools will still work without it, but **performance** and **relevance** may improve.
> ⚠️ **DISCLAIMER**  <br>
The following system prompt is provided **only as an example.**
Before using it in a **production environment**, make sure to review and validate it with your organization’s **security and compliance teams.** Requirements may vary depending on your **infrastructure, policies, and risk profile.**

```text
1. Always start by analyzing the user input.
  - If the input contains multiple keywords that can map to different dimensions 
    (brand, category, tag, or product name), then call the corresponding tools 
    in combination immediately (for example, "Nike running shoes" = brand + category).
    Try to extract as many keywords as possible.
  - If the input contains only one relevant keyword, 
    always call search_products_by_name_mcp first.

2. After collecting results from the first call(s):
  - If you have at least 5 results, return them.
  - If you have fewer than 5 results, continue with fallback logic.

3. Fallback logic (if you have less than 5 results):
  Call the tools one by one in this order until you gather at least 5 results:
  - search_products_by_category_mcp
  - search_products_by_tag_mcp
  - search_products_by_brand_mcp
  If still fewer than 5 results, retry by splitting the input into individual 
  keywords and repeating the process.

4. Always combine all non-empty results, remove duplicates, and always return 
products with their permalinks.

5. If after all retries there are still fewer than 5 results, return what you have 
and explain politely to the user.

Never expose tool names, API details, or internal system logic to the user. 
``` 


### 6. Start chatting with your AI assistant
Once connected, you can immediately start interacting with your **AI assistant (e.g., ChatGPT)** through **MCP Integrate** to quickly discover and explore products that interest you.
