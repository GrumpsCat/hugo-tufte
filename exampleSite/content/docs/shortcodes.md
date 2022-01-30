+++
author = "Slashformotion"
date = "2015-01-19T23:57:58-08:00"
hasMath = false
title = "Shortcodes"
hideDate = true
hideReadTime = true
+++

This theme provides the following shortcodes in an attempt to completely
support all the features present in the
[Tufte-css](https://github.com/edwardtufte/tufte-css) project.

- `blockquote`
  - **Description**: Wrap text in a blockquote and insert optional
  `cite` or `footer` metadata.
  - **Usage**: Accepts the named parameters `cite` and `footer`.
  - **Example**:
  ```md
  {{</* blockquote cite="www.shawnohare.com" footer="Shawn" */>}}
    There is nothing more beautiful than an elegant mathematical proof.
  {{</* /blockquote */>}}
  ```

- `div`
   - **Description**: This shortcode is provided as a work-around for wrapping
   complex blocks of markdown in div tags. The wrapped text can
   include other shortcodes
   - **Usage**: Identical to the `section` shortcode.
   Accepts the style parameters `class` and `id`.
   If only the positional argument `"end"` is passed, a closing tag
   will be inserted.
   - **Example**: `{{< div class="my-class" >}}` inserts a
   `<div class="my-class">` tag, while
   `{{<div "end" >}}` inserts the closing `</div>` tag.

- `epigraph`
  - **Description**: Create an epigraph with the wrapped text.
  - **Usage**: To include a footer with source attribution, pass in the
  optional named parameters `pre`, `cite`, `post`, `link`. These parameters
  make no styling assumptions, so spacing is important.  A more compactly
  styled epigraph will be used if the `type` parameter is set to `compact`.
  - **Example**:
  ```html
  {{< epigraph pre="Author Writer, " cite="Math is Fun" link='https://www.google.com' >}}
  This is an example of an epigraph with some math
  $ \mathbb N \subseteq \mathbb R $
  to start the beginning of a section.
  {{< /epigraph >}}
  ```

- `marginnote`
  - **Description**: Wrap text to produce a numberless margin note.
  - Usage: `{{< marginnote >}}...{{< /marginnote >}}`
  - **Example**: 
  ```html
  {{< marginnote >}}Some marginnote{{< /marginnote>}}
  ```

- `section`
   - **Description**: This shortcode is provided as a work-around for wrapping
   complex blocks of markdown in section tags. The wrapped text can
   include other shortcodes
   - **Usage**: Accepts the style parameters `class` and `id`.
   If only the positional argument `"end"` is passed, a closing tag
   will be inserted.
   - **Example**: `{{< section class="my-class" >}}` inserts a
   `<section class="my-class">` tag, while
   `{{<section "end" >}}` inserts the closing `</section>` tag.


- `sidenote`
  - **Description**: Wrap text to produce an automatically numbered sidenote.
  - **Usage**: identical to `marginnote`
  `{{< sidenote >}}...{{< /sidenote >}}`
  - **Example**: 
  ```html
  {{< sidenote >}}Some sidenote{{< /sidenote >}}
  ```