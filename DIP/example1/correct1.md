```python
class Notifier():
    def __init__(self):
        pass
    
    def notify(self, message: text):
        pass

class ExpenseNotifier(Notifier):

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

class ExpenseMailNotifier(Notifier):

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

class ExpenseTracker():

    def __init__(self, max_amount: int, notifier: Notifier):
        self.max_amount = max_amount
        self.used_amount = 0
        self.notifier = notifier
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:
            self.notifier.notify('You have reached the limit.')

```

1)
```python
notifier = ExpenseNotifier()
tracker = ExpenseTracker(100, notifier)
```
2)
```python
notifier = ExpenseMailNotifier()
tracker = ExpenseTracker(100, notifier)
```

<div style="text-align: right"> <a href="./wrong.md">prev</a> </div>
<div style="text-align: right"> <a href="./correct1.md">next</a> </div>
