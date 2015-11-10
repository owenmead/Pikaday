Pikaday - With Time Picker
========

### Key Config Changes

```javascript
showTime: true
showSeconds: false
use24hour: false
```

### Time support added to [dbushell/Pikaday][david Pika]

This fork allows the user to specify the time along with their date. Done so by adding a couple select inputs to manipulate the date Pikaday is generating.
* Used to set time aspects of date.
* Will not change the currently selected date.
* If no date is selected, will select today. Any of the arguments may be null, and will not affect the date.

Returns the selected date in a string format. If [Moment.js][moment] exists (recommended) then Pikaday can return any format that Moment understands, otherwise you're stuck with JavaScript's default.

`picker.getDate()`

Returns a basic JavaScript `Date` object of the selected day, or `null` if no selection.

`picker.setDate('2015-01-01')`

Set the current selection. This will be restricted within the bounds of `minDate` and `maxDate` options if they're specified. You can optionally pass a boolean as the second parameter to prevent triggering of the onSelect callback (true), allowing the date to be set silently.

`picker.getMoment()`

Returns a [Moment.js][moment] object for the selected date (Moment must be loaded before Pikaday).

`picker.setMoment(moment('14th February 2014', 'DDo MMMM YYYY'))`

Set the current selection with a [Moment.js][moment] object (see `setDate` for details).

### Change current view

`picker.gotoDate(new Date(2014, 1))`

Change the current view to see a specific date. This example will jump to February 2014 ([month is a zero-based index][mdn_date]).

`picker.gotoToday()`

Shortcut for `picker.gotoDate(new Date())`

`picker.gotoMonth(2)`

Change the current view by month (0: January, 1: Februrary, etc).

`picker.nextMonth()`
`picker.prevMonth()`

Go to the next or previous month (this will change year if necessary).

`picker.gotoYear()`

Change the year being viewed.

`picker.setMinDate()`

Update the minimum/earliest date that can be selected.

`picker.setMaxDate()`

Update the maximum/latest date that can be selected.

`picker.setStartRange()`

Update the range start date. For using two Pikaday instances to select a date range.

`picker.setEndRange()`

Update the range end date. For using two Pikaday instances to select a date range.

### Show and hide datepicker

`picker.isVisible()`

Returns `true` or `false`.

`picker.show()`

Make the picker visible.

`picker.adjustPosition()`

Recalculate and change the position of the picker.

`picker.hide()`

Hide the picker making it invisible.

`picker.destroy()`

Hide the picker and remove all event listeners — no going back!

### Internationalization

The default `i18n` configuration format looks like this:

```javascript
i18n: {
    previousMonth : 'Previous Month',
    nextMonth     : 'Next Month',
    months        : ['January','February','March','April','May','June','July','August','September','October','November','December'],
    weekdays      : ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'],
    weekdaysShort : ['Sun','Mon','Tue','Wed','Thu','Fri','Sat']
}
```

You must provide 12 months and 7 weekdays (with abbreviations). Always specify weekdays in this order with Sunday first. You can change the `firstDay` option to reorder if necessary (0: Sunday, 1: Monday, etc). You can also set `isRTL` to `true` for languages that are read right-to-left.


## Extensions

### Timepicker

Pikaday is a pure datepicker. It will not support picking a time of day. However, there have been efforts to add time support to Pikaday.  
See [#1][issue1] and [#18][issue18]. These reside in their own fork.

You can use the work [@owenmead][owenmead] did most recently at [owenmead/Pikaday][owen Pika]  
A more simple time selection approach done by [@xeeali][xeeali] at [xeeali/Pikaday][xeeali Pika] is based on version 1.2.0.  
Also [@stas][stas] has a fork [stas/Pikaday][stas Pika], but is now quite old


## Browser Compatibility

* IE 7+
* Chrome 8+
* Firefox 3.5+
* Safari 3+
* Opera 10.6+

[![browser compatibility](https://ci.testling.com/rikkert/pikaday.png)
](https://ci.testling.com/rikkert/pikaday)


* * *

## Authors

* Owen Mead-Robins [http://www.owenmead.com/][owenmead]

[david Pika]:   https://github.com/dbushell/Pikaday                              "Pikaday"
[owenmead]:     http://owenmead.com/                                             "owenmead.com"
