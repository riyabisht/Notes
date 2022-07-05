
# DArt

## Class

- dart is object oriented programming with classes and mixin-based inheritance
- every oject is an instance of a class
- `mixing-based inheritance` means very class has exactly one super class superclass.
- class body can be reused in multiple class hierarchies 
- `extenstion` method are used to add functionalities

### using member class 

- use . to refer to an instance variable or method
```dart
var p = Point(2,2);

assert(p.y == 2)
```
- use `?` instead of . to avoid exeecption when leftmost operand is null

```dart
// If p is non-null, set a variable equal to its y value.
var a = p?.y;
```
### constructor

- `constructor names` can be either `class Name` or `ClassName.identifier`

```dart
var p1 = Point(2, 2);
var p2 = Point.fromJson({'x': 1, 'y': 2})
```
- `new` is optional before constructor name

```dart
var p1 = new Point(2, 2);
var p2 = new Point.fromJson({'x': 1, 'y': 2});
```
- `constant constructor`:some class provide 
- create complie time constant constructor
- write `const`
```dart
var p = const ImmutablePoint(2,2);
```
### Getting an object's type

use `object.runtimeType`

```dart
print('The type of a is ${a.runtimeType}');
```
## Implelemt class

```dart
class Point{
    double? x; // unitialized instance variables
    double? y; 
    double z =0; //instiallised
}
```
- `unitiallized` variables have null value
- all instance variable genereate getter method 
- non final instance and late final instance variables wiithout 