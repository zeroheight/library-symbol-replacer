<img src='./images/cover.png'>

## Overview
Replace symbols in the current document with symbols from a Library.

Sketch 47 sees the introduction of Libraries, but migrating existing files to use Library symbols is one of the first big headaches. This plugin aims to help with that by allowing you to replace symbols in the current document with symbols from a Library document - maintaining overrides where possible.

N.B. the plugin currently uses symbol name to work out what to replace with what, so be careful of any conflicts.

## Installation
**[Download](https://api.sketchpacks.com/v1/plugins/com.zeroheight.library-symbol-replacer/download)**, unzip and double click the `.sketchplugin`

or

<a href="https://sketchpacks.com/zeroheight/library-symbol-replacer/install">
	<img width="160" height="41" src="http://sketchpacks-com.s3.amazonaws.com/assets/badges/sketchpacks-badge-install.png" >
</a>

## Usage
### Using the plugin
* Open a document where you want to replace symbols with Library symbols
* Run the plugin from `Plugins > Library Symbol Replacer > Replace symbols from Library`
* Select the Library file using the `Choose` dialog
* The plugin will tell you what replacements it thinks it can make
* When the replacements are done, it will also ask you if you want to delete the symbols which have been replaced

### Breaking up a big file
* If you're breaking up a big file, copy and paste some symbols into a different Sketch document
* Make that document a Library ([see Sketch docs if you need help](https://www.sketchapp.com/docs/libraries/adding-libraries))
* Repeat this into as many Libraries as you want
* In your original file, use the plugin to replace your document symbols with the new Library ones

## Issues
* It is currently quite dumb and just uses symbol **names** to match symbols - that's because symbol IDs can be different, depending on how you copy and paste thing around
* Hopefully the overrides should be fairly resilient, but there are a few Sketch bugs I came across while implementing this, so I had to work around those
* It won't work for replacing Library symbols with other Library symbols - this could be a future improvement

## Contact
Get in touch at robin#zeroheight.com, but use @ instead of # if you're not a 🤖

## License
Copyright (c) 2017 Zero Height Limited (zeroheight). See LICENSE.md for further details.
