[Using PhD to render documentation](using-phd.php)

[Compiling the PhD guide](render-phd-guide.php)

[Using PhD to render documentation](using-phd.php)

------

## Rendering the PHP Documentation Sources

> # Getting the PHP Documentation Sources
>
> To get the PHP documentation sources, simply [» check them out from SVN](http://wiki.php.net/doc/scratchpad/howto/checkout) with the following command.
>
> ```
> $ svn co http://svn.php.net/repository/phpdoc/modules/doc-en phpdoc
> ... output
>
> ```
>
> To prepare the documentation, **cd** to the phpdoc directory, and run configure.php.
>
> ```
> $ php doc-base/configure.php
> ```
>
> This process will generate a .manual.xml file in the current directory, which is what we need for building the docs. Now we're ready to proceed with running PhD to generate the PHP docs.

To quickly become familiar with using PhD, you can download the PHP documentation sources and render those.Running PhD to render the docs is surprisingly simple, so we'll start with that.

```
$ phd -d doc-base/.manual.xml -P PHP
... status messages

```

After a running for a few moments, PhD will generate all the output formats of the PHP Package into *output/*.

So now that you've seen the fruits of your labor, let's take a closer look at PhD and see what capabilities are available to us.

```
$ phd --help
PhD version: 1.1.6
Copyright(c) 2007-2013 The PHP Documentation Group

  -v
  --verbose <int>            Adjusts the verbosity level
  -f <formatname>
  --format <formatname>      The build format to use
  -P <packagename>
  --package <packagename>    The package to use
  -I
  --noindex                  Do not index before rendering but load from cache
                             (default: false)
  -M
  --memoryindex              Do not save indexing into a file, store it in memory.
                             (default: false)
  -r
  --forceindex               Force re-indexing under all circumstances
                             (default: false)
  -t
  --notoc                    Do not rewrite TOC before rendering but load from
                             cache (default: false)
  -d <filename>
  --docbook <filename>       The Docbook file to render from
  -x
  --xinclude                 Process XML Inclusions (XInclude)
                             (default: false)
  -p <id[=bool]>
  --partial <id[=bool]>      The ID to render, optionally skipping its children
                             chunks (default to true; render children)
  -s <id[=bool]>
  --skip <id[=bool]>         The ID to skip, optionally skipping its children
                             chunks (default to true; skip children)
  -l
  --list                     Print out the supported packages and formats
  -o <directory>
  --output <directory>       The output directory (default: .)
  -F filename
  --outputfilename filename  Filename to use when writing standalone formats
                             (default: <packagename>-<formatname>.<formatext>)
  -L <language>
  --lang <language>          The language of the source file (used by the CHM
                             theme). (default: en)
  -c <bool>
  --color <bool>             Enable color output when output is to a terminal
                             (default: true)
  -C <filename>
  --css <filename>           Link for an external CSS file.
  -g <classname>
  --highlighter <classname>  Use custom source code highlighting php class
  -V
  --version                  Print the PhD version information
  -h
  --help                     This help
  -e <extension>
  --ext <extension>          The alternative filename extension to use,
                             including the dot. Use 'false' for no extension.
  -S <bool>
  --saveconfig <bool>        Save the generated config (default: false).

  -Q
  --quit                     Don't run the build. Use with --saveconfig to
                             just save the config.
  -k
  --packagedir               Use an external package directory.


Most options can be passed multiple times for greater effect.

```

As you can see, there are plenty of options to look into in PhD. The most important options are those which allow you to select a format and package to output your documentation to.

```
$ phd --list
Supported packages:
        Generic
                xhtml
                bigxhtml
                manpage
        IDE
                xml
                funclist
                json
                php
                phpstub
        PEAR
                xhtml
                bigxhtml
                php
                chm
                tocfeed
        PHP
                xhtml
                bigxhtml
                php
                howto
                manpage
                pdf
                bigpdf
                kdevelop
                chm
                tocfeed
                epub
                enhancedchm

```

> **Note**:
>
> The format packages are provided by separate PEAR packages (doc.php.net/PhD_Generic, doc.php.net/PhD_IDE, doc.php.net/PhD_PEAR and doc.php.net/PhD_PHP) where only the Generic is installed by default.
>
> 

You can tell by the output of the *--list* option that PhD can also be used to render the docs as a PDF file, or as Unix Man Pages.

To select a format and package, you must use the *-f [formatName]* and *-P [packageName]* options.

```
$ phd -f manpage -P PHP -d .manual.xml
```

This command will output the documentation for PHP functions in the Unix Man page format.

------

[Using PhD to render documentation](using-phd.php)

[Compiling the PhD guide](render-phd-guide.php)

[Using PhD to render documentation](using-phd.php)