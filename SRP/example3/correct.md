```

class ExpenseNotifier():

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

```

```

class ExpenseTracker():

    def __init__(self, max_amount: int, notifier: ExpenseNotifier):
        self.max_amount = max_amount
        self.used_amount = 0
        self.notifier = notifier
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:
            self.notifier.notify('You have reached the limit.')

```


## Execution
```
notifier = ExpenseNotifier()
tracker = ExpenseTracker(100, notifier)
tracker.track(30)
tracker.track(60)
tracker.track(20)
```

### OUTPUT

```
You have reached the limit.
```
