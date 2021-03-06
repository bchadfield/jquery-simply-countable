# jQuery Simply Countable plugin

Fork of the original jQuery plugin to now provide a character counter for editable html tags. Works when typing and pasting text using the mouse.
Also provides the 

Original version:
* version - 0.5.0
* homepage - [http://github.com/aaronrussell/jquery-simply-countable/](http://github.com/aaronrussell/jquery-simply-countable/)
* author - [Aaron Russell](http://www.aaronrussell.co.uk)

This version:
* homepage - [http://github.com/bchadfield/jquery-simply-countable/](http://github.com/bchadfield/jquery-simply-countable/)
* author - [Ben Chadfield](http://chadfield.org)

## Usage

Simple usage:

    $('#my_textarea').simplyCountable();

Advanced usage:

    $('#my_textarea').simplyCountable({
        counter:            '#counter',
        countType:          'characters',
        maxCount:           140,
        operator:			'<=',
        strictMax:          false,
        safeClass:          'safe',
        overClass:          'over',
        thousandSeparator:  ',',
        onOverCount:        function(count, countable, counter){},
        onSafeCount:        function(count, countable, counter){},
        onMaxCount:         function(count, countable, counter){}
    });

## Options

* `counter` - A jQuery selector to match the 'counter' element. Defaults to `#counter`.
* `countType` - Select whether to count `characters` or `words`. Defaults to `characters`.
* `maxCount` - The maximum character (or word) count of the text input or textarea. Defaults to `140`.
* `operator` - Part of the equation `countType` `operator` `maxCount`. This replaces the previous `up` or `down` option. Defaults to `<=`.
* `strictMax` - Prevents the user from being able to exceed the `maxCount`. Defaults to `false`.
* `safeClass` - The CSS class applied to the counter element when it is within the maxCount figure. Defaults to `safe`.
* `overClass` - The CSS class applied to the counter element when it exceeds the maxCount figure. Defaults to `over`.
* `thousandSeparator` - The separator for multiples of 1,000. Set to `false` to disable. Defaults to `,`.
* `onOverCount` - Callback function called when counter goes over `maxCount` figure.
* `onSafeCount` - Callback function called when counter goes below `maxCount` figure.
* `onMaxCount` - Callback function called when in `strictMax` mode and counter hits `maxCount` figure.

## License

Dual licensed under the [MIT](http://www.opensource.org/licenses/mit-license.php) and [GPL](http://www.opensource.org/licenses/gpl-license.php) licenses.

Copyright (c) 2009-2013 [Aaron Russell](http://www.aaronrussell.co.uk).