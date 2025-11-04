+++
title = "ACP Fields in MCP Integrate"
description = ""
date = 2021-05-01T18:10:00+00:00
updated = 2021-05-01T18:10:00+00:00
draft = false
weight = 90
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false

prev = "docs/acp/acp-support.md"
next = "docs/acp/prepare-products.md"
+++

This section explains how **ACP fields** are handled in **MCP Integrate**. **Agentic Commerce Protocol (ACP)** defines a set of **product data fields** that enable seamless, **AI-driven** commerce. commerce. For more information about the fields, visit [Official ACP website](https://developers.openai.com/commerce/specs/feed "Official ACP website").

MCP Integrate provides:
* **Automatically mapped fields** — existing WooCommerce fields that correspond directly to ACP fields.
* **Added fields** — new fields introduced by the plugin, available as global settings or per-product fields.
* **Unsupported fields** — ACP fields that are not yet available in WooCommerce or MCP Integrate.

### 1. Automatically mapped fields
Here is a list of fields that are **automatically mapped** on WooCommerce fields:
| ACP Field             | WooCommerce Field     |
|-----------------------|-----------------------|
| id                    | _sku                  |
| gtin                  | _global_unique_id     | 
| title                 | post_title            | 
| description           | post_content          | 
| link                  | site_url + post_name  | 
| product_category      | taxonomy              | 
| brand                 | taxonomy              | 
| weight                | _weight               |
| length                | _length               | 
| width                 | _width                | 
| height                | _height               |
| dimensions            | _length x _width x _height |
| weight_unit           | woocommerce_dimension_unit |
| dimension_unit        | woocommerce_weight_unit |
| currency              | woocommerce_currency |
| image_link            | image_url | 
| additional_image_link | _product_image_gallery | 
| price                 | _price | 
| sale_price            | _sale_price | 
| sale_price_effective_date| _sale_price_dates_from + _sale_price_dates_to| 
| availability          | _stock_status | 
| inventory_quantity    | _stock | 
| item_group_id         | post_parent | 
| item_group_title      | post_title |
| offer_id              | _sku + seller_name + _price |
| shipping              | multiple fields |
| item_group_title      | post_title |
| product_review_count  | _wc_review_count |
| product_review_rating | _wc_average_rating |
| related_product_id    | _upsell_ids, _crosssell_ids |


### 2. Added fields
These fields are not included in WooCommerce by default, but **MCP Integrate** adds **full support** for them:
* enable_search
* enable_checkout
* mpn
* condition
* material
* age_group
* video_link
* model_3d_link
* unit_pricing_measure / base_measure
* pickup_method
* pickup_sla
* color
* size
* size_system
* gender
* delivery_estimate
* seller_name
* seller_url
* seller_privacy_policy
* seller_tos
* return_policy
* return_window
* warning 
* age_restriction

See the next page for instructions on how to set them up.

### 3. Unsupported fields
These fields are not yet supported, but may be added in future updates:
| Conditionally required| Recommended         |Optional|
|-----------------------|---------------------|-----------------------------|
| availability_date     | shipping            | applicable_taxes_fees       |
|                       | q_and_a             | pricing_trend               |
|                       | relationship_type   | Custom_variant1_category    |
|                       | raw_review_data     | Custom_variant1_option      |
|                       | geo_price           | Custom_variant2_category    |
|                       | geo_availability    | Custom_variant2_option      |
|                       | popularity_score    | Custom_variant3_category    |
|                       | return_rate         | Custom_variant3_option      |
|                       |                     | store_review_count          |
|                       |                     | store_review_rating         |
|                       |                     | expiration_date             |