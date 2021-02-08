# Risk Management
##

```javascript

x = price you bought at
stop = x * 0.01

var ap = 0.0

if close < ema76
    ap := lowest(close?, x?)
else if close > ema76
    ap := highest(close, x)
else if ...

y= cross(close, ap)
if(y)
    alert(message='{"stopPrice":"{{stop}}"}')

alertcondition(y, "trailingStop", message='{"activationPrice":"{{ap}}"}')

set limit sell orders at pivot point
----------------------
if(y)
    alert(message='{"stopPrice":"{{stop}}"}')
else
    sell

    ...
