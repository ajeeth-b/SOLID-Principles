```python
class Shape:
    def __init__(self):
        pass
    
    def area(self):
        pass
    
    def volume(self):
        pass

class Square(Shape):
    def __init__(self, length):
        self.length = length
    
    def area(self):
        return self.length**2
    
    def volume(self):
        return 0

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
        self.pi = 3.14
        
    def area(self):
        return self.pi * self.radius**2
    
    def volume(self):
        return 0

class Cube(Shape):
    def __init__(self, length):
        self.length = length
    
    def area(self):
        return 6*self.length**2
    
    def volume(self):
        return self.length**3


class AreaCalculator:
    def __init__(self, shapes):
        self.shapes = shapes
    
    def sum(self):
        result = 0
        for shape in self.shapes:
            result += shape.area()
        return result

class VolumeCalculator(AreaCalculator):
    def __init__(self, shapes):
        self.shapes = shapes
    
    def sum(self):
        result = 0
        for shape in self.shapes:
            result += [shape.volume()]
        return sum_of_array(result)

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
```python

area_calculator = AreaCalculator(shapes)
output1 = CalculatorOutput(area_calculator)

area_calculator = VolumeCalculator(solid_shapes)
output2 = CalculatorOutput(area_calculator)

output1.return_as_string()
output2.return_as_string()

```


<div style="text-align: right"> <a href="./wrong.md">prev</a> </div>
