```
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

class CalculatorOutput:
    
    def __init__(self, calculator: AreaCalculator):
        self.calculator = calculator

    def return_as_string(self):
        str(self.calculator.sum())
    
    def return_as_json(self):
        to_json(self.calculator.sum())
    
    def return_as_html(self):
        to_html(self.calculator.sum())
```


## Execution
```
shapes = [
    Square(4),
    Circle(5)
]

area_calculator = AreaCalculator(shapes)
output1 = CalculatorOutput(area_calculator)
output1.return_as_string()
```