[General DocBook extensions](ext-general.php)

[Extending PhD](phd-extension.php)

[DocBook extensions](docbook-extensions.php)

------

## PEAR specific DocBook extensions

The DocBook extensions listed here are only available when using a PEAR theme.

## Linking to PEAR API documentation: <phd:pearapi> (Tag)

A large part of the PEAR manual is about packages and how to use them. Package authors often find they need to link to the API documentation of a specific method, variable or class of their package. To ease the linking process, the ** tag was introduced.

You can let PhD automatically create the link text by just closing the tag, or specify the tag text via the tag's content.

## Package links

*phd:package* name is put into the attribute, any text:

```
<phd:pearapi phd:package="HTML_QuickForm"/>
<phd:pearapi phd:package="HTML_QuickForm">some text</phd:pearapi>
```

[» HTML_QuickForm](http://pear.php.net/package/HTML_QuickForm/docs/latest/li_HTML_QuickForm.html) [» some text](http://pear.php.net/package/HTML_QuickForm/docs/latest/li_HTML_QuickForm.html)

## Class links

Class name as *phd:linkend* attribute value.

```
<phd:pearapi phd:package="HTML_QuickForm" phd:linkend="HTML_QuickForm_element"/>
<phd:pearapi phd:package="HTML_QuickForm" phd:linkend="HTML_QuickForm_element">some text</phd:pearapi>
```

[» HTML_QuickForm_element](http://pear.php.net/package/HTML_QuickForm/docs/latest/HTML_QuickForm/HTML_QuickForm_element.html) [» some text](http://pear.php.net/package/HTML_QuickForm/docs/latest/HTML_QuickForm/HTML_QuickForm_element.html)

## Class method links

Class and method name as *phd:linkend* text, separated by a double colon.

```
<phd:pearapi phd:package="HTML_QuickForm" phd:linkend="HTML_QuickForm_element::setName"/>
<phd:pearapi phd:package="HTML_QuickForm" phd:linkend="HTML_QuickForm_element::setName">some text</phd:pearapi>
```

[» HTML_QuickForm_element::setName()](http://pear.php.net/package/HTML_QuickForm/docs/latest/HTML_QuickForm/HTML_QuickForm_element.html#methodsetName) [» some text](http://pear.php.net/package/HTML_QuickForm/docs/latest/HTML_QuickForm/HTML_QuickForm_element.html#methodsetName)

## Class variable links

Class and variable name as *phd:linkend* text, separated by a double colon and a dollar sign before the variable name.

```
<phd:pearapi phd:package="Net_Geo" phd:linkend="Net_Geo::$cache_ttl"/>
<phd:pearapi phd:package="Net_Geo" phd:linkend="Net_Geo::$cache_ttl">some text</phd:pearapi>
```

[» Net_Geo::$cache_ttl](http://pear.php.net/package/Net_Geo/docs/latest/Net_Geo/Net_Geo.html#var$cache_ttl) [» some text](http://pear.php.net/package/Net_Geo/docs/latest/Net_Geo/Net_Geo.html#var$cache_ttl)

------

[General DocBook extensions](ext-general.php)

[Extending PhD](phd-extension.php)

[DocBook extensions](docbook-extensions.php)