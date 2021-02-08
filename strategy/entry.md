# strategy.entry
## **Parameters:**

```javascript

```

```javascript
strategy.entry('{"Long", strategy.long, stop = high, alert_message='{"long":"' + tostring(high) + '"}')")
```
## strategy:

```javascript
//@version=4

strategy("Strategy using `alert_message`")
r = rsi(close, 20)

// Detect crosses.
xUp = crossover( r, 50)
xDn = crossunder(r, 50)

// Place order on crosses using a custom alert message for each.
if xUp
    strategy.entry("Long", strategy.long, stop = high, alert_message = "Stop-buy executed (stop was " + tostring(high) + ")")
else if xDn
    strategy.entry("Short", strategy.short, stop = low, alert_message = "Stop-sell executed (stop was " + tostring(low) + ")")

// plot the 
plotchar(xUp, "Go Long",  "▲", location.bottom, color.lime, size = size.tiny)
plotchar(xDn, "Go Short", "▼", location.top,    color.red,  size = size.tiny)
hline(50)
plot(r)
```
