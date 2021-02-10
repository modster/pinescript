# strategy()

## strategy.entry()
---
```
strategy.entry(id, long, qty, limit, stop, oca_name, oca_type, comment, when, alert_message) → void
```

EXAMPLE

---
```
strategy.entry(id="Long", long=true, qty=1, stop=longStop, oca_name="Greefer", oca_type=strategy.oca.reduce, comment="Long :" + tostring(close), alert_message="Long: "+ tostring(close))
strategy.entry(id="Long", long=true, qty=1, stop=longStop, oca_name="Greefer", oca_type=strategy.oca.reduce, comment="Long :" + tostring(close), alert_message="Long: "+ tostring(close))
```
## strategy.close()
---
```
strategy.close(id, when, comment, qty, qty_percent, alert_message) → void
```

```
strategy.close(id="Long", comment="Exit Long", qty=0.01, alert_message="Exit Long: " + tostring(close) )
strategy.close(id="Short", comment="Exit Short", qty=0.01, alert_message="Exit Short: " + tostring(close) )
```

EXAMPLE

---
```
strategy.close(id="Long", comment="Exit Long", qty=0.01, alert_message="Exit Long: " + tostring(close) )
strategy.close(id="Short", comment="Exit Short", qty=0.01, alert_message="Exit Short: " + tostring(close) )
plot(strategy.position_size)
```

## strategy.exit()
---
```
strategy.exit(id, from_entry, qty, qty_percent, profit, limit, loss, stop, trail_price, trail_points, trail_offset, oca_name, comment, when, alert_message) → void
```
EXAMPLE

```
strategy.exit(id="Exit Long", from_entry="Long", qty=0.05, limit=, loss, stop, oca_name="Greeffer", comment="Exit Long", alert_message=alert_message="Exit Long: "+ tostring(close))
strategy.exit(id="Exit Short", from_entry="Short", qty=0.05, limit=, loss, stop, oca_name="Greeffer", comment="Exit Short", alert_message=alert_message="Exit Short: "+ tostring(close))
```
