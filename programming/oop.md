# OOP

#### Encapsulation

This concept is also often used to hide the internal representation, or state, of an object from the outside

#### Polymorphism

In object-oriented programming, polymorphism refers to a programming language's ability to process objects differently depending on their data type or class. More specifically, it is the ability to redefine methods for derived classes.

#### S.O.L.I.D.

* **Single-responsibility Principle:** A class should have one and only one reason to change, meaning that a class should have only one job.
* **Open-closed Principle:** Objects or entities should be open for extension, but closed for modification.
* **Liskov substitution principle:** The principle defines that objects of a superclass shall be replaceable with objects of its subclasses without breaking the application. That requires the objects of your subclasses to behave in the same way as the objects of your super-class. [Read More](https://stackify.com/solid-design-liskov-substitution-principle/)
* **Interface segregation principle:**
* **Dependency Inversion principle:**

#### Why Getters and Setters are good?

 Because we can handle the user input by setters and the output by getters. Maybe in the future we need to change the value of the variable before returning it to the user, it would be a nightmare maintenance if we used the property directly all over the code, but with a getter we could do it only in one place.

#### What is Inversion of Control \(IoC\)?

Means, instead of create a new object inside another class, pass it to the constructor. for example:

```php
class TextEditor {

    private SpellChecker $checker;

    public TextEditor() {
        $this.checker = new SpellChecker();
    }
}
```

it's better to change it to this:

```php
class TextEditor {

    private IocSpellChecker $checker;

    public TextEditor(IocSpellChecker $checker) {
        $this.checker = $checker;
    }
}
SpellChecker sc = new SpellChecker; // dependency
TextEditor textEditor = new TextEditor(sc);
```

Now, the `TextEditor` class is not dependent on only one `SpellChecker` class and the user can use another implementation of `SpellChecker` for the `TextEditor`.

### Design Patterns

#### Singleton: Only one instance of a class during the run-time

```php
    private static $instance;

    public static function getInstance() {
        if (!(self::$instance instanceof self)) {
            self::$instance = new self();
        }
        return self::$instance;
    }
```

**Use cases:** Logger, Config reader

#### Factory Pattern: 

1.  **Simple Factory Pattern.** This allows interfaces for creating objects without exposing the object creation logic to the client.
2.  **Factory Method Pattern.** This allows interfaces for creating objects, but allow sub-classes to determine which class to instantiate.
3.  **Abstract Factory Pattern.** Unlike the above two patterns, an abstract factory is an interface to create of related objects without specifying/exposing their classes. We can also say that it provides an object of another factory that is responsible for creating required objects.

**Use case:** Database factory, by changing the data-source, for example from SQLite to Mysql it will a Mysql class.

#### Builder Pattern

Lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.

Use Case: PHPUnit `createMock` method using Builder design pattern to create a mock object.



Fecade Pattern

Provides a simplified interface to a library, a framework, or any other complex set of classes.

Use Case: Used heavily in Laravel 







## References

{% embed url="https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design\#toc-single-responsibility-principle" %}

{% embed url="https://stackoverflow.com/questions/56860/what-is-an-example-of-the-liskov-substitution-principle" %}

{% embed url="https://stackoverflow.com/questions/757743/what-is-the-difference-between-builder-design-pattern-and-factory-design-pattern" %}



