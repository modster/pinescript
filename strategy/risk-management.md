# Risk Management
## Determine what the stop, take-profit, activationPrice, and limit values should be for entries and exits

### let user set stop %, default is 1%
---
```javascript
stop = input(defval=1, title="Stop %", type=input.float, minval=0.01, maxval=100, step=0.01)
// for buy orders:
longStop = (100 - stop) / 100
longStop := close * longStop
plotchar(longStop, "longStop", "", location.top)
// for buy orders:
shortStop = (100 + stop) / 100
shortStop := close * longStop
plotchar(shortStop, "shortStop", "", location.top)
```
###  use pivotHigh and pivotLow for limit and take-profit orders
---
```
var pivotLo = 0.0
var pivotHi = 0.0

pivotHiCondition= not na(pivotHigh)
pivotHi := pivotHiCondition ? pivotHigh : pivotHi[1]
label.new(bar_index, pivotHi, text=tostring(pivotHi))

pivotLoCondition= not na(pivotLow)
pivotLow := pivotLowCondition ? pivotLow : pivotLow[1]
label.new(bar_index, pivotHi, text=tostring(pivotHi))

```
### ratcheting stop loss
---
```
if long
    stopPrice = x * stop

```
### activationPrice
---
```
// Trailing Stop:
var activationPrice = lowest(close, length) //<--------------

var stopPrice = 

if close < stopPrice
    activationPrice := lowest(close, length)
else if close > ema76
    ap := highest(close, length)

alertcondition(y, "trailingStop", message='{"activationPrice":"{{}}", stopPrice":"{{plot("activationPrice")}}"}')
```
###
---
```

```

---
```

```
