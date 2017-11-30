<img src='https://raw.githubusercontent.com/zeroheight/library-symbol-replacer/master/images/cover.png'>

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
* Run the plugin from `Plugins > Library Symbol Replacer > Replace symbols from a new library`
* Select the Library file using the `Choose` dialog
* The plugin will tell you what replacements it thinks it can make
* When the replacements are done, it will also ask you if you want to delete the symbols which have been replaced

### Breaking up a big file
* If you're breaking up a big file, copy and paste some symbols into a different Sketch document
* Make that document a Library ([see Sketch docs if you need help](https://www.sketchapp.com/docs/libraries/adding-libraries))
* Repeat this into as many Libraries as you want
* In your original file, use the plugin to replace your document symbols with the new Library ones

### Multiple files
If you have nested symbols that you want to send to different libraries (e.g. components that contain icons, and you want a separate Components and Icons library) - when you copy your components symbols out of your original file, you'll bring with them the icon symbols that they contain, which would create duplicates (the same icon would become two symbols, one in Components and one in Icons).

To remedy that you can either:

* Run the replacer plugin within your Components library first, to replace all icon symbols by icons from the Icons library. You should make sure that Components doesn't contain any other symbols than the component ones. Then you can run the plugin within your original file.
* or, run the replacer plugin in your original file after transferring out the icons, but before transferring out the components themselves. That way the components will already be linked with the Icons Library's icons, instead of the local ones. If you have circular dependencies between your libraries, this approach might not be feasible.

Overrides should be preserved with either method.

## Issues
* It is currently quite dumb and just uses symbol **names** to match symbols - that's because symbol IDs can be different, depending on how you copy and paste thing around
* Hopefully the overrides should be fairly resilient, but there are a few Sketch bugs I came across while implementing this, so I had to work around those
* It won't work for replacing Library symbols with other Library symbols - this could be a future improvement

## Contact
Get in touch at robin#zeroheight.com, but use @ instead of # if you're not a 🤖

## License
Copyright (c) 2017 Zero Height Limited (zeroheight). See LICENSE.md for further details.
