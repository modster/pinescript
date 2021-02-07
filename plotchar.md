# plotchar()
```javascript
plotchar(series, title, char, location, color, transp, offset, text, textcolor, editable, size, show_last, display) → void
```

### ARGUMENTS
- series (series) Series of data to be plotted as shapes. Series is treated as a series of boolean values for all location values except location.absolute. Required argument.

- title (const string) Title of the plot.
char (input string) Character to use as a visual shape.

- location (input string) Location of shapes on the chart. Possible values are: location.abovebar, location.belowbar, location.top, location.bottom, location.absolute. Default value is location.abovebar.
color (color) Color of the shapes. You can use constants like 'color=color.red' or 'color=#ff001a' as well as complex expressions like 'color = close >= open ? color.green : color.red'. Optional argument.

- transp (input integer) Transparency of the shapes. Possible values are from 0 (not transparent) to 100 (invisible). Optional argument.
- offset (integer) Shifts shapes to the left or to the right on the given number of bars. Default is 0.

- text (const string) Text to display with the shape. You can use multiline text, to separate lines use '\n' escape sequence. Example: 'line one\nline two'

- textcolor (color) Color of the text. You can use constants like 'textcolor=color.red' or 'textcolor=#ff001a' as well as complex expressions like 'textcolor = close >= open ? color.green : color.red'. Optional argument.

- editable (const bool) If true then plotchar style will be editable in Format dialog. Default is true.
show_last (input integer) If set, defines the number of chars (from the last bar back to the past) to plot on chart.

- size (const string) Size of characters on the chart. Possible values are: size.auto, size.tiny, size.small, size.normal, size.large, size.huge. Default is size.auto.

- display (const integer) Controls where the plot is displayed. Possible values are: display.none, display.all. Default is display.all

https://www.tradingview.com/pine-script-reference/v4/#fun_plotchar