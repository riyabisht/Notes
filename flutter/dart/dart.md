---
layout: default
title: Basics
parent: Dart
---

# Dart 

## Basics 

1. TOC
{:toc}

* In Dart, you can define code outside of classes. Variables, functions, getters, and setters can all live outside of classes.
* Dart doesn't have keywords for `public`, `private`, or `protected`.

```dart 
Bicycle(this.cadence, this.speed, this.gear);
```

* This constructor has no body, which is valid in Dart.
* If you forget the semicolon (;) at the end of a no-body constructor, DartPad displays the following error: "A function body must be provided."

```dart
Bicycle(int cadence, int speed, int gear)
      : this.cadence = cadence,
        this.speed = speed,
        this.gear = gear;
```

* Using `this` in a constructor's parameter list for assigning values to instance variables.
* `new` keyword became optional in Dart 2.
* If you know that a variable's value won't change, then you can use `final` instead of `var`.

* `print()` function accepts any object (not just strings). It converts it to a String using the object's toString() method.


```dart
@override
String toString() => 'Bicycle: $speed mph';
```

* `override` :  the analyzer that you are intentionally overriding a member. The analyzer raises an error if you fail to properly perform the override.
* Dart supports single or double quotes when specifying strings.
* Shorten one-line functions or methods using fat arrow (=>) notation
* Add a read-only variable
    * To mark a Dart identifier as private to its library, start its name with an underscore (_).
    * Each variable (even if it's a number) must either be initialized or be declared nullable by adding ? to its type declaration.
    *  Dart compiler enforces library privacy for any identifier prefixed with an underscore
    * Library privacy generally means that the identifier is visible only inside the file (not just the class) that the identifier is defined in.
    * Dart provides implicit getters and setters for all public instance variables.
    

```dart
    class Bicycle {
  int cadence;
  int _speed = 0;
  int get speed => _speed;
  int gear;

  Bicycle(this.cadence, this.gear);

  void applyBrake(int decrement) {
    _speed -= decrement;
  }

  void speedUp(int increment) {
    _speed += increment;
  }

  @override
  String toString() => 'Bicycle: $_speed mph';
}

void main() {
  var bike = Bicycle(2, 1);
  print(bike);
}

```
## imports

To access API's defined in other libraries use `import `



