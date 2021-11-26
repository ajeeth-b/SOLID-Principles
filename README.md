# SOLID Principles

**S** - Single Responsiblity principle(SRP)

**O** - Open/Closed Principle

**L** - Liskov Substitution Principle(LSP)

**I** - Interface Segregation Principle(ISP)

**D** - Dependency Inversion Principle(DIP)

```
The mail goal of SOLID principles is to reduce dependencies so that  changes or addition in one area of software without impacting others.
```

## [SRP](https://github.com/ajeeth-b/SOLID-Principles/tree/master/SRP)
```
A class should have one and only one reason to change, meaning that a class should have only one job.
```
- when we acheive SRP, the amount of posiblity of code reusabilty increases
- Code maintainablity
- Dependency management
- Loose coupling


[example1](https://github.com/ajeeth-b/SOLID-Principles/tree/master/SRP/example1/wrong.md)

## [OCP](https://github.com/ajeeth-b/SOLID-Principles/tree/master/OCP)
```
Objects or entities should be open for extension but closed for modification.
```

- a new functionality should be implemented by adding new class, method or attributes, insted of changing current code.

[example1](https://github.com/ajeeth-b/SOLID-Principles/tree/master/OCP/example1/wrong.md)
## [LSP](https://github.com/ajeeth-b/SOLID-Principles/tree/master/LSP)

```
If A is a sub type of B, then object of type B may be replaced with type A. 
```

- Derived type must be completly substitutable for their base types.
- To maintain strong sub typing.
- client should behave same regardless of sub type instance. 

[example1](https://github.com/ajeeth-b/SOLID-Principles/tree/master/LSP/example1/wrong.md)

## [ISP](https://github.com/ajeeth-b/SOLID-Principles/tree/master/ISP)
```
A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.
```
- have smallest possible interface between class/obj when they communicate
- keep your interfaces as small as posible.

[example1](https://github.com/ajeeth-b/SOLID-Principles/tree/master/ISP/example1/wrong.md)

## [DIP](https://github.com/ajeeth-b/SOLID-Principles/tree/master/DIP)
```
Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.
```
- depend upon Interface/abstraction rather than concrete classes.

[example1](https://github.com/ajeeth-b/SOLID-Principles/tree/master/DIP/example1/wrong.md)