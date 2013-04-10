# sugar-unix

Methods for dealing with unix timestamps with Sugar.  For some reason javascript
returns timestamps as milliseconds rather than seconds.

## Usage

```js
// Statically, get the current time.
Date.unix() === (Date.now()/1000).round() === <the current time as a number>

// Call it on any date object.
(new Date()).unix()

// Parse too!
Date.fromUnix(1234567890)

///// BE CAREFUL /////
new Date(1234567890) != Date.fromUnix(1234567890)
// Because the date constructor uses milliseconds since the epoch.
```
