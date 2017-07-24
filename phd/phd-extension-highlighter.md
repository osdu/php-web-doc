[Extending PhD](phd-extension.php)

[Links](links.php)

[Extending PhD](phd-extension.php)

------

## Writing an own syntax highlighter

A syntax highlighter for PhD is nothing more than a simple PHP class that has two methods, a *factory* and *highlight*.

*factory* is static and takes the format name (i.e. *pdf*, *xhtml*, *troff*) as only parameter. It returns the highlighter instance object for the given format. The method is called for each output format the documentation is rendered to.

*highlight* takes three parameters, *text*, *role* and *format*. It is called whenever a piece of source code needs to be highlighted and expects the highlighted source code to be returned in whatever format the current rendering format is expected to be.

Take a look at the provided highlighters, *phpdotnet\phd\Highlighter*, *phpdotnet\phd\Highlighter_GeSHi* and *phpdotnet\phd\Highlighter_GeSHi11x*. They will serve as good examples how to implement your own highlighter.

Once you wrote your custom source code highlighting class, it's time to [try it out](render-custom.php#render-custom-highlighter).

------

[Extending PhD](phd-extension.php)

[Links](links.php)

[Extending PhD](phd-extension.php)