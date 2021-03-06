## Finite-Countdown

A front-end countdown plugin that reflects the difference to an ending-time regardless of a user's local timezone.

### Install

```
npm-install "finite-countdown"
```

### Usage

```
var finiteCountdown = require("finite-countdown");

// ending-time as a valid DateString
var end = "2014/11/25 13:00:00";

// additional options
var opts = {
  timezone: "America/New_York", // timezone in context of the ending-time
  selector: ".countdown",       // jquery selector for the countdown's container
  format: "dd:hh:mm:ss",        // remaining time display format
  delimiter: ":",               // delimiting character
  show_units: false,            // use unit strings instead of delimiter
  remove_on_end: false          // remove countdown from the page upon completion
};

$(function() {

  // start and display the countdown
  finiteCountdown(end, opts);

});

```

### Defaults

For supported Timezones see [Moment Timezone](http://momentjs.com/timezone/)
```
defaults =
  selector: ".countdown"
  timezone: "America/Los_Angeles"
  format: "hh:mm:ss"
  delimiter: ":"
  show_units: false
  remove_on_end: false
```

### Format

| Unit | Token | Output |
| ---- | ----- | ------ |
| **Days** | d | 0 1 ... 364 365  |
|      | dd    | 00 01 ... 364 365 |  
| **Hours** | h | 0 1 ... 22 23 |
|      | hh    | 00 01 ... 22 23 |
| **Minutes** | m | 0 1 ... 58 59 |
|      | mm    | 00 01 ... 58 59 |
| **Seconds** | s | 0 1 ... 58 59 |
|      | ss    | 00 01 ... 58 59 |

### Dependencies

- [Moment.js](http://momentjs.com/) - Parse, validate, manipulate, and display dates in javascript.
- [Moment Timezone](http://momentjs.com/timezone/) - Parse and display dates in any timezone.
- [jQuery](http://jquery.com/)

## LICENSE

Copyright (c) 2014 Ron Gierlach

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
