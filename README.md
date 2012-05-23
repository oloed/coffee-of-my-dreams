# MacchiatoScript
Just because this is my favorite coffee.

The list contains changes of coffeescript so it'll become the best possible
compiled to js language in my interpretation.

## Changes
* Add support for dashes in variable names
https://github.com/gkz/LiveScript/issues/17
* Add support for Scala placeholder
https://github.com/gkz/LiveScript/issues/19
* Auto-add `use strict` to the result js.
* Play with `Object.freeze` / `const` to achieve great immutability of shit.
(still not sure how exactly)

## Example code

```coffeescript
['hitler ', 1945].map(_.to-string()).map(_.trim()).filter(_.length > 5)
[1, 2, 3].map(_ * 2).filter(_ > 5).reduce-left(_ + _)
```

will be compiled to

```javascript
['hitler ', 1945]
  .map(function(_0) {return _0.toString();})
  .map(function(_0) {return _0.trim();})
  .filter(function(_0) {return _0.length > 5;});
[1, 2, 3]
  .map(function(_0) {return _0 * 2;})
  .filter(function(_0) {return _0 > 5;})
  .reduceLeft(function(_0, _1) {return _0 + _1;});
```
