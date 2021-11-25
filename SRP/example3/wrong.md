```
class ExpenceTracker():

    def __init__(self, max_amount: int):
        self.max_amount = max_amount
        self.used_amount = 0
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:
            self.pop_up_notification('You have reached the limit.')
    
    def pop_up_notification(self, message: text):
        # code for popup notification

```

```
tracker = ExpenceTracker(100)
tracker.track(30)
tracker.track(60)
tracker.track(20)
```

### OUTPUT

```
You have reached the limit.
```
