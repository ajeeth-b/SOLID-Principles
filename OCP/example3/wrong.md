```

class ExpenseNotifier():

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

class ExpenseMailNotifier():

    def __init__(self, mail_id: text):
        self.mail_id = mail_id
    
    def notify(self, message: text):
        # code to send mail

```

```

class ExpenseTracker():

    def __init__(self, max_amount: int, medium: text):
        self.max_amount = max_amount
        self.used_amount = 0
        self.medium = medium
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:

            if self.medium == 'console':
                notifier = ExpenseNotifier()
                notifier.notify('You have reached the limit.')
            elif self.medium == 'mail':
                notifier = ExpenseMailNotifier('solid@gmail.com')
                notifier.notify('You have reached the limit.')

```


## Execution
```
tracker = ExpenseTracker(100, medium='mail')
tracker.track(30)
tracker.track(60)
tracker.track(20)
```

### OUTPUT

```
You have reached the limit.
```
