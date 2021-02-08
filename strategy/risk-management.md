# Risk Management


```javascript
//@version=4
// s t o p L o s s
// a function that determines what the stopLoss should be short and long entries
stop = input(defval=0.01, title="Stop", type=, minval=, maxval=100, step=0.01, options) → input float

x = [price you bought at]

if long
    stopPrice = x * y

// Trailing Stop:
var activationPrice = lowest(close, length)

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

//set limit sell orders at pivotHigh and pivotLow


// 
if(y)
    alert(message='{"stopPrice":"{{stop}}"}')
else
    sell

    ...
```

