Metrolook
=========

A skin for MediaWiki

The author of the skin is http://www.pidgi.net/wiki/Main_Page


Compatible with MediaWiki 1.24+

If you would like compatibility with mediawiki 1.24, 1.23, 1.22 or 1.21 please visit 

1.24

https://github.com/paladox2015/Metrolook/tree/MediaWiki-1.24

1.23

https://github.com/paladox2015/Metrolook/tree/MediaWiki-1.23

1.22

https://github.com/paladox2015/Metrolook/tree/MediaWiki-1.22

1.21

https://github.com/paladox2015/Metrolook/tree/MediaWiki-1.21

Please be aware that there are issues in the codes if you see any could you point it out it would help. and there are things like logos already set sorry i will put a setting there.

A working demo of the skin is available at http://pidgi.net/metrolooktest/index.php/Main_Page . This is currently using MediaWiki 1.24wmf18 and version 2.3 of the master branch of the skin.


## Settings

1.24 only

To enable logo

$Logoshow = true;

Default is

$Logoshow = false;

To enable sidebar search bar

$SearchBar = false;

Default is

$SearchBar = true;

## Customizing top bar color

To customise top bar colour add the following to MediaWiki:common.css

and all you need to do is edit background-colour and the top bar should change colour but please remember there is also hover which is when you hover it goes a different colour.

<pre>
/* Top Bar colour and hover colour start */
 
#mw-page-base {
	height: 2.5em;
	background-color: dodgerBlue;
	background-position: bottom left;
	background-repeat: repeat-x;
	/* This image is only a fallback (for IE 6-9), so we do not @embed it. */
	background-image: url('images/page-fade.png');
}
 
div.vectorTabs a:hover {
         background-color: blue;
}
 
div.onhoverbg:hover {
         background-color: blue;
}
 
img.custom3:hover{
            background-color: blue;
}
 
div.vectorMenu:hover h5 a {
           background-color: blue;
}
 
div.vectorMenu h5 a {
        display: inline-block;
	width: 24px;
	height: 2em;
	background-color: dodgerBlue; 
	.background-image-svg('images/arrow-down-icon.svg', 'images/arrow-down-icon.png');
	background-position: 50% 50%; 
	background-repeat: no-repeat;
	.transition(background-position 250ms);
}
div.vectorMenu:hover {
           background-color: blue;
}
 
/* Top Bar colour and hover colour end */
</pre>

## Known Issues

* Mobile view of desktop is not shown correcly.


## Version

3.x.x requires MediaWiki 1.25.

2.x.x requires MediaWiki 1.24.

1.x.x requires MediaWiki 1.23.


## Removed things

Please do not remove this section. it is for things that have been removed and used for if something goes wrong and th eproblem was because it was removed then they can use the things here.

```html
<link href='http://fonts.googleapis.com/css?family=Yanone+Kaffeesatz:700' defer="defer" rel='stylesheet' type='text/css'>
<meta name="msapplication-TileImage" content="http://www.pidgi.net/new/public/images/pidgiwiki.png"/>
<meta name="msapplication-TileColor" content="#BE0027"/>
```
