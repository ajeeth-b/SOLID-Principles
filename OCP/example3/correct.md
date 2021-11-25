```

class ExpenseNotifier():

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

class ExpenseMailNotifier():

    def __init__(self, mail_id: text):
        self.mail_id = mail_id
    
    def check_network(self):
        # code to check internet connectivity
    
    def notify(self, message: text):
        # code to send mail

```

```

class ExpenseTracker():

    def __init__(self, max_amount: int, notifier: [ExpenseNotifier, ExpenseMailNotifier]):
        self.max_amount = max_amount
        self.used_amount = 0
        self.notifier = notifier
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:
            notifier.notify('You have reached the limit.')

```


## Execution
```
notifier = ExpenseMailNotifier('solid@gmail.com')
tracker = ExpenseTracker(100, notifier)
tracker.track(30)
tracker.track(60)
tracker.track(20)
```

### OUTPUT

```
You have reached the limit.
```


----
----



```

class Notifier():
    def __init__(self):
        pass
    
    def notify(self):
        pass

    def check_network(self):
        # code to check internet connectivity

class ExpenseNotifier(Notifier):

    def __init__(self):
        pass
    
    def notify(self, message: text):
        # code for popup notification

class ExpenseMailNotifier(Notifier):

    def __init__(self, mail_id: text):
        self.mail_id = mail_id
    
    def notify(self, message: text):
        self.check_network()
        # code to send mail

```

```

class ExpenseTracker():

    def __init__(self, max_amount: int, notifier: Notifier):
        self.max_amount = max_amount
        self.used_amount = 0
        self.notifier = notifier
    
    def track(self, expense_amount: int):
        self.used_amount += expense_amount
        if self.used_amount >= self.max_amount:
            notifier.notify('You have reached the limit.')

```


## Execution
```
notifier = ExpenseMailNotifier('solid@gmail.com')
tracker = ExpenseTracker(100, notifier)
tracker.track(30)
tracker.track(60)
tracker.track(20)
```

### OUTPUT

```
You have reached the limit.
```
