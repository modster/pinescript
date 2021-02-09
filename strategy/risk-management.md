# Risk Management
## Determine what the stop, take-profit, activationPrice, and limit values should be for entries and exits.

### Let the user set stop %, default is 0.1%
---
```javascript
stop = input(defval=0.1, title="Stop %", type=input.float, minval=0.01, maxval=100, step=0.01)
// for buy orders:
longStop = (100 - stop) / 100
longStop := close * longStop
plotchar(longStop, "longStop", "", location.top)
// for buy orders:
shortStop = (100 + stop) / 100
shortStop := close * longStop
plotchar(shortStop, "shortStop", "", location.top)
```
### Limit, take-profit, actiivationPrice
---
```javascript
var pivotLo = 0.0
var pivotHi = 0.0

pivotHiCondition= not na(pivotHigh)
pivotHi := pivotHiCondition ? pivotHigh : pivotHi[1]
// label.new(bar_index, pivotHi, text=tostring(pivotHi))

pivotLoCondition= not na(pivotLow)
pivotLow := pivotLowCondition ? pivotLow : pivotLow[1]
// label.new(bar_index, pivotHi, text=tostring(pivotHi))
if (...)
    alert(message='{"activationPrice":"' + tostring(pivotHi) +'", "limit":"' + tostring(pivotLo) +'"}')
```

### Trailing Stop
The Trailing Stop is a type of order on Binance. On a long position the activation price is < then the purchase price. The activaation price must be hit before the trailing stop begins "trailing"
( a work in progress )

---
```
// Trailing Stop:
var activationPrice = pivotHigh

alertcondition(y, "trailingStop", message='{"activationPrice":"{{}}", stopPrice":"{{plot("activationPrice")}}"}')
```
### Are we long or short?
---
```
var position = false

if ...
    panic := true
else
    panic := false
```
### ratcheting stop loss
---
```
var panic = false
var ratchetingStop = 

if crossunder(close, ratchetingStop))
    panic := true
else
    panic := false

alertcondition(panic, title="ratchetingStop", message='{"marketOrder":"{{plot("position")}}"}')
```



---
```

```
