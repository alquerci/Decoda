# Decoda v3.3.2 #

A lightweight lexical string parser for BBCode styled markup.

## Compatibility ##

Version(s) 3.x are not backwards compatible with 2.9 and lower. The newer versions were completely rewritten as a lexical parser that examines the string stack, where as the older versions were using archaic regex parsing. The newer versions also boast a very powerful filter and hook system, so your old code will need to be changed to support the newer functionality.

## Requirements ##

* PHP 5.2, 5.3

## Contributors ##

* "Marten-Plain" emoticons by Mårten Lundin - http://adiumxtras.com/index.php?a=xtras&xtra_id=6920
* "HTML_BBCodeParser" by Seth Price - http://pear.php.net/package/HTML_BBCodeParser/

## Features ##

* Parses custom code to valid (X)HTML markup
* Setting to make links and emails auto-clickable
* Setting to use shorthand text for links and emails
* Provides Filters to parse markup and custom code
* Provides Hooks to execute during the parsing cycle
* Provides functionality to render complex markup using a template system
* Can censor offensive words
* Can convert smiley faces into images
* Basic support for localized messages
* Supports a wide range of tags
* Fixes incorrectly nested tags by removing the broken/unclosed tags
* Logs errors for validation

## Filters ##

The following filters and supported tags are available.

* Default: b, i, u, s, sup, sub
* Block: align, float, hide, alert, note, div, spoiler, center
* Code: code, var
* Email: email, mail
* Image: image, img
* List: list, olist, li
* Quote: quote
* Text: font, size, color, h1-h6
* Url: url, link
* Video: video

## Hooks ##

The following hooks are available.

* Censor: Censors all words found within config/censored.txt
* Clickable: Converts all non-tag wrapped URLs and emails into clickable links
* Emoticon: Converts all smilies found within config/emoticons.json into emoticon images

## Unsupported ##

* URLs that begin with www will not be converted (intentional)
* Certain videos are not supported as their embed code does not match the URL in the address bar

## Documentation ##

Thorough documentation can be found here: http://milesj.me/code/php/decoda