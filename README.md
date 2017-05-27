# osrsbox-tooltips
## An Old School Runescape (OSRS) Tooltip library

This repository is a library for creating Old School RuneScape (OSRS) tooltips to enhance user experience on fan websites. The repository hosts the files necessary to implement OSRS tooltips on web pages. The project is based on World of Warcraft (WOW) tooltips - primarily the [WOWhead tooltips](http://www.wowhead.com/tooltips) that are used on the WOWhead website and other WOW fan sites. You can see a more thorough working demo of WOWhead tootips [here](http://wow.zamimg.com/widgets/power/demo.html).

## OSRS Tooltip Example

The OSRS tooltip library provide default support for providing tooltips to:

1. Text: usually item names
2. Images: usually a thumbnail picture on an image

The image below shows an example of tooltips for the Rune platebody (g) and the Rune platelegs (g). The first tooltip is hoverable text. You will notice the unique style of the link, with a gold colour and surrounded by [square brackets]. This makes it easy to distinguish text items with tooltips. The second tooltip is a hoverable image. This method does not include any identifiable design to state whether it is a tooltip - however, should be used when there is no room to include any text.

![Sample of OSRS tooltips when user hovers over image of an OSRS item](docs\sample_img.png)

## Usage Example

OSRS tooltips are pretty simple to use. The process requires two main additions to your web page: 1) Including the JavaScript and CSS code in your web page header; and 2) Including an HTML in your web page body to display a text or image which is used to display the actual tooltip when hovered.

### 1) Include JavaScript and CSS style sheet in the web page header

The JavaScript code (osrsbox-tooltips.js) needs to be included the HTML source code header for the web page when you want to use OSRS tooltips.

``` html
<script type="text/javascript" src="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.js"></script>
```

The CSS style code (osrsbox-tooltips.css) also needs to be included the HTML source code header for the web page when you want to use OSRS tooltips.

```html
<link rel="stylesheet" type="text/css" href="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.css">
```

The following code provides a full working example of a header with links to the the JavaScript and CSS files hosted on osrsbox.com:

```html
<head>
	<link rel="stylesheet" type="text/css" href="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.css">
	<script type="text/javascript" src="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.js"></script>
</head>
```

### 2) Include HTML element to show tooltip

Once the OSRS tooltip library has been included in the header we can create HTML elements which have tooltips when a user hovers their mouse over the element. The OSRS tooltip library provide default support for providing tooltips to:

1. Text: usually item names
2. Images: usually a thumbnail picture on an image

Some code below indicates the use of each method of displaying OSRS tooltips.

Text example:

```html
<div class="tooltip">
	<span class="osrs-tooltip" id='2615' title='Please wait ...'>[Rune platebody (g)]</span>
</div><!-- /.tooltip -->
```
Image example:

``` html
<div class="tooltip">
	<span class="osrs-tooltip" id='2617' title='Please wait ...'><img class="" height="32" width="32" src="http://osrsbox.com/osrsbox-db/items-icons/2/2617.png"></span>
</div><!-- /.tooltip -->
```

### Full working example

Sometimes code snippets can be difficult to understand or implement. Therefore, the following HTML code is a full working example of how to use OSRS tooltips on a web page. This is barebones example with minimal page formatting and style. 

Code includes a hoverable text in the form of an item name, as well as a hoverable thumbnail image example. 

```html
<!DOCTYPE html>
<html>
<head>
	<title>OSRSBOX | Simple HTML Example using OSRS Tooltips by PH01L</title>
    <!-- External links to osrsbox-tooltip library (JS and CSS) -->
	<link href="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.css" rel="stylesheet" type="text/css">
	<script src="http://osrsbox.com/osrsbox-tooltips/osrsbox-tooltips.js" type="text/javascript">
	</script>
</head>
<body>
    <div class="tooltip">
		<span class="osrs-tooltip" id='2615' title='Please wait ...'>[Rune platebody (g)]</span>
	</div><!-- /.tooltip -->
	<div class="tooltip">
		<span class="osrs-tooltip" id='2617' title='Please wait ...'><img class="" height="32" width="32" src="http://osrsbox.com/osrsbox-db/items-icons/2/2617.png"></span>
	</div><!-- /.tooltip -->
</body>
</html>
```

# TODO

Cover connection to RESTful API

Link to projects using OSRS tooltips

