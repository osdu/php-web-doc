[Rendering the PHP Documentation Sources](render-phpdoc.php)

[Customizing the rendering results](render-custom.php)

[Using PhD to render documentation](using-phd.php)

------

## Compiling the PhD guide

The PhD guide is this manual you are reading currently. It lives in PhD's SVN repository under docs/phd-guide/phd-guide.xml. If you installed PhD from SVN, you already have it. Otherwise, get it:

```
$ svn checkout http://svn.php.net:/repository/phd/trunk/docs/phd-guide
U phd/docs/phd-guide/phd-guide.xml

```

Now you have everything you need. Just type

```
$ cd phd/docs/phd-guide/
$ phd -f bigxhtml -d phd-guide.xml

```

There should be an .html file in the directory now. View it with a browser!

That's all to say. This way you can render your own docbook files, too.

------

[Rendering the PHP Documentation Sources](render-phpdoc.php)

[Customizing the rendering results](render-custom.php)

[Using PhD to render documentation](using-phd.php)