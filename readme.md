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
  * [:warning:Providing text alternatives on `<applet>` elements](#providing-text-alternatives-on-applet-elements)
  * [Using `alt` attributes on images used as submit buttons](#using-alt-attributes-on-images-used-as-submit-buttons)
  * [Using `alt` attributes on `<img>` elements](#using-alt-attributes-on-img-elements)
  * [Using `<caption>` elements to associate data table captions with data tables](#using-caption-elements-to-associate-data-table-captions-with-data-tables)
  * [Using description lists](#using-description-lists)
  * [Using `<h1>` to `<h6>` to identify headings](#using-h1-to-h6-to-identify-headings)
  * [Using `id` and `headers` attributes to associate data cells with header cells in data tables](#using-id-and-headers-attributes-to-associate-data-cells-with-header-cells-in-data-tables)
  * [Using `<label>` elements to associate text labels with form controls](#using-label-elements-to-associate-text-labels-with-form-controls)
  * [Using `longdesc`](#using-longdesc)
  * [Using `<noembed>` with `<embed>`](#using-noembed-with-embed)
  * [Using `<ol>`, `<ul>` and `<dl>` for lists or groups of links](#using-ol-ul-and-dl-for-lists-or-groups-of-links)
  * [Using semantic markup to mark emphasized or special text](#using-semantic-markup-to-mark-emphasized-or-special-text)
  * [Using table markup to present tabular information](#using-table-markup-to-present-tabular-information)
  * [Using the body of the `<object>` element](#using-the-body-of-the-object-element)
  * [Using the `<dfn>` element to identify the defining instance of a word](#using-the-dfn-element-to-identify-the-defining-instance-of-a-word)
  * [Using the `dir` attribute on an inline element to resolve problems with nested directional runs](#using-the-dir-attribute-on-an-inline-element-to-resolve-problems-with-nested-directional-runs)
  * [Using the `lang` attribute on the `<html>` element](#using-the-lang-attribute-on-the-html-element)
  * [Using the `lang` attribute to identify changes in the human language](#using-the-lang-attribute-to-identify-changes-in-the-human-language)
  * [Using the `<link>` element and navigation tools](#using-the-link-element-and-navigation-tools)
  * [:warning:Using the `<link>` element to link to a glossary](#using-the-link-element-to-link-to-a-glossary)
  * [Using the `<ruby>` element](#using-the-ruby-element)
  * [Using the `scope` attribute to associate header cells and data cells in data tables](#using-the-scope-attribute-to-associate-header-cells-and-data-cells-in-data-tables)
  * [:warning:Using the `title` attribute of the `<frame>` and `<iframe>` elements](#using-the-title-attribute-of-the-frame-and-iframe-elements)
  * [Using the `title` attribute to identify form controls when the `<label>` element cannot be used](#using-the-title-attribute-to-identify-form-controls-when-the-label-element-cannot-be-used)
  * [Using null `alt` text and no `title` attribute on `<img>` elements for images that Assistive Technology should ignore](#using-null-alt-text-and-no-title-attribute-on-img-elements-for-images-that-assistive-technology-should-ignore)
  * [Providing heading elements at the beginning of each section of content](#providing-heading-elements-at-the-beginning-of-each-section-of-content)
  * [:warning:Using `<frame>` elements to group blocks of repeated material](#using-frame-elements-to-group-blocks-of-repeated-material)
  * [Providing a description for groups of form controls using `<fieldset>` and `<legend>` elements](#providing-a-description-for-groups-of-form-controls-using-fieldset-and-legend-elements)
  * [:warning:Using the `summary` attribute of the `<table>` element to give an overview of data tables](#using-the-summary-attribute-of-the-table-element-to-give-an-overview-of-data-tables)
  * [Ensuring that opening and closing tags are used according to specification](#ensuring-that-opening-and-closing-tags-are-used-according-to-specification)
  * [:warning:Ensuring that Web pages are well-formed](#ensuring-that-Web-pages-are-well-formed)
  * [Using meta refresh to create an instant client-side redirect](#using-meta-refresh-to-create-an-instant-client-side-redirect)
  * [Identifying the purpose of a link using link text combined with its enclosing list item](#identifying-the-purpose-of-a-link-using-link-text-combined-with-its-enclosing-list-item)
  * [Identifying the purpose of a link using link text combined with its enclosing paragraph](#identifying-the-purpose-of-a-link-using-link-text-combined-with-its-enclosing-paragraph)
  * [Identifying the purpose of a link in a data table using the link text combined with its enclosing table cell and associated table header cells](#identifying-the-purpose-of-a-link-in-a-data-table-using-the-link-text-combined-with-its-enclosing-table-cell-and-associated-table-header-cells)
  * [Identifying the purpose of a link using link text combined with the preceding heading element](#identifying-the-purpose-of-a-link-using-link-text-combined-with-the-preceding-heading-element)
  * [Identifying the purpose of a link in a nested list using link text combined with the parent list item under which the list is nested](#identifying-the-purpose-of-a-link-in-a-nested-list-using-link-text-combined-with-the-parent-list-item-under-which-the-list-is-nested)
  * [Using the `target` attribute to open a new window on user request and indicating this in link text](#using-the-target-attribute-to-open-a-new-window-on-user-request-and-indicating-this-in-link-text)
  * [Using a button with a `<select>` element to perform an action](#using-a-button-with-a-select-element-to-perform-an-action)

## HTML

### [Combining adjacent image and text links for the same resource](https://www.w3.org/WAI/WCAG21/Techniques/html/H2)

It's better to combine adjacent image and text links into a single `<a>` element.

Provided the `<img>` element contained in the `<a>` element would:

* Have an empty `alt` attribute when the `<a>` text would duplicate the information conveyed
* Have a valid `alt` attribute value when it would complement the `<a>` text

### [Creating a logical tab order through links, form controls, and objects](https://www.w3.org/WAI/WCAG21/Techniques/html/H4)

The `tabindex` attribute may be used to alter the tab order when the default is insufficient. For example on forms, or when a search field is the first thing you want users to tab into.

### [Providing text alternatives for the `<area>` elements of image maps](https://www.w3.org/WAI/WCAG21/Techniques/html/H24)

The `alt` attribute may be used on an `<area>` element to provide text alternatives on regions of an image map.

### [Providing a title using the `<title>` element](https://www.w3.org/WAI/WCAG21/Techniques/html/H25)

All HTML pages, including frames, must have a `<title>` element in the `<head>` with a simple phrase defining the purpose of the page.

### [Providing definitions for abbreviations by using the `<abbr>` element](https://www.w3.org/WAI/WCAG21/Techniques/html/H28)

Use the `<abbr>` element for any abbreviations, acronyms, and initialisms.

### [Providing link text that describes the purpose of a link for anchor elements](https://www.w3.org/WAI/WCAG21/Techniques/html/H30)

Provide descriptive text as the content of the `<a>` element.

If the only content of a link is an image, the text alternative for the image is used instead.

When the content of a link contains both text and one or more images, if the text is sufficient to describe the purpose of the link, the images may have an empty text alternative. When the images convey information beyond the purpose of the link, they must also have appropriate `alt` text.

### [Providing submit buttons](https://www.w3.org/WAI/WCAG21/Techniques/html/H32)

Provide a way to submit form data by having one of these:

* `<button type="submit">Submit</button>`
* `<input type="submit">`
* `<input type="image">`

### [Supplementing link text with the `title` attribute](https://www.w3.org/WAI/WCAG21/Techniques/html/H33)

Use the `title` attribute on the `<a>` element to provide additional text describing the link. It's used to clarify or further describe the purpose of the link.

Information the user should know, before following a link, should be provided in the link text.

### [Using a Unicode right-to-left mark (RLM) or left-to-right mark (LRM) to mix text direction inline](https://www.w3.org/WAI/WCAG21/Techniques/html/H34)

To bulletproof the correct handling of bidirectional text in HTML (for legacy or non-conformant browsers) you can add a Unicode control character to indicate the base direction of the surrounding text.

* `&lrm;` or `&#x200e;` for the left-to-right mark
* `&rlm;` or `&#x200f;` for the right-to-left mark

For example, assuming a base language of English (left-to-right), we'll use a phrase in Arabic (right-to-left) mid-sentence:

```html
<p>As the proverb says "<span lang="ar">اصبر تنل‏</span>&lrm;". Do not despair</p>
```

### [Providing text alternatives on `<applet>` elements](https://www.w3.org/WAI/WCAG21/Techniques/html/H35)

:warning: **Note**: `<applet>` is obsolete. Use `<embed>` or `<object>` instead.

The `alt` attribute may be used on an `<applet>` element to label it. Provide text alternatives to it in the body of the element.

### [Using `alt` attributes on images used as submit buttons](https://www.w3.org/WAI/WCAG21/Techniques/html/H36)

For `<input type="image">`, the `alt` attribute of the `<input>` element is used to provide a functional label that indicates the button's function, not the image description.

### [Using `alt` attributes on `<img>` elements](https://www.w3.org/WAI/WCAG21/Techniques/html/H37)

When using the `<img>` element, specify a short text alternative with the `alt` attribute.

When an image contains words that are important to understanding the content, the `alt` text should include those words.

The text alternative does not necessarily describe the visual characteristics of the image itself but must convey the same meaning as the image.

### [Using `<caption>` elements to associate data table captions with data tables](https://www.w3.org/WAI/WCAG21/Techniques/html/H39)

The `<caption>` represents the title of its parent `<table>`. It's a table identifier and acts like a title or heading for the table.

Using it allows screen readers to navigate directly to the caption for a table if one is present.

### [Using description lists](https://www.w3.org/WAI/WCAG21/Techniques/html/H40)

Provide description of names or terms using `<dl>`, `<dt>`, and `<dd>`. Multiple terms can be associated with a single description, as can a single term with multiple descriptions.

The `title` attribute can be used to provide additional information about the description list.

### [Using `<h1>` to `<h6>` to identify headings](https://www.w3.org/WAI/WCAG21/Techniques/html/H42)

Use heading markup to provide semantic code for headings in the content. It will allow assistive technologies to present the heading status of text to a user. A screen reader can recognize the code and announce the text as a heading with its level. Screen readers users are also able to navigate heading markup more quickly to find content of interest.

### [Using `id` and `headers` attributes to associate data cells with header cells in data tables](https://www.w3.org/WAI/WCAG21/Techniques/html/H43)

Use only when data cells are associated with more than one row and/or one column header.

Add a `headers` attribute to each `<td>`. Its value should be the `id` value(s) of the associated header cell(s) (separated by spaces, if multiple).

<details><summary>Example</summary>

```html
<table>
  <thead>
    <tr>
      <th id="b" rowspan="2">Budget</th>
      <th id="g" colspan="3">Groceries</th>
      <th id="r" rowspan="2">Remaining</th>
    </tr>
    <tr>
      <th id="v" headers="g">Veggies</th>
      <th id="f" headers="g">Fruit</th>
      <th id="m" headers="g">Meat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="b">$50</td>
      <td headers="g v">$10</td>
      <td headers="g f">$5</td>
      <td headers="g m">$20</td>
      <td headers="r">$15</td>
    </tr>
  </tbody>
</table>
```

</details>

### [Using `<label>` elements to associate text labels with form controls](https://www.w3.org/WAI/WCAG21/Techniques/html/H44)

Use the `<label>` element to explicitly associate a form control with a label. It's attached to a specific form control though its `for` attribute, which must be the same as the value of the `id` attribute of the form control.

<details><summary>Elements that use explicitly associated labels</summary>

* `<input type="text">`
* `<input type="checkbox">`
* `<input type="radio">`
* `<input type="file">`
* `<input type="password">`
* `<textarea>`
* `<select>`

</details>

<details><summary>Elements that do not use <code>&lt;label&gt;</code></summary>

* `<input type="submit">`: Use `value` attribute instead
* `<input type="reset">`: Use `value` attribute instead
* `<input type="hidden">`: Use `value` attribute instead
* `<input type="button">`: Use `value` attribute instead
* `<input type="image">`: Use `alt` attribute instead
* `<button>`: Use element content instead

</details>

### [Using `longdesc`](https://www.w3.org/WAI/WCAG21/Techniques/html/H45)

Provide information in a resource designated by the `longdesc` attribute when a short text alternative does not adequately convey the function or information provided in the image.

The `longdesc` attribute is a URI. And can be either a reference to a separate resource, or within the same page.

<details><summary>Example</summary>

```html
<!-- Long description in a separate resource -->
<img src="graph.jpg" alt="A complex graph" longdesc="graph-description.html">

<!-- Long description within the same page -->
<img src="graph.jpg" alt="A complex graph" longdesc="data.html#graph-description">
...
<div id="graph-description">
  <p>...</p>
</div>
```

</details>

### [Using `<noembed>` with `<embed>`](https://www.w3.org/WAI/WCAG21/Techniques/html/H46)

Provide alternative content for the `<embed>` element in a `<noembed>` element.

`<noembed>` is rendered only if the `<embed>` is not supported. It is a good idea to include it as a child element of `<embed>`, instead of positioning it anywhere else on the page, so that it functions as a text alternative associated with the `<embed>` element it describes.

### [Using `<ol>`, `<ul>` and `<dl>` for lists or groups of links](https://www.w3.org/WAI/WCAG21/Techniques/html/H48)

Create lists of related items using list elements appropriate for their purposes.

* The `<ol>` element is used when the list is ordered
* The `<ul>` element is used when the list is unordered
* Definition lists (`<dl>`) are used to group terms with their definitions

Avoid making lists using (visually formatting) markup like `*`, `•`, and `<br>`, as that is more difficult to navigate.

### [Using semantic markup to mark emphasized or special text](https://www.w3.org/WAI/WCAG21/Techniques/html/H49)

Use semantic markup to mark emphasized or special text. It provides structure to the document, and browsers can use it to make it perceivable to the user.

* `<em>` to represent stress emphasis of its contents
* `<strong>` to represent strong importance, seriousness, or urgency for its contents
* `<blockquote>` to represent a section that is quoted from another source
* `<cite>` to represent the title of a work (e.g. a book, a song, a film, etc.)
* `<q>` to represent some phrasing content quoted from another source
* `<sup>` to represent a superscript
* `<sub>` to represent a subscript

### [Using table markup to present tabular information](https://www.w3.org/WAI/WCAG21/Techniques/html/H51)

Use `<table>`, `<tr>`, `<th>`, and `<td>` to present tabular information

### [Using the body of the `<object>` element](https://www.w3.org/WAI/WCAG21/Techniques/html/H53)

The body of the `<object>` element can be used to provide a complete text alternative for the object, or may contain additional non-text content with text alternatives.

### [Using the `<dfn>` element to identify the defining instance of a word](https://www.w3.org/WAI/WCAG21/Techniques/html/H54)

The `<dfn>` element is used to indicate the defining instance of the enclosed term. It marks the occurrence of the term where the term is defined.

### [Using the `dir` attribute on an inline element to resolve problems with nested directional runs](https://www.w3.org/WAI/WCAG21/Techniques/html/H56)

The `dir` attribute is a global attribute that specifies the element's text directionality.

Its values can be:

* `ltr` to indicate left-to-right text
* `rtl` to indicate right-to-left text
* `auto` to indicate direction should be determined programmatically

### [Using the `lang` attribute on the `<html>` element](https://www.w3.org/WAI/WCAG21/Techniques/html/H57)

Identify the default language of a document by providing the `lang` global attribute on the `<html>` element.

### [Using the `lang` attribute to identify changes in the human language](https://www.w3.org/WAI/WCAG21/Techniques/html/H58)

Identify any changes in language on a page by using the `lang` global attribute. Its values are defined [here](https://tools.ietf.org/html/bcp47) consisting of a primary code followed by an optional subcode.

For example: `en` for English, and `en-GB` for British English.

### [Using the `<link>` element and navigation tools](https://www.w3.org/WAI/WCAG21/Techniques/html/H59)

The `<link>` element can provide metadata about the position of an HTML page within a set of Web pages or can assist in locating content with a set of Web pages.

The value of its `rel` attribute represents the relationship between the document containing the hyperlink and the destination resource.

Several values of [`rel`](https://html.spec.whatwg.org/multipage/links.html#linkTypes) are useful.

For example:

* `next` to indicate the next document in the series is the referenced document
* `prev` to indicate the previous document in the series is the referenced document

### [Using the `<link>` element to link to a glossary](https://www.w3.org/WAI/WCAG21/Techniques/html/H60)

:warning: **Note**: `rel="glossary"` is a valid link type in [HTML 4.01](https://www.w3.org/TR/html401/types.html#h-6.12). But it's not part of the predefined list in the [latest HTML standard](https://html.spec.whatwg.org/multipage/links.html#linkTypes).

Use a `<link>` element with `rel="glossary"` to provide a mechanism for locating a glossary on a separate page.

### [Using the `<ruby>` element](https://www.w3.org/WAI/WCAG21/Techniques/html/H62)

Use [the `<ruby>` element](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-ruby-element) to provide information about the pronunciation and meaning of a run of text where meaning is determined by pronunciation.

<details><summary>Example</summary>

```html
<p>
  <ruby>
    <rb>Charlize Theron</rb>
    <rp>(</rp>
      <rt>shar-LEEZ THERR-ən</tr>
    <rp>)</rp>
  </ruby>
</p>
```

</details>

### [Using the `scope` attribute to associate header cells and data cells in data tables](https://www.w3.org/WAI/WCAG21/Techniques/html/H63)

The `scope` attribute may be used to clarify the scope of any cell used as a header. The `scope` identifies whether the cell is a header for a row, column, or group of rows or columns. The values `row`, `col`, `rowgroup`, and `colgroup` identify these possible scopes respectively.

For simple tables that have the headers in the first row or column then it is sufficient to simply use the `<th>` elements without `scope`.

<details><summary>Example</summary>

```html
<table>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Email</th>
      <th scope="col">Phone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">John Doe</th>
      <td>john@doe.com</td>
      <td>1234567890</td>
    </tr>
    <tr>
      <th scope="row">Jane Doe</th>
      <td>jane@doe.com</td>
      <td>9876543210</td>
    </tr>
  </tbody>
</table>
```

</details>

### [Using the `title` attribute of the `<frame>` and `<iframe>` elements](https://www.w3.org/WAI/WCAG21/Techniques/html/H64)

:warning: **Note**: `<frame>`, `<frameset>`, and `<noframes>` are obsolete. Use `<iframe>` and CSS instead, or use server-side includes to generate complete pages with the various invariant parts merged in.

Provide a label for a frame so users can determine which frame to enter and explore in detail.

This is different than the `<title>` element. The attribute facilitates navigation among frames and the element clarifies the user's current location.

### [Using the `title` attribute to identify form controls when the `<label>` element cannot be used](https://www.w3.org/WAI/WCAG21/Techniques/html/H65)

Use the `title` attribute to provide an accessible name for form controls when the visual design does not include text on the screen that can be associated with the control as a label.

<details><summary>Example</summary>

```html
<input type="text" title="Area code" size="3" value="">
<input type="text" title="First three digits of phone number" size="3" value="">
<input type="text" title="Last four digits of phone number" size="4" value="">
```

</details>

### [Using null `alt` text and no `title` attribute on `<img>` elements for images that Assistive Technology should ignore](https://www.w3.org/WAI/WCAG21/Techniques/html/H67)

`<img>` elements can be safely ignored by Assistive Technology if no `title` attribute is used and the alternative text is set to null (e.g. `alt=""`).

### [Providing heading elements at the beginning of each section of content](https://www.w3.org/WAI/WCAG21/Techniques/html/H69)

Use section headings to convey the structure of the content. Avoid skipping levels in the sequence of headings.

### [Using `<frame>` elements to group blocks of repeated material](https://www.w3.org/WAI/WCAG21/Techniques/html/H70)

:warning: **Note**: `<frame>`, `<frameset>`, and `<noframes>` are obsolete. Use `<iframe>` and CSS instead, or use server-side includes to generate complete pages with the various invariant parts merged in.

Use frames to organize elements to provide a mechanism for easily bypassing blocks of repeated content.

If the site uses framesets, organize the blocks of content into separate frames. Make certain that the repeated blocks of content appear in the same `<frame>` within the `<frameset>` of each Web page. In addition, each `<frame>` element must have a `title` attribute to describe the content of the frame.

### [Providing a description for groups of form controls using `<fieldset>` and `<legend>` elements](https://www.w3.org/WAI/WCAG21/Techniques/html/H71)

Form controls can be grouped by enclosing them within the `<fieldset>` element. All controls within a given `<fieldset>` are then related.

The first element inside the `<fieldset>` must be a `<legend>` element, which provides a label or description for the group.

This is most important for related radio buttons and checkboxes, or where a group of controls within a larger form requires an additional heading to provide a description specific to that particular group.

### [Using the `summary` attribute of the `<table>` element to give an overview of data tables](https://www.w3.org/WAI/WCAG21/Techniques/html/H73)

:warning: **Note**: `summary` on `<table>` is obsolete. Use [these techniques](https://html.spec.whatwg.org/multipage/tables.html#table-descriptions-techniques) instead.

Provide a brief overview of how data has been organized into a table or a brief explanation of how to navigate the table.

### [Ensuring that opening and closing tags are used according to specification](https://www.w3.org/WAI/WCAG21/Techniques/html/H74)

Provide closing tags for all elements that require them.

Ensure there are no closing tags for all elements that forbid them.

Ensure opening and closing tags of all elements are correctly nested.

### [Ensuring that Web pages are well-formed](https://www.w3.org/WAI/WCAG21/Techniques/html/H75)

:warning: **Note**: Only applies if you're using [the XML syntax](https://html.spec.whatwg.org/multipage/xhtml.html#the-xhtml-syntax) for writing HTML.

Avoid key errors that are known to cause problems by checking document well-formedness with an XML parser.

### [Using meta refresh to create an instant client-side redirect](https://www.w3.org/WAI/WCAG21/Techniques/html/H76)

:information_source: **Note**: Redirects are preferably implemented on the server side.

Enable redirects on the client side without confusing the user.

<details><summary>Example</summary>

```html
<head>
  <!-- Immediate (0 seconds) redirect to another URI (example.com) -->
  <meta http-equiv="refresh" content="0; url=https://example.com">
</head>
```

</details>

### [Identifying the purpose of a link using link text combined with its enclosing list item](https://www.w3.org/WAI/WCAG21/Techniques/html/H77)

The `<li>` enclosing the `<a>` provides context for an otherwise unclear link when the `<li>` is the nearest enclosing block-level ancestor element.

<details><summary>Example</summary>

```html
<ul>
  <li>
    Our biggest discounts of the year:
    <a href="/winter-sale">The Winter Sale</a>.
  </li>
  ...
</ul>
```

</details>

### [Identifying the purpose of a link using link text combined with its enclosing paragraph](https://www.w3.org/WAI/WCAG21/Techniques/html/H78)

Same as ["Identifying the purpose of a link using link text combined with its enclosing list item"](#identifying-the-purpose-of-a-link-using-link-text-combined-with-its-enclosing-list-item). Except `<p>` provides the context.

### [Identifying the purpose of a link in a data table using the link text combined with its enclosing table cell and associated table header cells](https://www.w3.org/WAI/WCAG21/Techniques/html/H79)

The table header cell(s) associated to the `<td>` enclosing the `<a>` provides context for an otherwise unclear link when the `<td>` is the nearest enclosing block-level ancestor element.

### [Identifying the purpose of a link using link text combined with the preceding heading element](https://www.w3.org/WAI/WCAG21/Techniques/html/H80)

Whenever possible, provide link text that identifies the purpose of the link without needing additional context.

The preceding heading to the `<a>` provides context for an otherwise unclear link.

### [Identifying the purpose of a link in a nested list using link text combined with the parent list item under which the list is nested](https://www.w3.org/WAI/WCAG21/Techniques/html/H81)

Whenever possible, provide link text that identifies the purpose of the link without needing additional context.

Same as ["Identifying the purpose of a link using link text combined with its enclosing list item"](#identifying-the-purpose-of-a-link-using-link-text-combined-with-its-enclosing-list-item). Except the links are in a nested list inside an `<li>`.

### [Using the `target` attribute to open a new window on user request and indicating this in link text](https://www.w3.org/WAI/WCAG21/Techniques/html/H83)

On links that open new windows, provide both a `target="_blank"` attribute value and information indicating that such link will open in a new window in the link text.

### [Using a button with a `<select>` element to perform an action](https://www.w3.org/WAI/WCAG21/Techniques/html/H84)

Avoid having an action occur as a side effect of choosing a value for the `<select>` element.

Instead allow the user to control when an action is performed by selecting a button to perform the action.

## Disclaimer

This document is a summarized list of informative techniques for accessible Web content.

It is best used alongside "[How to Meet WCAG 2.1](https://www.w3.org/WAI/WCAG21/quickref/)" and "[Web Content Accessibility Guidelines (WCAG) 2.1](https://www.w3.org/TR/2018/REC-WCAG21-20180605/)" for meeting the success criteria established in the guidelines. For more on techniques [click here](https://www.w3.org/WAI/WCAG21/Understanding/understanding-techniques.html).

## Credit

Original W3C document: [Techniques for WCAG 2.1](https://www.w3.org/WAI/WCAG21/Techniques)

Copyright © 2017-2018 [W3C](https://www.w3.org/)® ([MIT](https://www.csail.mit.edu/), [ERCIM](https://www.ercim.eu/), [Keio](https://www.keio.ac.jp/), [Beihang](http://ev.buaa.edu.cn/)). W3C [liability](https://www.w3.org/Consortium/Legal/ipr-notice#Legal_Disclaimer), [trademark](https://www.w3.org/Consortium/Legal/ipr-notice#W3C_Trademarks) and [document use](https://www.w3.org/Consortium/Legal/copyright-documents) rules apply.
