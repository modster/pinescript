# Risk Management
## s t o p L o s s ( )
### A function that determines what the stop, take-profit, and limit should be for short and long entries
---
```javascript
//@version=4

// let user change stop % 
stop = input(defval=0.01, title="Stop", type=input.float, minval=0.01, maxval=100, step=0.01)
x = [price you bought at] // <--------------
limit = // <---------------

if long
    stopPrice = x * stop

// Trailing Stop:
var activationPrice = lowest(close, length) //<--------------

// this part needs work
if close < ema76
    activationPrice := lowest(close, length)
else if close > ema76
    ap := highest(close, length)

// option #1 is to use alert():
y= cross(close, ap)
if(y)
    alert(message='{"stopPrice":"{{stop}}"}')

// option #2 is to use alertcondition():
alertcondition(y, "trailingStop", message='{"activationPrice":"{{}}", stopPrice":"{{plot("activationPrice")}}"}')
```
### use pivotHigh and pivotLow for limit and take-profit orders
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
