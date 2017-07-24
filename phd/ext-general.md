[DocBook extensions](docbook-extensions.php)

[PEAR specific DocBook extensions](ext-pear.php)

[DocBook extensions](docbook-extensions.php)

------

## General DocBook extensions

The extensions listed here are available in all PhD themes and formats.

## Manual chunking with "phd:chunk" (Attribute)

PhD automatically chooses which sections, chapters or other tags get their own file (chunk) when using a chunked theme. Sometimes the result of this automatism is not optimal and you want to fine-tune it. The attribute "phd:chunk" is offered as solution by PhD.

## Allowed values

*phd:chunk* may have values *true* and *false*. They force the element to be chunked or not.

## Allowed in

*phd:chunk* may be used in every tag that accepts [» db.common.attributes](http://www.docbook.org/tdg5/en/html/ref-elements.html#common.attributes).

## Example

```
<?xml version="1.0" encoding="utf-8"?>
<preface xmlns="http://docbook.org/ns/docbook"
 xmlns:phd="http://www.php.net/ns/phd"
 xml:id="preface"
 phd:chunk="false"
>
 <info>
  <title>Preface</title>
 ..
 </info>
 ..
</preface>
```

## Generating Table Of Contents: <phd:toc> (Tag)

To manually insert a Table Of Contents (TOC) that creates a list of links to children elements of a specified tag.

phd:toc-depth

## Allowed in

** is can be used everywhere ** is allowed.

## Children

You can add a title with **.

## Attributes

| Attribute name | Description                              | Default value |
| -------------- | ---------------------------------------- | ------------- |
| phd:element    | ID of the element whose children shall be linked | *none*        |
| phd:toc-depth  | Depth of the TOC/Number of levels        | *1*           |

------

[DocBook extensions](docbook-extensions.php)

[PEAR specific DocBook extensions](ext-pear.php)

[DocBook extensions](docbook-extensions.php)