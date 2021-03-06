# Number Shuffler

This module shuffle NUMBER.

![demo](https://raw.githubusercontent.com/wiki/mildjester/number-shuffler/demo.gif)

## Installation

npm
```
$ npm install number-shuffler
```

cdn
```
<script src="https://unpkg.com/number-shuffler@0.1.0/dist/number-shuffler.js"></script>
```

## Usage

### import
import this module. (if install via npm only)
```
import * as NumberShuffler from "number-shuffler";
```

### initialize
pass element that display number in init method argument.
```
let ns = NumberShuffler.init(TargetElement);
```

### set option
Set the options if necessary.
```
ns.setOption({
    interval: 50,
    digit: 6,
});
```

|option|type|description|default|
|------|----|-----------|-------|
|format|boolean|flag for format a number.|true|
|interval|number|interval to switch numbers.(msec) |30|
|digit|number|the number of digits|3|


### start / stop

```
// start shuffling a number.
ns.start()

// stop shuffling a number.
ns.stop()
```

## Example
HTML
```
<div id="numBox">000,000</div>
<button type="button" id="startBtn">start</button>
<button type="button" id="stopBtn">stop</button>
```

Javascript
```
import * as NumberShuffler from "number-shuffler";

document.addEventListener("DOMContentLoaded", function() {
  let numBoxElm = document.getElementById('numBox');
  let ns = NumberShuffler.init(numBoxElm);

  ns.setOption({
    interval: 50,
    digit: 6,
  });

  document.getElementById('startBtn').addEventListener('click', function(){
    ns.start();
  });
  document.getElementById('stopBtn').addEventListener('click', function(){
    ns.stop();
  });
});
```
