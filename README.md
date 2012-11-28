Alternative autocompletion for Sublime Text 2
=============================================

This plugin adds an autocompletion command to Sublime Text 2 that acts similarly to TextMate:

* Hitting the autocomplete key will attempt to complete the current word by looking at similar words in the current document.

* Hitting the autocomplete key multiple times will cycle through the available words.

* The last autocomplete position is remembered, so you can perform an autocompletion, move the cursor around, move back to where you were, and continue cycling through the completions.

* Candidate completions are selected prioritized by distance to the cursor.

The plugin improves on TextMate in one respect: If no candidates are found, the plugin reverts to using a simple fuzzy, case-insensitive matching algorithm that is similar to Sublime's file/class matching algorithm. For example, typing `appc` might match `ApplicationController`.

Compatibility
-------------

Tested with Sublime Text 2 build 2095 and later. The key bindings described below will work for build 2134 (and onwards, presumably).

Installation using Package Control (simplest)
---------------------------------------------

1. Install the [Package Control plugin](http://wbond.net/sublime_packages/package_control) unless you don't have it already.

2. Open Package Controll and choose "Install Package".

3. Select `alternative_autocompletion`.

Manual installation
-------------------

Drop the entire folder in Sublime's `Packages` folder. You can do this using `git clone` thus:

    $ cd .../Packages  # Whatever the location is

    $ git clone git://github.com/alexstaubo/sublime_text_alternative_autocompletion.git


To map to the tab key it gets a bit more complex to preserve indentation behaviour:

Keyboard mappings
-----------------

The default keyboard settings use the **Escape** key for autocompletion. To use the **tab** key instead you will need to add some complex custom keyboard mappings (Preferences -> "Key Bindings - User"). Copy the bindings found in `Tabs.sublime-keymap`.

Limitations
-----------

Currently does not work with multiple selections.

License
-------

Copyright 2011 Alexander Staubo. MIT license. See `LICENSE` file for license.
