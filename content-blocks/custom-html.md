# Custom HTML

## Overview

The Custom HTML content block enables you to insert your own HTML code into designs crafted in the builder. While it's as straightforward as adding a text block, this feature is primarily intended for those proficient in HTML. Using custom HTML can impact how your design adjusts to various screen sizes, so make sure the HTML you use is responsive and email compliant. Note that custom HTML typically falls outside of standard support.\


<figure><img src="https://lh7-eu.googleusercontent.com/-8YjBcyUDf7hjR8sKq-MNvOLCywdqJNX9WK6sJAqvwm_Ge3WrGnTw-eUYtYXaJ7T3LJfw87LL7mCsxtpQF3YuQTtN2zqkFZS-g0hnSZDIutDIvaqkDbQXD9IbgiYgJbm-T023WsJ8HSBjgpZpCp0rsg" alt=""><figcaption></figcaption></figure>

## Why Use Custom HTML?

Here are a few scenarios where custom HTML can be valuable:

* **Customized Content:** You're not restricted to predefined settings, giving you more control over styling.
* **Special Elements:** Add content like HTML5 videos or anchor links, which are not standard elements in the builder.
* **Advanced CSS Effects:** While CSS animations aren't universally supported in emails, they can make your web pages more engaging.
* **Live Content:** Embed real-time content like product recommendations or countdowns by pasting code from external vendors.

## How to Add Custom HTML

1. **Drag the Block:** Insert an HTML content block into your design, just like you would with any other block.
2. **Edit HTML:** Click the block to open the HTML editor on the sidebar. You'll see placeholder code, which you can replace with your own HTML. Syntax highlighting and indentation features help make the code readable.

<figure><img src="https://lh7-eu.googleusercontent.com/2kI4wBse5pF1jPtDXy6YlPmvSUTtdlGLAEBCJ75AeVlRJf4ryFXNG9NjsfbllfucnJO6VGN4qZJAN_lUXpN-Ybbjw8jStPtlCEbw_l913Dyt3tn4jrmSQnl3N584OEF2RxRNIZbkwQuk87qwqhBGLPI" alt=""><figcaption></figcaption></figure>

## HTML Tag Restrictions in Emails

When adding custom HTML to emails, a code sanitizer checks and automatically corrects your code. Unsupported tags like \<script> and \<iframe> are removed to avoid security risks and deliverability issues.

### Allowed HTML Tags: (for emails only)

<details>

<summary>List of allowed tags</summary>

```
    a
    abbr
    acronym
    address
    area
    article
    aside
    b
    base
    basefont
    bdo
    big
    blockquote
    br
    button
    caption
    center
    cite
    code
    col
    colgroup
    dd
    del
    details
    dfn
    dialog
    dir
    div
    dl
    dt
    em
    embed
    fieldset
    figcaption
    figure
    footer
    font
    form
    head
    header
    h1
    h2
    h3
    h4
    h5
    h6
    hgroup
    hr
    html
    i
    img
    input
    ins
    kbd
    keygen
    label
    legend
    li
    link
    main
    map
    mark
    menu
    meta
    nav
    object
    ol
    optgroup
    option
    p
    param
    picture
    pre
    progress
    q
    s
    samp
    section
    select
    small
    source
    span
    strike
    strong
    style
    sub
    summary
    sup
    table
    tbody
    td
    template
    textarea
    tfoot
    th
    thead
    time
    title
    tr
    track
    tt
    u
    ul
    var
    video
```

</details>

<details>

<summary>List of allowed attributes</summary>

```
*:          style, id, class, data-*, title
div:        itemscope, itemtype
meta:       itemprop, content
a:          href, name, target
img:        align, alt, border, height, hspace, src, vspace, width, usemap
table:      align, bgcolor, border, cellpadding, cellspacing, width
tbody:      align, valign
td:         align, bgcolor, colspan, height, rowspan, valign, width
tr:         align, bgcolor, valign
tfoot:      align, valign
th:         align, bgcolor, colspan, height, rowspan, valign, width
thead:      align, valign
li:         type
video:      autoplay, controls, height, loop, muted, poster, preload, src, width
source:     media, src, type
map:        name
area:       alt, coords, href, shape, target
ol:         start
input:      alt, type, checked, multiple, value, name]
```

</details>

<details>

<summary>List of allowed link protocols</summary>

```
http, https, ftp, mailto, tel, sms
```

</details>

{% hint style="info" %}
**Note:** If the sanitizer is off, you can add any HTML you'd like. However, this is not recommended, because it can result in rendering issues. The sanitizer is intended to support you in using reliable HTML tags for rendering.
{% endhint %}

## Using Custom HTML with Pages

The Page Builder doesn't employ a sanitizer, offering more freedom but also more responsibility. You can use any HTML, CSS, or JavaScript syntax when designing landing pages.

## Accessibility Keys for Custom HTML Content Blocks

This section outlines and describes the accessibility keys currently available for navigating the Custom HTML content block. In this section, you'll learn about which keys to use to set your focus, customize properties, exit your design, and save your changes.

{% hint style="warning" %}
We are still working on developing our application's accessibility, and you may notice that some actions aren't available yet. Additional accessibility features are coming soon.&#x20;
{% endhint %}

### **Setting Your Focus**

Take the following steps to set your focus:

1. **Select the Custom HTML Block:** Use `ArrowUp` or `ArrowDown` to navigate to the Custom HTML block. A high-contrast border will appear to show it's selected.
2. **Activate the Block:** Press `Enter` to activate the block, preparing the sidebar for HTML input.

### **Enter HTML**

Take the following steps to enter your HTML:

1. **Accessing the HTML Editor:** After activation, use `Tab` to move to the HTML editor in the sidebar, where you can input your HTML.
2. **Inputting and Editing HTML Code:** Enter your HTML code directly in the editor.

### **Exiting and Saving Changes**

Use the following key to save and exit your design:

* Press `Esc` to exit the editor and save your changes.
