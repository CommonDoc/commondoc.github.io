# [Package] common-doc

CommonDoc classes and and accessors.

## [Class] code-block

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `language`: The language of the code block's contents.

## [Function] document-reference

~~~lisp
(document-reference object)
~~~

## [Class] block-quote

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] text

~~~lisp
(text object)
~~~

## [Class] unordered-list

Slots:

* `metadata`: Node metadata.

* `children`: The list of `list-item` instances.

## [Function] title

~~~lisp
(title object)
~~~

## [Function] version

~~~lisp
(version object)
~~~

## [Function] keywords

~~~lisp
(keywords object)
~~~

## [Class] document-link

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `document-reference`: A reference key for the linked document.
 If `nil`, the link is only to a section within the document.

* `section-reference`: A reference key for the linked section.

## [Class] definition-list

Slots:

* `metadata`: Node metadata.

* `children`: The list of `definition` instances.

## [Class] paragraph

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] inline-quote

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] subject

~~~lisp
(subject object)
~~~

## [Function] publisher

~~~lisp
(publisher object)
~~~

## [Class] list-item

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] markup

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] cells

~~~lisp
(cells object)
~~~

## [Function] rows

~~~lisp
(rows object)
~~~

## [Class] italic

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] ordered-list

Slots:

* `metadata`: Node metadata.

* `children`: The list of `list-item` instances.

## [Function] source

~~~lisp
(source object)
~~~

## [Function] rights

~~~lisp
(rights object)
~~~

## [Class] text-node

Slots:

* `metadata`: Node metadata.

* `text`: The node's text.

## [Class] section

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `title`: The section title.

* `reference`: A reference key for this section.

## [Class] document-node

Slots:

* `metadata`: Node metadata.

## [Function] term

~~~lisp
(term object)
~~~

## [Function] language

~~~lisp
(language object)
~~~

## [Class] bold

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] find-node

~~~lisp
(find-node tag-name)
~~~

Find a node class by its tag name.

## [Class] base-list

Slots:

* `metadata`: Node metadata.

## [Class] cell

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] image

Slots:

* `metadata`: Node metadata.

* `source`: The source where the image is stored.

* `description`: A plain text description of the image.

## [Function] image

~~~lisp
(image object)
~~~

## [Function] reference

~~~lisp
(reference object)
~~~

## [Class] definition

Slots:

* `metadata`: Node metadata.

* `term`: The definition term.

* `definition`: Defines the term.

## [Function] definition

~~~lisp
(definition object)
~~~

## [Class] row

Slots:

* `metadata`: Node metadata.

* `header`: The row header.

* `footer`: The row footer.

* `cells`: The cells in the row.

## [Class] figure

Slots:

* `metadata`: Node metadata.

* `image`: The figure's image.

* `description`: A description of the image.

## [Function] find-tag

~~~lisp
(find-tag class)
~~~

Return a node class' tag name.

## [Function] footer

~~~lisp
(footer object)
~~~

## [Function] created-on

~~~lisp
(created-on object)
~~~

## [Function] description

~~~lisp
(description object)
~~~

## [Class] document

Slots:

* `children`: The document's children nodes.

* `title`: The document's title.

* `creator`: The creator of the document.

* `publisher`: The document's publisher.

* `subject`: The subject the document deals with.

* `description`: A description of the document.

* `keywords`: A list of strings, each being a keyword for the document.

* `reference`: A reference string to uniquely identify the
              document within a certain context.

* `language`: An [RFC4646](http://www.ietf.org/rfc/rfc4646.txt) string denoting the language the document is written in.

* `rights`: Information on the document's copyright.

* `version`: The document version.

* `created-on`: The date and time when the document was
               created. By default, this is the date and time at instance
               creation.

## [Class] superscript

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] web-link

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `uri`: The URI of the external resource.

## [Function] section-reference

~~~lisp
(section-reference object)
~~~

## [Function] metadata

~~~lisp
(metadata object)
~~~

## [Class] base-quote

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] strikethrough

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] content-node

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] children

