+++
title = "Preparing WooCommerce products for ACP"
description = ""
date = 2021-05-01T18:10:00+00:00
updated = 2021-05-01T18:10:00+00:00
draft = false
weight = 100
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false

prev = "docs/acp/product-fields.md"
+++

The **MCP-Integrate** plugin helps you make your **WooCommerce** products fully compatible with the **Agentic Commerce Protocol (ACP).**

To add **product fields required by ACP** that don’t exist in **WooCommerce** by default, follow these steps:

### 1. Global fields
Go to **Settings > MCP Integrate**, where you’ll find all global fields grouped into categories: **Required, Conditionally required, Recommended, and Optional.**
Fill in the necessary details **(required fields are mandatory for ACP compatibility)**, then click **Save changes** at the bottom of the page.

![ACP global fields](/images/acp_global_fields.png)

### 2. Product-specific fields
Open any product by going to **WooCommerce > Products > All Products**, then select a product to edit.
At the bottom of the product edit page, you’ll find the **ACP Fields** section, organized by the same categories: **Required, Conditionally required, Recommended, and Optional.**
Complete the necessary fields **(required ones must be filled for ACP compatibility)**.

<img src="/images/acp_product_specific_fields.png" alt="ACP product specific fields" style="width: 730px; height: auto; display: block; margin: 1rem auto;" />


Finish by clicking **Update** in the upper-right corner of the page to save your changes.
<img src="/images/update_product.png" alt="Update product" style="margin: 1rem auto;" />