# Effective a11y

> Hands-on Web accessibility.

## Table of contents

* [HTML](#html)
  * [Combining adjacent image and text links for the same resource](#combining-adjacent-image-and-text-links-for-the-same-resource)
  * [Creating a logical tab order through links, form controls, and objects](#creating-a-logical-tab-order-through-links-form-controls-and-objects)
  * [Providing text alternatives for the `<area>` elements of image maps](#providing-text-alternatives-for-the-area-elements-of-image-maps)
  * [Providing a title using the `<title>` element](#providing-a-title-using-the-title-element)
  * [Providing definitions for abbreviations by using the `<abbr>` element](#providing-definitions-for-abbreviations-by-using-the-abbr-element)
  * [Providing link text that describes the purpose of a link for anchor elements](#providing-link-text-that-describes-the-purpose-of-a-link-for-anchor-elements)
  * [Providing submit buttons](#providing-submit-buttons)
  * [Supplementing link text with the `title` attribute](#supplementing-link-text-with-the-title-attribute)
  * [Using a Unicode right-to-left mark (RLM) or left-to-right mark (LRM) to mix text direction inline](#using-a-unicode-right-to-left-mark-rlm-or-left-to-right-mark-lrm-to-mix-text-direction-inline)
  * [Providing text alternatives on `<applet>` elements](#providing-text-alternatives-on-applet-elements)
  * [Using `alt` attributes on images used as submit buttons](#using-alt-attributes-on-images-used-as-submit-buttons)

## HTML

### Combining adjacent image and text links for the same resource

It's better to combine adjacent image and text links into a single `<a>` element.

Provided the `<img>` element contained in the `<a>` element would:

* Have an empty `alt` attribute when the `<a>` text would duplicate the information conveyed
* Have a valid `alt` attribute value when it would complement the `<a>` text

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H2)</sub>

### Creating a logical tab order through links, form controls, and objects

The `tabindex` attribute may be used to alter the tab order when the default is insufficient. For example on forms, or when a search field is the first thing you want users to tab into.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H4)</sub>

### Providing text alternatives for the `<area>` elements of image maps

The `alt` attribute may be used on an `<area>` element to provide text alternatives on regions of an image map.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H24)</sub>

### Providing a title using the `<title>` element

All HTML pages, including frames, must have a `<title>` element in the `<head>` with a simple phrase defining the purpose of the page.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H25)</sub>

### Providing definitions for abbreviations by using the `<abbr>` element

Use the `<abbr>` element for any abbreviations, acronyms, and initialisms.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H28)</sub>

### Providing link text that describes the purpose of a link for anchor elements

Provide descriptive text as the content of the `<a>` element.

If the only content of a link is an image, the text alternative for the image is used instead.

When the content of a link contains both text and one or more images, if the text is sufficient to describe the purpose of the link, the images may have an empty text alternative. When the images convey information beyond the purpose of the link, they must also have appropriate `alt` text.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H30)</sub>

### Providing submit buttons

Provide a way to submit form data by having one of these:

* `<button type="submit">Submit</button>`
* `<input type="submit">`
* `<input type="image">`

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H32)</sub>

### Supplementing link text with the `title` attribute

Use the `title` attribute on the `<a>` element to provide additional text describing the link. It's used to clarify or further describe the purpose of the link.

Information the user should know, before following a link, should be provided in the link text.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H33)</sub>

### Using a Unicode right-to-left mark (RLM) or left-to-right mark (LRM) to mix text direction inline

To bulletproof the correct handling of bidirectional text in HTML (for legacy or non-conformant browsers) you can add a Unicode control character to indicate the base direction of the surrounding text.

* `&lrm;` or `&#x200e;` for the left-to-right mark
* `&rlm;` or `&#x200f;` for the right-to-left mark

For example, assuming a base language of English (left-to-right), we'll use a phrase in Arabic (right-to-left) mid-sentance:

```html
<p>As the proverb says "<span lang="ar">اصبر تنل‏</span>&lrm;". Do not despair</p>
```

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H34)</sub>

### Providing text alternatives on `<applet>` elements

:warning: `<applet>` is deprecated and obsolete. Use `<embed>` or `<object>` instead.

The `alt` attribute may be used on an `<applet>` element to label it. Provide text alternatives to it in the body of the element.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H35)</sub>

### Using `alt` attributes on images used as submit buttons

For `<input type="image">`, the `alt` attribute of the `<input>` element is used to provide a functional label that indicates the button's function, not the image description.

<sub>[More information](https://www.w3.org/WAI/WCAG21/Techniques/html/H36)</sub>

## Disclaimer

This document is a summarized list of informative techniques for accessible Web content.

It's best used alongside "[How to Meet WCAG 2.1](https://www.w3.org/WAI/WCAG21/quickref/)" and "[Web Content Accessibility Guidelines (WCAG) 2.1](https://www.w3.org/TR/2018/REC-WCAG21-20180605/)" for meeting the success criteria established in the standard. For more on techniques [click here](https://www.w3.org/WAI/WCAG21/Understanding/understanding-techniques.html).

## Credit

Original W3C document: [Techniques for WCAG 2.1](https://www.w3.org/WAI/WCAG21/Techniques)

Copyright © 2017-2018 [W3C](https://www.w3.org/)® ([MIT](https://www.csail.mit.edu/), [ERCIM](https://www.ercim.eu/), [Keio](https://www.keio.ac.jp/), [Beihang](http://ev.buaa.edu.cn/)). W3C [liability](https://www.w3.org/Consortium/Legal/ipr-notice#Legal_Disclaimer), [trademark](https://www.w3.org/Consortium/Legal/ipr-notice#W3C_Trademarks) and [document use](https://www.w3.org/Consortium/Legal/copyright-documents) rules apply.
