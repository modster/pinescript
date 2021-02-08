# Risk Management


```javascript
// Stop Loss:
x = [price you bought at]
stopPrice = x * 0.01

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

