---
title: Classes
layout: docs
---

The following is a reference of CommonDoc classes and their methods.

# Basic Classes

## `document-node`

The base class of all document classes.

Slots:

* `metadata`: Node metadata.

## `content-node`

A node with children. This is the base class of all nodes that have a `children`
slot (Except `document`, since this class inherits from document-node) and can
also be used as a way to represent a generic grouping of elements. This is
useful when building a CommonDoc document by parsing some input language.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `text-node`

A node representing a bare string of text.

Slots:

* `metadata`: Node metadata.

* `text`: The node's text.

## `paragraph`

A paragraph.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

# Markup

## `markup`

The superclass of all inline markup elements.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `bold`

Text in this element is bold.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `italic`

Text in this element is italicized.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `underline`

Text in this element is underlined.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `strikethrough`

Text in this element is striked out.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `code`

Text in this element is monospaced or otherwise marked as
  code or computer output.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `superscript`

Text in this element is superscripted relative to containing elements.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `subscript`

Text in this element is subscripted relative to containing elements.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

# Code

## `code-block`

A block of code.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `language`: The language of the code block's contents.

# Quotes

## `base-quote`

The base class of all quotes.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `inline-quote`

A quote that occurs inside a paragraph in the document.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `block-quote`

A block quote.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

# Links

## `link`

The base class for all links, internal and external.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `document-link`

A link to a section of this document, to another document and optionally a
  section within that document. See also the `reference` slot in the `document`
  class.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `document-reference`: A reference key for the linked document.
 If `nil`, the link is only to a section within the document.

* `section-reference`: A reference key for the linked section.

## `web-link`

An external link.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `uri`: The URI of the external resource.

# Lists

## `base-list`

The base class of all lists.

Slots:

* `metadata`: Node metadata.

## `list-item`

The item in a non-definition list.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## `definition`

An item in a definition list.

Slots:

* `metadata`: Node metadata.

* `term`: The definition term.

* `definition`: Defines the term.

## `unordered-list`

A list where the elements are unordered.

Slots:

* `metadata`: Node metadata.

* `children`: The list of `list-item` instances.

## `ordered-list`

A list where the elements are ordered.

Slots:

* `metadata`: Node metadata.

* `children`: The list of `list-item` instances.

## `definition-list`
A list of definitions.

Slots:

* `metadata`: Node metadata.

* `children`: The list of `definition` instances.

# Images and Figures

## `image`

An image.

Slots:

* `metadata`: Node metadata.

* `source`: The source where the image is stored.

* `description`: A plain text description of the image.

## `figure`

A figure, an image plus an annotation.

Slots:

* `metadata`: Node metadata.

* `image`: The figure's image.

* `description`: A description of the image.

# Tables

## `table`

A table.

Slots:

* `metadata`: Node metadata.

* `rows`: The list of rows in a table.

## `row`

A row in a table.

Slots:

* `metadata`: Node metadata.

* `header`: The row header.

* `footer`: The row footer.

* `cells`: The cells in the row.

## `cell`

A cell in a table.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

# Structure

## `section`

Represents a section in the document. Unlike HTML, where a
  section is just another element, sections in CommonDoc contain their contents.

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `title`: The section title.

* `reference`: A reference key for this section.

## `document`

A document.

Slots:

* `children`: The document's children nodes.

* `title`: The document's title.

* `creator`: The creator of the document.

* `publisher`: The document's publisher.

* `subject`: The subject the document deals with.

* `description`: A description of the document.

* `keywords`: A list of strings, each being a keyword for the document.

* `reference`: A reference string to uniquely identify the document within a
              certain context.

* `language`: An [RFC4646](http://www.ietf.org/rfc/rfc4646.txt) string denoting
  the language the document is written in.

* `rights`: Information on the document's copyright.

* `version`: The document version.

* `created-on`: The date and time when the document was created. By default,
               this is the date and time at instance creation.
