# input()
```
input(defval, title, type, confirm) → input bool
```
```
input(defval, title, type, confirm) → input color
```
```
input(defval, title, type, minval, maxval, confirm, step, options) → input integer
```
```
input(defval, title, type, minval, maxval, confirm, step, options) → input float
```
```
input(defval, title, type, confirm, options) → input string
```
```
input(defval, title, type) → series[float]
```

EXAMPLE
```
b = input(title="On/Off", type=input.bool, defval=true)
plot(b ? open : na)
```
```
i = input(title="Offset", type=input.integer, defval=7, minval=-10, maxval=10)
plot(offset(close, i))
```
```
f = input(title="Angle", type=input.float, defval=-0.5, minval=-3.14, maxval=3.14, step=0.02)
plot(sin(f) > 0 ? close : open)

```
```
sym = input(title="Symbol", type=input.symbol, defval="DELL")

```
```
res = input(title="Resolution", type=input.resolution, defval="60")
```
```
c = input(title="Plot Color", type=input.color, defval=color.red)
plot(close, color=c)
plot(security(sym, res, close), color=color.green)
```
```
s = input(title="Session", defval="24x7", options=["24x7", "0900-1300", "1300-1700", "1700-2100"])
plot(time(timeframe.period, s))
```
```
src = input(title="Source", type=input.source, defval=close)
plot(src)
```
```
date1 = input(title="Date", type=input.time, defval=timestamp("20 Feb 2020 00:00 +0300"))
plot(date1)
```
```
date2 = input(title="Date", type=input.time, defval=timestamp("2020-02-20T00:00+03:00"))
plot(date2)
```