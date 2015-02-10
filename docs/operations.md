---
title: Operations on documents
layout: docs
---

>As computers capable of constructing concordances become mor and more
>acessible, the task of compiling such an index becomes less and less
>significant. What was once the work of a lifetime – or longer – is now a
>relatively modest project. In 1875, Mary Cowden Clarke produly wrote in the
>preface to her concordance of Shakespeare that "to furnish a faithful guide to
>this rich mine of intellectual treasure... has been the ambition of a life; and
>it is hoped that the sixteen years' assiduous labour... may be found to have
>accomplished that ambition" (Clarke 1875). It may have been hard for
>Mrs. Clarke to imagine that a century later, just one person, Todd K. Bender,
>professor of English at the University of Wisconsin, would produce nine
>concordances in the time it took her to construct one.
>
>Witten, I., & Moffat, A. (1999). *Managing gigabytes: Compressing and indexing
>documents and images* (2nd ed.). San Francisco, Calif.: Morgan Kaufmann.

Representing documents is half the battle: Now we need ways to traverse, edit
and filter them.

# Built-in Operations

## Testing Equality

The `node-equal` method can be used to check equality between two nodes. It
recursively traverses the node trees, applying node-specific equality functions
to verify that the two trees match.

~~~lisp

~~~

## Extracting Features

It's common to find, in printed work, lists of figures and tables. Operations to
extract both these objects from documents are provided in the `collect-figures`
and `collect-tables` methods, which extract, respectively, a list of all figure
and table elements in the document.
