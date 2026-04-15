# Admin Activity Spike SPL Starter

```spl
index=authentication user_role=admin
| bucket _time span=15m
| stats count by _time user
| where count > 10
```

Tune to your environment and combine with change context.
