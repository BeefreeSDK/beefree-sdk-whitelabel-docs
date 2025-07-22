---
description: Learn more about how to apply custom HTML to the head tags of your code.
---

# Add Custom Head HTML

## Overview

The **Settings** tab within the builder has an option that allows you to add custom HTML to the `<head>` section of your email or page design. This feature lets you easily inject CSS and metadata into the `<head>` section of your email, without relying on error-prone workarounds like using the HTML block, which is intended for different use cases, or post-processing your design's HTML after you export it. Adding custom `<head>` HTML is ideal if you want to add metadata, a favicon, or a stylesheet—especially if you're part of a large team managing high-volume campaigns. Whether you're a developer, a designer, or a marketing pro, this gives you the flexibility and precision needed for enterprise-level customization.

## Sanitizer Tags and Attributes

Prior to using the **Custom Head HTML** setting, familiarize yourself with the [tags](add-custom-head-html.md#table-1-allowed-tags), [attributes](add-custom-head-html.md#table-2-allowed-attributes-by-tag), and [protocols](add-custom-head-html.md#table-3-allowed-link-protocols) that are available when the [sanitizer](add-custom-head-html.md#the-sanitizer-and-adding-custom-html) is on. Each of the following tables in this section list and define the tags, attributes, and protocols you can use when the [sanitizer](add-custom-head-html.md#the-sanitizer-and-adding-custom-html) is **on**.

{% hint style="warning" %}
**Important:** If the sanitizer if **off**, you can add any custom HTML in the `<head>` section you'd like. However, it is important to consider using your own code may affect how the design is rendered. This could prevent it from adjusting to the screen size (for example, the responsiveness of the design). Make sure to use HTML that is email-compliant and responsive.
{% endhint %}

### Table 1: **Allowed Tags**

The following table lists and defines tags you can add the `<head>` section of the HTML when the **sanitizer is on**. It also provides examples you can reference.

{% hint style="info" %}
**Note:** If the sanitizer is off, you can add any attribute or tag.
{% endhint %}

| Tag Name | Description                                                               | HTML Example                                                              |
| -------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `base`   | Specifies the base URL for all relative URLs in the document              | `<base href="https://example.com" target="_blank">`                       |
| `link`   | Defines relationships between the current document and external resources | `<link href="styles.css" rel="stylesheet" type="text/css">`               |
| `meta`   | Provides metadata such as page description, keywords, author, etc.        | `<meta name="description" content="Free Web tutorials">`                  |
| `style`  | Embeds internal CSS styles                                                | `<style type="text/css" media="screen">body { font-size: 16px; }</style>` |
| `title`  | Sets the title of the document shown in browser tabs                      | `<title>My Website</title>`                                               |

### Table 2: **Allowed Attributes (by tag)**

The following table lists and defines attributes (by tag) you can add the `<head>` section of the HTML when the **sanitizer is on**. It also provides examples you can reference.

{% hint style="info" %}
**Note:** If the sanitizer is off, you can add any attribute or tag.
{% endhint %}

| Tag/Attribute            | Description                                           | HTML Example                                                           |
| ------------------------ | ----------------------------------------------------- | ---------------------------------------------------------------------- |
| `base`: `href`           | Base URL to use for relative URLs                     | `<base href="https://example.com">`                                    |
| `base`: `target`         | Default target for all hyperlinks and forms           | `<base target="_blank">`                                               |
| `link`: `href`           | URL to the external resource                          | `<link href="style.css">`                                              |
| `link`: `rel`            | Relationship between current and linked document      | `<link rel="stylesheet">`                                              |
| `link`: `type`           | Type of linked resource (usually MIME type)           | `<link type="text/css">`                                               |
| `link`: `sizes`          | Sizes of icons for visual representations             | `<link rel="icon" sizes="32x32" href="favicon-32.png">`                |
| `link`: `media`          | Specifies media/device for which the styles apply     | `<link rel="stylesheet" media="screen" href="style.css">`              |
| `meta`: `name`           | Name of metadata (e.g., description, keywords)        | `<meta name="viewport" content="width=device-width, initial-scale=1">` |
| `meta`: `content`        | Value associated with `name` or `property`            | `<meta name="description" content="Page about cats">`                  |
| `meta`: `charset`        | Declares the character encoding                       | `<meta charset="UTF-8">`                                               |
| `meta`: `property`       | Used for Open Graph or similar metadata standards     | `<meta property="og:title" content="Website title">`                   |
| `style`: `type`          | MIME type of the style content                        | `<style type="text/css">p { color: red; }</style>`                     |
| `style`: `media`         | Specifies the media/device the style is optimized for | `<style media="print">body { font-size: 12pt; }</style>`               |
| `title`: _no attributes_ | The `title` tag does not accept any attributes        | `<title>My Site</title>`                                               |

### Table 3: **Allowed Link Protocols**

The following table lists and defines link protocols you can add the `<head>` section of the HTML when the **sanitizer is on**. It also provides examples you can reference.

{% hint style="info" %}
**Note:** If the sanitizer is off, you can add any attribute or tag.
{% endhint %}

| Protocol | Description                 | HTML Example                                                       |
| -------- | --------------------------- | ------------------------------------------------------------------ |
| `http`   | HyperText Transfer Protocol | `<link href="http://example.com/style.css" rel="stylesheet">`      |
| `https`  | Secure version of HTTP      | `<link href="https://secure.com/app.css" rel="stylesheet">`        |
| `ftp`    | File Transfer Protocol      | `<link href="ftp://fileserver.com/resource.css" rel="stylesheet">` |

## How to Add Custom Head HTML

Take the following steps to add custom `<head>` HTML to your email or page design:

1. Enter the email or page builder.
2. Navigate to the sidebar.
3. Click on **SETTINGS.**
4. Scroll down to the **Custom Head HTML** section.
5. Type the \<head> HTML in the window.&#x20;
6. Save your changes.

When you export your HTML, the custom `<head>` HTML you added will be visible at the very end of the `<head>` section.&#x20;

{% hint style="info" %}
I**mportant:** While you can add custom `<head>` HTML that will be appended at the very end of the `<head>` section, you will not be able edit the existing HTML in the `<head>` section. &#x20;
{% endhint %}

## CSS Classes Overview

Emails, Pages, and Popups use a structured system of CSS classes to support navigation and custom styling. These classes reflect the layout hierarchy and block types, making it easier to apply targeted styles or understand the generated HTML.

### Email Design Classes

The class structure for emails follows a nested pattern:

```
body
└── nl-container
    └── row / row-X {mobile_hide / desktop_hide}
        └── row-content {stack} {reverse}
            └── column / column-X
                └── [Y_block] block-X {mobile_hide / desktop_hide}
```

#### **Key conventions:**

* `row-X`, `column-X`, and `block-X` indicate the order within the hierarchy.
* `{stack}` enables column stacking on mobile; `{reverse}` reverses the stacking order.
* `.mobile_hide` and `.desktop_hide` toggle visibility per device.

#### **Content block types** (`[Y_block]`) include:

* `.button_block`, `.divider_block`, `.image_block`, `.social_block`, `.html_block`, `.video_block`, `.icons_block`, `.menu_block`, `.addon_block`, `.heading_block`, `.paragraph_block`, `.list_block`, `.table_block`
* Deprecated: `.text_block`, `.empty_block`

### Pages and Popups

Page and Popup classes are similarly structured, with an `X-` prefix (default: `bee`, customizable per account):

```
X-page-container
└── X-row / X-row-Y {X-mobile_hide / X-desktop_hide}
    └── X-row-content {reverse}
        └── X-col / X-col-Y X-col-wZ
            └── X-block / X-block-Y X-[block name] {X-mobile_hide / X-desktop_hide}
```

#### **Notable patterns:**

* `X-col-wZ` denotes width (1–12 grid units).
* `X-block` identifies the content block type, such as:
  * `.X-button`, `.X-divider`, `.X-image`, `.X-social`, `.X-html`, `.X-video`, `.X-icons`, `.X-forms`, `.X-menu`, `.X-addon`, `.X-heading`, `.X-paragraph`, `.X-list`, `.X-table`, `.X-spacer`
  * Deprecated: `.X-text`, `.X-empty`

## Example Applications

This section includes three example scenarios of adding custom `<head>` HTML, and their corresponding code snippets. You can use these code snippets to start experimenting with the Custom Head HTML Setting, and start adding custom `<head>` code to your email and page designs.&#x20;

### Add a Favicon in the Head Code

Paste the following code in the **Custom Head HTML** window and save your changes to apply a favicon. If you'd like to customize this snippet, you can replace the `href` URL with your own image source for the favicon.

{% code overflow="wrap" %}
```html
<link rel="icon" type="image/x-icon" href="https://d15k2d11r6t6rl.cloudfront.net/pub/bfra/a34isttz/en5/ruc/8zo/tennis-shoes-footwear-fashion-nike-7968714.jpg">
```
{% endcode %}

### Use a Stylesheet URL

Paste the following code in the **Custom Head HTML** window and save your changes to apply the styles within the stylesheet. If you'd like to customize this snippet, you can replace the `href` URL with your own stylesheet URL.

{% code overflow="wrap" %}
```html
<link rel="stylesheet" href="https://zairro.github.io/beefree-custom-css/beefree-custom-design-html.css">
```
{% endcode %}

### Paste CSS Directly in the Window

Paste the following code in the **Custom Head HTML** window and save your changes to apply the CSS styles to your design.

```css
<style>
        * {
            box-sizing: border-box;
            font-family: 'Google Sans', Arial, sans-serif;
        }
        body {
            margin: 0;
            padding: 0;
            background-color: #f5f9f5;
            color: #2c3e2c;
        }
        a[x-apple-data-detectors] {
            color: inherit !important;
            text-decoration: inherit !important
        }
        #MessageViewBody a {
            color: inherit;
            text-decoration: none
        }
        p {
            line-height: inherit
        }
        .desktop_hide, .desktop_hide table {
            mso-hide: all;
            display: none;
            max-height: 0;
            overflow: hidden
        }
        .image_block img + div {
            display: none
        }
        sub, sup {
            font-size: 75%;
            line-height: 0
        }
        #converted-body .list_block ol, #converted-body .list_block ul, .body [class~=x_list_block] ol, .body [class~=x_list_block] ul, u + .body .list_block ol, u + .body .list_block ul {
            padding-left: 20px
        }
        
        /* Forest theme colors */
        h1, h2, h3 {
            color: #1a3a1a;
        }
        .button {
            background-color: #3a5a40 !important;
            border-color: #3a5a40 !important;
        }
        .button:hover {
            background-color: #2e4a34 !important;
        }
        table {
            border-color: #8ba888 !important;
        }
        thead {
            background-color: #e8f5e8 !important;
            color: #1a3a1a !important;
        }
        td {
            border-color: #8ba888 !important;
        }
        .nl-container {
            background-color: #f5f9f5 !important;
        }
        .row-content {
            background-color: #ffffff;
            border: 1px solid #d8e3d8;
        }

        @media (max-width: 520px) {
            .social_block.desktop_hide .social-table {
                display: inline-block !important
            }
            .mobile_hide {
                display: none
            }
            .row-content {
                width: 100% !important
            }
            .stack .column {
                width: 100%;
                display: block
            }
            .mobile_hide {
                min-height: 0;
                max-height: 0;
                max-width: 0;
                overflow: hidden;
                font-size: 0
            }
            .desktop_hide, .desktop_hide table {
                display: table !important;
                max-height: none !important
            }
        }
        /*[if mso ]>
        <style>sup, sub { font-size: 100% !important; } sup { mso-text-raise:10% } sub { mso-text-raise:-10% }</style> 
        <![endif]*/
    </style>
```

## Keyboard Navigation

You can use the keyboard to navigate the builder and add custom `<head>` HTML code. Reference the [Custom Keyboard Navigation article](../accessibility/custom-keyboard-navigation.md) to learn more about custom keyboard navigation options available within the builder.

{% hint style="info" %}
**Note:** The **Custom Head HTML** window also includes autocompletion options.
{% endhint %}

## The Sanitizer and Adding Custom HTML

When using custom HTML in the email builder, a code sanitizer will validate your code. It will automatically correct some issues such as HTML tags that are left open. It will also strip out code that isn't often supported by email clients. For example, script and iframe tags are removed since they often cause deliverability problems of security risks.

## Additional Considerations

Prior to adding your own custom `<head>` HTML consider the following:

* If the sanitizer is on, you can only use the following tags in the custom `<head>` HTML section . If it is off, there are no restrictions to which tags you can add.
  * `base`
  * `link`
  * `meta`
  * `style`
  * `title`
* If the sanitizer is on, you can only use the attributes listed in the [attributes by tag table](add-custom-head-html.md#table-2-allowed-attributes-by-tag).&#x20;
  * **Note:** If the sanitizer is off, you can use any HTML attribute or tag. Use this option carefully to ensure your designs are still responsive and render correctly.
* You cannot edit existing HTML within the `<head>` tags, you can only add custom HTML to that will be appended at the end of the `<head>` section.
* When the [sanitizer](add-custom-head-html.md#the-sanitizer-and-adding-custom-html) is on, the [HTML block](../content-blocks/custom-html.md) and Custom Head HTML setting have different available tags and attributes that are unique to each feature.  &#x20;
