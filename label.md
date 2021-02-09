# label

## label.new
### Creates new label object
---
```
label.new(x, y, text, xloc, yloc, color, style, textcolor, size, textalign, tooltip) → series[label]
```
### EXAMPLE
```
var label1 = label.new(bar_index, low, text="Hello, world!", style=label.style_circle)
label.set_x(label1, 0)
label.set_xloc(label1, time, xloc.bar_time)
label.set_color(label1, color.red)
label.set_size(label1, size.large)
```
## RETURNS
Label ID object which may be passed to label.setXXX and label.getXXX functions

---
### EXAMPLE

Debugging a numerical value

---
```
label.new(bar_index, high, text=tostring(high))
```

### EXAMPL
---
```
//@version=4
study("Simple label", "", true)
label.new(bar_index, high, syminfo.ticker)
```