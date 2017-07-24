[Getting PhD](getting-phd.php)

[Using PhD to render documentation](using-phd.php)

[Getting PhD](getting-phd.php)

------

## Installation

PhD is distributed via an own PEAR channel, `doc.php.net`. Using it is also the most easy way to get it.

## Installation via PEAR

> **Note**:
>
> You need a working [» PEAR installation](http://pear.php.net/manual/en/installation.php).
>
> 

To install the latest version of PhD:

```
$ pear install doc.php.net/phd

... downloading

$ phd --version
PhD Version: 1.0.0-stable
PHP Version: 5.3.3
Copyright(c) 2007-2010 The PHP Documentation Group

```

Installing the PhD Packages:

```
$ pear install doc.php.net/phd_php
Starting to download PhD_PHP-1.0.0.tgz (18,948 bytes)
[...]
install ok: channel://doc.php.net/PhD_PHP-1.0.0

$ pear install doc.php.net/phd_pear
downloading PhD_PEAR-1.0.0.tgz ...
[...]
install ok: channel://doc.php.net/PhD_PEAR-1.0.0

```

That's it!

## Installation from SVN

To get the latest and greatest features that have not been released yet, you can use PhD from SVN.

```
$ svn checkout http://svn.php.net:/repository/phd/trunk phd
... output

pear install package.xml package_generic.xml package_php.xml package_pear.xml 
[...]
install ok: channel://doc.php.net/PhD-1.0.1
install ok: channel://doc.php.net/PhD_Generic-1.0.1
install ok: channel://doc.php.net/PhD_PHP-1.0.1
install ok: channel://doc.php.net/PhD_PEAR-1.0.1
bjori@jessica:/usr/src/php/svn/phd/trunk$ 

$ phd --version
PhD Version: phd-from-svn
PHP Version: 5.3.3-dev
Copyright(c) 2007-2010 The PHP Documentation Group

```

And now you're done.

------

[Getting PhD](getting-phd.php)

[Using PhD to render documentation](using-phd.php)

[Getting PhD](getting-phd.php)