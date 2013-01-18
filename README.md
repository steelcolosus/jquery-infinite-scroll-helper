jQuery Infinite Scroll Helper
=============================

A lightweight implementation of the infinite scroll mechanic.  By providing two essential callbacks, `loadMore` and `doneLoading`, the jQuery Infinite Scroll Helper plugin makes it a breeze to add infinite scrolling functionality to your page.


Options
-------

### bottomBuffer ###
_(integer)_ The number of pixels from the bottom of the window in which the `loadMore` function should be invoked.  The default is 0.

### doneLoading ###
_(function)_ A callback function that must return `true` or `false`, depending on whether loading has completed.

### interval
_(integer)_ The interval, in milliseconds, that the doneLoading callback will be called by the plugin.  The default is 300.

### loadMore ###
_(function)_ A callback function that is invoked when the scrollbar eclipses the bottom threshold of the element.

### loadingClass ###
_(string)_ The class name that will be applied to the element when `loadMore` is called. It is removed once `doneLoading` returns `true`.  The default is `loading`.

Methods
-------

### destroy ###
Destroys the plugin instance, removing all internal listeners and nullifying any external references.

	$(selector).infiniteScrollHelper('destroy');


Usage
------

	$('#my-element-to-watch').infiniteScrollHelper({
		loadMore: function(page) {
			// load some data, parse some data
		},

		doneLoading: function() {
			// return true if you are done doing your thing, false otherwise
			return false;
		}
	});


Dependencies
------------

* jQuery 1.7.0+


Changelog
---------

### 1.0.3
* Changing details in manifest file
* Doc updates

### 1.0.2
* Fixed manifest file keyword error

### 1.0.1
* Regenerated minified/production script to match development version

### 1.0.0
* Initial Release