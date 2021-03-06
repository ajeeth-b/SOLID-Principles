```python
class Square:
    def __init__(self, length):
        self.length = length
    
    def area(self):
        return self.length**2

class Circle:
    def __init__(self, radius):
        self.radius = radius
        self.pi = 3.14
        
    def area(self):
        return self.pi * self.radius**2

class Triangle:
    def __init__(self, base, height):
        self.base = base
        self.height = height
    
    def area(self):
        return (self.base*self.height)/2


class AreaCalculator:
    def __init__(self, shapes):
        self.shapes = shapes
    
    def calculate(self):
        result = 0
        for shape in self.shapes:
            result += shape.area()
        return result

class CalculatorOutput:
    
    def __init__(self, calculator: AreaCalculator):
        self.calculator = calculator

    def return_as_string(self):
        str(self.calculator.calculate())
    
    def return_as_json(self):
        to_json(self.calculator.calculate())
    
    def return_as_html(self):
        to_html(self.calculator.calculate())
```


## Execution
```python
shapes = [
    Square(4),
    Circle(5),
    Triangle(5)
]

area_calculator = AreaCalculator(shapes)
output1 = CalculatorOutput(area_calculator)
output1.return_as_string()
```

<div style="text-align: right"> <a href="./wrong.md">prev</a> </div>
