Pikaday - With Time Picker
========

### Key Config Changes

```javascript
showTime: true
showSeconds: false
use24hour: false
defaultTime: '00:00:00'
hourStep: 1
minuteStep: 1
secondStep: 1
```

### Time support added to [dbushell/Pikaday][david Pika]

This fork allows the user to specify the time along with their date. Done so by adding a couple select inputs to manipulate the date Pikaday is generating.
* Used to set time aspects of date.
* Will not change the currently selected date.
* If no date is selected, will select today. Any of the arguments may be null, and will not affect the date.


## Authors

* Owen Mead-Robins [http://www.owenmead.com/][owenmead]

[david Pika]:   https://github.com/dbushell/Pikaday                              "Pikaday"
[owenmead]:     http://owenmead.com/                                             "owenmead.com"
