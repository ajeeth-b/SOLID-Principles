```python
class Square:
    def __init__(self, length):
        self.length = length

class Circle:
    def __init__(self, radius):
        self.radius = radius


class AreaCalculator:
    def __init__(self, shapes):
        self.shapes = shapes
    
    def sum(self):
        result = 0
        for shape in self.shapes:
            if type(shape) == Square:
                result += shape.length**2
            elif type(shape) == Circle:
                result += 3.14* shape.radius**2
        return result

    def output(self):
        str(self.sum())
```

## Execution
```python
shapes = [
    Square(4),
    Circle(5)
]

area_calculator = AreaCalculator(shapes)
area_calculator.output()
```

<div style="text-align: right"> <a href="./correct.md">next</a> </div>