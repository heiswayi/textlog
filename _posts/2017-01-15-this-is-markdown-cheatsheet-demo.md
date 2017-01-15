---
layout: post
title: This is markdown cheatsheet demo
tags: [Demo, Markdown]
---

# Typography

## Headings

Headings from `H1` to `H6` are constructed with a `#` for each level.

``` markdown
# H1 Heading (suitable for site use)
## H2 Heading (suitable for site use)
### H3 Heading (in blog post, best to start with this one down to H5)
#### H4 Heading
##### H5 Heading
###### H6 Heading
```

Output:

# H1 Heading (suitable for site use)

## H2 Heading (suitable for site use)

### H3 Heading (in blog post, best to start with this one down to H5)

#### H4 Heading

##### H5 Heading

###### H6 Heading

## Body Copy

Body copy written as normal, plain text will be wrapped with `<p></p>` tags in the rendered HTML.

``` markdown
Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus. Et legere ocurreret pri, animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex, soluta officiis concludaturque ei qui, vide sensibus vim ad.
```

Output:

Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus. Et legere ocurreret pri, animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex, soluta officiis concludaturque ei qui, vide sensibus vim ad.

## Emphasis

### Bold

For emphasizing a snippet of text with a heavier font-weight.

The following snippet of text is **rendered as bold text**.

``` markdown
**rendered as bold text**
```

Output:

**rendered as bold text**

### Italics

For emphasizing a snippet of text with italics.

The following snippet of text is _rendered as italicized text_.

``` markdown
_rendered as italicized text_
```

Output:

_rendered as italicized text_

### Strikethrough

In GFM you can do strikethroughs.

``` markdown
~~Strike through this text.~~
```

Output:

~~Strike through this text.~~

## Blockquotes

For quoting blocks of content from another source within your document.

Add `>` before any text you want to quote.

``` markdown
> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.
```

Output:

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.

## Lists

### Unordered

A list of items in which the order of the items does not explicitly matter.

You may use any of the following symbols to denote bullets for each list item:

```markdown
* valid bullet
- valid bullet
+ valid bullet
```

For example:

``` markdown
+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Integer molestie lorem at massa
+ Facilisis in pretium nisl aliquet
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at
+ Faucibus porta lacus fringilla vel
+ Aenean sit amet erat nunc
+ Eget porttitor lorem
```

Output:

+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Integer molestie lorem at massa
+ Facilisis in pretium nisl aliquet
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Vestibulum laoreet porttitor sem
  - Ac tristique libero volutpat at
+ Faucibus porta lacus fringilla vel
+ Aenean sit amet erat nunc
+ Eget porttitor lorem

### Ordered

A list of items in which the order of items does explicitly matter.

``` markdown
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel
7. Aenean sit amet erat nunc
8. Eget porttitor lorem
```

Output:

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel
7. Aenean sit amet erat nunc
8. Eget porttitor lorem

**TIP**: If you just use `1.` for each number, GitHub will automatically number each item. For example:

``` markdown
1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
1. Eget porttitor lorem
```

Output:

1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
1. Eget porttitor lorem


## Code

### Inline code

Wrap inline snippets of code with `` ` ``.

```
For example, `DisplayHelloWorld()` should be wrapped as "inline".
```

Output:

For example, `DisplayHelloWorld()` should be wrapped as "inline".


### Indented code

Or indent several lines of code by at least four spaces, as in:

```
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

Output:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code


### Block code "fences"

Use "fences"  ```` ``` ```` to block in multiple lines of code.

<pre>
```html
Sample text here...
```
</pre>

```
Sample text here...
```

### Syntax highlighting

GFM, or "GitHub Flavored Markdown" also supports syntax highlighting. To activate it, simply add the file extension of the language you want to use directly after the first code "fence", ` ``` js `, and syntax highlighting will automatically be applied in the rendered HTML. For example, to apply syntax highlighting to JavaScript code:

<pre>
```javascript
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
</pre>

Output:

```javascript
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```

Output (in HTML):

```xml
<div class="highlight"><pre><span class="nx">grunt</span><span class="p">.</span><span class="nx">initConfig</span><span class="p">({</span>
  <span class="nx">assemble</span><span class="o">:</span> <span class="p">{</span>
    <span class="nx">options</span><span class="o">:</span> <span class="p">{</span>
      <span class="nx">assets</span><span class="o">:</span> <span class="s1">'docs/assets'</span><span class="p">,</span>
      <span class="nx">data</span><span class="o">:</span> <span class="s1">'src/data/*.{json,yml}'</span><span class="p">,</span>
      <span class="nx">helpers</span><span class="o">:</span> <span class="s1">'src/custom-helpers.js'</span><span class="p">,</span>
      <span class="nx">partials</span><span class="o">:</span> <span class="p">[</span><span class="s1">'src/partials/**/*.{hbs,md}'</span><span class="p">]</span>
    <span class="p">},</span>
    <span class="nx">pages</span><span class="o">:</span> <span class="p">{</span>
      <span class="nx">options</span><span class="o">:</span> <span class="p">{</span>
        <span class="nx">layout</span><span class="o">:</span> <span class="s1">'default.hbs'</span>
      <span class="p">},</span>
      <span class="nx">files</span><span class="o">:</span> <span class="p">{</span>
        <span class="s1">'./'</span><span class="o">:</span> <span class="p">[</span><span class="s1">'src/templates/pages/index.hbs'</span><span class="p">]</span>
      <span class="p">}</span>
    <span class="p">}</span>
  <span class="p">}</span>
<span class="p">};</span>
</pre></div>
```

## Links

### Basic link

```markdown
[Assemble](http://assemble.io)
```

Output (hover over the link, there is no tooltip):

[Assemble](http://assemble.io)

Output (in HTML):

```html
<a href="http://assemble.io">Assemble</a>
```

### Add a title

```markdown
[Upstage](https://github.com/upstage/ "Visit Upstage!")
```

Output (hover over the link, there should be a tooltip):

[Upstage](https://github.com/upstage/ "Visit Upstage!")

Output (in HTML):

```html
<a href="https://github.com/upstage/" title="Visit Upstage!">Upstage</a>
```

### Named Anchors

Named anchors enable you to jump to the specified anchor point on the same page. For example, each of these chapters:

```markdown
# Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)
```

will jump to these sections:

```markdown
## Chapter 1 <a id="chapter-1"></a>
Content for chapter one.

## Chapter 2 <a id="chapter-2"></a>
Content for chapter one.

## Chapter 3 <a id="chapter-3"></a>
Content for chapter one.
```
**NOTE** that specific placement of the anchor tag seems to be arbitrary. They are placed inline here since it seems to be unobtrusive, and it works.

# Horizontal Rules

The HTML `<hr>` element is for creating a "thematic break" between paragraph-level elements. In markdown, you can create a `<hr>` with any of the following:

* `___`: three consecutive underscores
* `---`: three consecutive dashes
* `***`: three consecutive asterisks

Output:

___

---

***

# Tables

Tables are created by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned.

```markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

Output:

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

### Right aligned text

Adding a colon on the right side of the dashes below any heading will right align text for that column.

```markdown
| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

Output:

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

# Images

Images have a similar syntax to links but include a preceding exclamation point.

```markdown
![Minion](http://octodex.github.com/images/minion.png)
```

Output:

![Minion](http://octodex.github.com/images/minion.png)

or

```markdown
![Alt text](http://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")
```

Output:

![Alt text](http://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

```markdown
![Alt text][id]
```

Output:

![Alt text][id]

With a reference later in the document defining the URL location:

```markdown
[id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat"
```

[id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat"
