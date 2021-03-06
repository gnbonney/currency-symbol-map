# currency-symbol-map

A function to lookup the currency symbol for a given currency code and vice versa.

## Installation

    npm install currency-symbol-mapper

## Usage

### Get symbol from currency code
```js
var getSymbolFromCurrency = require('currency-symbol-map').getSymbolFromCurrency;
getSymbolFromCurrency('GBP'); //=> '£'
getSymbolFromCurrency('EUR'); //=> '€'
getSymbolFromCurrency('USD'); //=> '$'
getSymbolFromCurrency('NOT A VALID CODE'); //=> undefined
```

### Get currency code from symbol
```js
var getCurrencyFromSymbol = require('currency-symbol-map').getCurrencyFromSymbol;
getCurrencyFromSymbol('£'); //=> 'GBP'
getCurrencyFromSymbol('€'); //=> 'EUR'
getCurrencyFromSymbol('$'); //=> 'USD'
getCurrencyFromSymbol('NOT A VALID CODE'); //=> undefined
```

### Exposed maps for other processing
```js
var symbolCurrencyMap = require('currency-symbol-map').symbolCurrencyMap;
/*
{
  "$": "USD",
  "£": "GBP",
  ...
}
*/

var currencySymbolMap = require('currency-symbol-map').currencySymbolMap;
/*
{
  "USD": "$",
  "GBP": "£",
  ...
}
*/
```

## Shorthand usage

```js
var getSymbol = require('currency-symbol-map')
getSymbol('GBP') //=> '£'
getSymbol('EUR') //=> '€'
getSymbol('USD') //=> '$'
getSymbol('NOT A VALID CODE') //=> '?'
```

## Tests
```bash
npm test
```

## Credits

Forked from project maintained by Ben Gourley (https://github.com/bengourley/currency-symbol-map).
