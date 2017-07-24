[Compiling the PhD guide](render-phd-guide.php)

[DocBook extensions](docbook-extensions.php)

[Using PhD to render documentation](using-phd.php)

------

## Customizing the rendering results

PhD lets you specify a number of options to customize the generated documentation files. The following sections describe some of them.

## Source code highlighter

Part of the documentation of programming languages is source code examples. PhD is able to colorize the source code of many types of source code with the help of *highlighters*.

To utilize syntax highlighting, your opening ** tags need a *role* attribute describing the type of source code. Examples are *php*, *html* and *python*.

> **Note**:
>
> PhD currently only highlights the code if it is embedded in a *CDATA* section.
>
> 

**Example #1 A programlisting tag with a role**

```
<programlisting role="php"><![CDATA[
<?php
echo "Hello world!";
?>
```

```
]]></programlisting>
```

By default, PhD uses the source code highlighter that is built into PHP itself. It is only able to highlight PHP code and nothing else.

If your documentation contains other types of source code or markup, like XML, HTML, Javascript or any other language, you should try the [» GeSHi](http://qbnz.com/highlighter/) highlighter that is shipped with PhD:

1. Install GeSHi from the MediaWiki PEAR channel:

   ```
   $ pear channel-discover mediawiki.googlecode.com/svn
   $ pear install mediawiki/geshi
   ```

2. Use the GeSHi syntax highlighting class when rendering your documentation:

   ```
   $ phd -g 'phpdotnet\phd\Highlighter_GeSHi' -d phd-guide.xml
   ```

   ​

If you have GeSHi version 1.1.x installed, you should use the *phpdotnet\phd\Highlighter_GeSHi11x* highlighter, which is adapted to GeSHi's new API.

Apart from using the highlighter shipped with PhD, you can [build your own highlighters](phd-extension-highlighter.php).

------

[Compiling the PhD guide](render-phd-guide.php)

[DocBook extensions](docbook-extensions.php)

[Using PhD to render documentation](using-phd.php)