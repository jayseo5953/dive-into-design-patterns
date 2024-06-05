# Pillars of OOP

## Abstraction

- Hiding unimportant implementation
- Providing a generalization
- Having objects represent the real world objects
- May not be 100% accurate of the real world object but should be accurate in the specific context that is relevant
- e.g AirPlane objects can have different states(attributes) and behaviour(methods) depending on the context (airplane simulator, airplane booking system)

## Encapsulation

- Hiding information
- Hide details under the hood (usually with `private` or `protected` keyword)
- Expose an interface for interaction with other objects
- OOP programming languages provide `interface` or `protocol` keyword that defines interaction between objects
- Interfaces are objects not actual class without states but only with methods
- E.g. Airport objects can interact with any objects that implements `FlyingTransPort` interface whatever the object that is
- Ensures two objects interact correctly

## Inheritance

- Ability to create new classes on top of existing classes
- Code reuse
- Limitation is that subclasses inherit all methods (interface) of parents even though they do not make sense for the child classes
- One class can implement multiple classes so subclasses must implement all of its parent’s interface

## Polymorphism

- Superclasses themselves or their behaviour are meant to be overridden.
- For example, Animal class’s makeSound method
- Or the superclass is too general so that many of its parts will be replaced.
- Then we can set a class as `abstract` class
- `Abstract` class is a class that is not meant to be used to produce instances but only an extraction of core part so that it will be extended to create new classes that can produce instances (concrete class)
- `Abstract` methods are just a container with empty body which will be filled by subclasses
- Ability of an object to pretend to be something else
- When a method is called, the program can trace down the subclass of the object and whose method is being called and run it.
- When an object exists and we do not know if it is a dog or cat who share the same superclass. The program will know which subclass it is and run its method.
- E.g. Checkbox, Input, Button all inherit from HtmlElement. They all have `render` method in it which will render different things. There is an object called `element` which we do not know in the current context. But the program will figure out which subclass it is an instance of, and render the correct one. `element.render()`
