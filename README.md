Metrolook
=========

A skin for MediaWiki

The author of the skin is http://www.pidgi.net/wiki/Main_Page


Compatible with MediaWiki 1.25+

If you would like compatibility with mediawiki 1.24, 1.23, 1.22 or 1.21 please visit 

1.24

https://github.com/paladox2015/Metrolook/tree/REL1_24

1.23

https://github.com/paladox2015/Metrolook/tree/REL1_23

1.22

https://github.com/paladox2015/Metrolook/tree/REL1-22

1.21

https://github.com/paladox2015/Metrolook/tree/REL1_21

Please be aware that there are issues in the codes if you see any could you point it out it would help. and there are things like logos already set sorry i will put a setting there.

A working demo of the skin is available at http://www.pidgi.net/metrolooktest/index.php/Main_Page . This is currently using MediaWiki 1.25wmf12 and version 3.0 beta 13 of the master branch of the skin.

## Installation

Download and save in skins/ folder 

Add this to LocalSettings.php

<pre>
require_once "$IP/skins/Metrolook/Metrolook.php";
</pre>

## Settings

1.25 only

To enable logo

$logo = true;

Default is

$logo = false;

To enable sidebar search bar

$SearchBar = false;

Default is

$SearchBar = true;


To turn it off

$DownArrow = false;

Default is

$DownArrow = true;

To turn it off

$Line = false;

Default is

$Line = true;

to change link

$link1 = false;

$image1 = false;

$url1 = link of website;

$picture1 = image link;

Default is

$link1 = true;

$image1 = true;

to change link

$link2 = false;

$image2 = false;

$url2 = link of website;

$picture2 = image link;

Default is

$link2 = true;

$image2 = true;

to change link

$link3 = false;

$image3 = false;

$url3 = link of website;

$picture3 = image link;

Default is

$link3 = true;

$image3 = true;

to change link

$link4 = false;

$image4 = false;

$url4 = link of website;

$picture4 = image link;

Default is

$link4 = true;

$image4 = true;

Default is

$link5 = false;

$image5 = false;

to turn it on

$link5 = true;

$image5 = true;

$url5 = link of website;

$picture5 = image link;

Default is

$link6 = false;

$image6 = false;

to turn it on

$link6 = true;

$image6 = true;

$url6 = link of website;

$picture6 = image link;

To disable upload Button on top bar please add this to LocalSettings.php

$UploadButton = false;

Default is

$UploadButton = true;

## Customizing top bar color

To customise top bar colour ether add it to theme.css which is in metrolook skin folder or MediaWiki:Metrolook.css from web browser.

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
    min-width: auto;
}
@media only screen and (min-device-width : 768px) and (max-device-width : 1024px) and (orientation : portrait) {
#mw-page-base {
    height: 2.5em;
    background-color: dodgerBlue;
    background-position: bottom left;
    background-repeat: repeat-x;
    /* This image is only a fallback (for IE 6-9), so we do not @embed it. */
    background-image: url('images/page-fade.png');
    min-width:65em;
}
}
@media only screen and (min-device-width : 768px) and (max-device-width : 1024px) and (orientation : landscape) {
#mw-page-base {
    height: 2.5em;
    background-color: dodgerBlue;
    background-position: bottom left;
    background-repeat: repeat-x;
    /* This image is only a fallback (for IE 6-9), so we do not @embed it. */
    background-image: url('images/page-fade.png');
    min-width:65em;
}
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

div.vectorMenu ul {
        position: absolute;
        background-color: white;
        border: solid 2px dodgerBlue;
        border-top-width: 0;
        list-style-type: none;
        list-style-image: none;
        padding: 0;
        padding-top:5px;
        margin: 0;
        margin-left: -6px;
        text-align: left;
}

/* Top Bar colour and hover colour end */

</pre>

## Known Issues

* Mobile view of desktop is not shown correcly.

## Support comming soon

Note plans may change.

Comming soon support for 

* MediaWiki 1.21

## Version

3.x.x requires MediaWiki 1.25.

2.x.x requires MediaWiki 1.24.

1.x.x requires MediaWiki 1.23.

0.3.x requires MediaWiki 1.22.


## Removed things

Please do not remove this section. it is for things that have been removed and used for if something goes wrong and th eproblem was because it was removed then they can use the things here.

```html
<link href='http://fonts.googleapis.com/css?family=Yanone+Kaffeesatz:700' defer="defer" rel='stylesheet' type='text/css'>
<meta name="msapplication-TileImage" content="http://www.pidgi.net/new/public/images/pidgiwiki.png"/>
<meta name="msapplication-TileColor" content="#BE0027"/>
```

```html
				<?php if ( $Logoshow ): ?>
				<div id="p-logo" role="banner"><a style="background-image: url(<?php
					$this->text( 'logopath' )
					?>);" href="<?php
					echo htmlspecialchars( $this->data['nav_urls']['mainpage']['href'] )
					?>" <?php
					echo Xml::expandAttributes( Linker::tooltipAndAccesskeyAttribs( 'p-logo' ) )
					?>></a></div>
					<?php else: ?>
				<?php endif; ?>
```