~~~lisp
(children object)
~~~

## [Function] uri

~~~lisp
(uri object)
~~~

## [Function] header

~~~lisp
(header object)
~~~

## [Macro] define-node

~~~lisp
(define-node name (&rest superclasses) slots &rest class-options)
~~~

Define a CommonDoc node.

## [Class] subscript

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Function] find-special-slots

~~~lisp
(find-special-slots class)
~~~

Return a node class' special slots.

## [Class] code

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] underline

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

## [Class] table

Slots:

* `metadata`: Node metadata.

* `rows`: The list of rows in a table.

## [Class] link

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

# [Package] common-doc.error

CommonDoc errors.

## [Function] path-string

~~~lisp
(path-string condition)
~~~

## [Class] bad-pathname

Slots:

* `format-control`: NIL

* `format-arguments`: NIL

* `path-string`: NIL

## [Class] macro-error

Slots:

* `format-control`: NIL

* `format-arguments`: NIL

## [Class] no-macro-expander

Slots:

* `format-control`: NIL

* `format-arguments`: NIL

* `node`: NIL

## [Function] node

~~~lisp
(node condition)
~~~

## [Class] common-doc-error

Slots:

* `format-control`: NIL

* `format-arguments`: NIL

# [Package] common-doc.file

File-related operations for CommonDoc.

## [Function] absolute-path

~~~lisp
(absolute-path pathname-or-string)
~~~

Take a pathname or string. If it's absolute, return it,
  otherwise, merge it with *base-directory*.

## [Variable] *base-directory*

The directory all resources with relative paths are based from. This is
intended to be bound by a `let` by specific input formats.

# [Package] common-doc.ops

Common operations on CommonDoc documents.

## [Function] collect-figures

~~~lisp
(collect-figures doc)
~~~

## [Function] traverse-document

~~~lisp
(traverse-document node function)
~~~

Apply a side effectful function recursively to every element
  in the document. Depth-first.

## [Function] node-specific-equal

~~~lisp
(node-specific-equal node-a node-b)
~~~

Use this method to make node equality more specific.

## [Function] node-equal

~~~lisp
(node-equal node-a node-b)
~~~

Recursively check whether two nodes are equal.

## [Function] collect-tables

~~~lisp
(collect-tables doc)
~~~

## [Function] collect-external-links

~~~lisp
(collect-external-links doc)
~~~

# [Package] common-doc.format

CommonDoc input/output formats.

## [Class] document-format

Slots:

## [Function] parse-document

~~~lisp
(parse-document document-format input)
~~~

Parse an input into a CommonDoc document.

## [Function] emit-to-string

~~~lisp
(emit-to-string format document)
~~~

## [Function] emit-document

~~~lisp
(emit-document document-format document stream)
~~~

Dump a CommonDoc document into a stream.

# [Package] common-doc.macro

CommonDoc macros.

## [Function] expand-macro

~~~lisp
(expand-macro node)
~~~

Replace a macro node with a primitive node.

## [Function] name

~~~lisp
(name object)
~~~

## [Function] expand-macros

~~~lisp
(expand-macros node)
~~~

Recursively expand all macros in `node`.

## [Class] macro-node

Slots:

* `metadata`: Node metadata.

* `children`: The node's children.

* `name`: The name of the macro.

# [Package] common-doc.util

CommonDoc utilities.

## [Macro] doc

~~~lisp
(doc class args &rest children)
~~~

Easily create a document or node.

  `(doc subscript ())`

  is equivalent to:

  `(make-instance 'subscript)`

  `(doc document (:title "My Document") (text-node (:text "...")))`

  is equivalent to:

  `(make-instance 'document :title "My Document" :children (list (make-instance 'text-node :text "...")))`

## [Function] make-meta

~~~lisp
(make-meta pairs)
~~~

Create a metadata hash table from a list of cons cells.

## [Function] make-text

~~~lisp
(make-text string &optional metadata)
~~~

Create a text node from the contents of a string.
