# DartTaskIDK3

# Dart_gaga
```dart 
import 'dart:math';
import 'package:flutter/material.dart';

abstract class Shape {
  double getArea();
}

class Circle implements Shape {
  final double radius;

  Circle(this.radius);

  @override
  double getArea() {
    return pi * radius * radius;
  }
}

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    final Circle circle = Circle(5);

    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Задача 1'),
        ),
        body: Center(
          child: Text(
            'Площадь круга: ${circle.getArea().toStringAsFixed(2)}',
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:26] Zex: 
[05.05.2026 23:29] Zex: import 'package:flutter/material.dart';

abstract class Animal {
  String sound();
}

class Dog extends Animal {
  @override
  String sound() {
    return "Woof!";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Dog dog = Dog();

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 2')),
        body: Center(
          child: Text(
            dog.sound(),
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:30] Zex: 
[05.05.2026 23:30] Zex: import 'package:flutter/material.dart';

abstract class Drawable {
  String draw();
}

class Rectangle implements Drawable {
  @override
  String draw() {
    return "Drawing rectangle";
  }
}

class Triangle implements Drawable {
  @override
  String draw() {
    return "Drawing triangle";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final List<Drawable> objects = [
    Rectangle(),
    Triangle(),
  ];

  @override
  Widget build(BuildContext context) {
    final result = objects.map((object) => object.draw()).join('\n');

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 3')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:30] Zex: 
[05.05.2026 23:32] Zex: import 'package:flutter/material.dart';

abstract class Vehicle {
  double speed;

  Vehicle(this.speed);

  void accelerate();
}

class Car extends Vehicle {
  Car(double speed) : super(speed);

  @override
  void accelerate() {
    speed += 10;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Car car = Car(50);

  @override
  Widget build(BuildContext context) {
    car.accelerate();

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 4')),
        body: Center(
          child: Text(
            'Скорость после ускорения: ${car.speed}',
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:32] Zex: 
[05.05.2026 23:33] Zex: import 'package:flutter/material.dart';

class Parent {
  String greet() {
    return "Hello from Parent";
  }
}

class Child extends Parent {
  @override
  String greet() {
    return "Hello from Child";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Child child = Child();

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 5')),
        body: Center(
          child: Text(
            child.greet(),
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:33] Zex: 
[05.05.2026 23:34] Zex: import 'package:flutter/material.dart';

abstract class Calculator {
  int add(int a, int b);
  int subtract(int a, int b);
  int multiply(int a, int b);
}

class SimpleCalculator implements Calculator {
  @override
  int add(int a, int b) => a + b;

  @override
  int subtract(int a, int b) => a - b;

  @override
  int multiply(int a, int b) => a * b;
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final SimpleCalculator calculator = SimpleCalculator();

  @override
  Widget build(BuildContext context) {
    final result = '''
10 + 5 = ${calculator.add(10, 5)}
10 - 5 = ${calculator.subtract(10, 5)}
10 * 5 = ${calculator.multiply(10, 5)}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 6')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:35] Zex: 
[05.05.2026 23:36] Zex: import 'package:flutter/material.dart';

abstract class Person {
  String firstName;
  String lastName;

  Person(this.firstName, this.lastName);

  String showInfo();
}

class Student extends Person {
  Student(String firstName, String lastName) : super(firstName, lastName);

  @override
  String showInfo() {
    return "Student: $firstName $lastName";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Student student = Student("Ivan", "Petrov");

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 7')),
        body: Center(
          child: Text(
            student.showInfo(),
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:36] Zex: 
[05.05.2026 23:37] Zex: import 'package:flutter/material.dart';

abstract class Shape {
  double getArea();
}

class Circle implements Shape {
  double radius;

  Circle(this.radius);

  @override
  double getArea() => 3.14 * radius * radius;
}

class Rectangle implements Shape {
  double width;
  double height;

  Rectangle(this.width, this.height);

  @override
  double getArea() => width * height;
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final List<Shape> shapes = [
    Circle(5),
    Rectangle(4, 6),
  ];

  @override
  Widget build(BuildContext context) {
    final result = shapes
        .map((shape) => 'Площадь: ${shape.getArea()}')
        .join('\n');

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 8')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:37] Zex: 
[05.05.2026 23:38] Zex: import 'package:flutter/material.dart';

class Book {
  String title;
  String author;
  int year;

  Book(this.title, this.author, this.year);

  @override
  String toString() {
    return "Book: $title\nAuthor: $author\nYear: $year";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Book book = Book("Dart Basics", "Alex Ivanov", 2024);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 9')),
        body: Center(
          child: Text(
            book.toString(),
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:38] Zex: 
[05.05.2026 23:40] Zex: import 'package:flutter/material.dart';

abstract class NamedObject {
  String get name;
}

class User implements NamedObject {
  @override
  String name;

  User(this.name);
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final User user = User("Alice");

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 10')),
        body: Center(
          child: Text(
            'Name: ${user.name}',
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:40] Zex: 
[05.05.2026 23:41] Zex: import 'package:flutter/material.dart';

class Animal {
  String describe() {
    return "This is an animal";
  }
}

class Mammal extends Animal {
  @override
  String describe() {
    return "This is a mammal";
  }
}

class Dog extends Mammal {
  @override
  String describe() {
    return "This is a dog";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Animal animal = Animal();
  final Mammal mammal = Mammal();
  final Dog dog = Dog();

  @override
  Widget build(BuildContext context) {
    final result = '''
${animal.describe()}
${mammal.describe()}
${dog.describe()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 11')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:41] Zex: 
[05.05.2026 23:43] Zex: import 'package:flutter/material.dart';

mixin Flying {
  String fly() {
    return "Flying...";
  }
}

class Bird with Flying {
  String makeSound() {
    return "Chirp!";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Bird bird = Bird();

  @override
  Widget build(BuildContext context) {
    final result = '''
${bird.makeSound()}
${bird.fly()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 12')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:43] Zex: 
[05.05.2026 23:46] Zex: import 'package:flutter/material.dart';

class Logger {
  String log(String message) {
    return "Default log: $message";
  }
}

class CustomLogger extends Logger {
  @override
  String log(String message) {
    return "Custom log: $message";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Logger defaultLogger = Logger();
  final Logger customLogger = CustomLogger();

  @override
  Widget build(BuildContext context) {
    final result = '''
${defaultLogger.log("Hello")}
${customLogger.log("Hello")}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 13')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:46] Zex: 
[05.05.2026 23:48] Zex: import 'package:flutter/material.dart';

abstract class DatabaseConnection {
  String connect();

  String getVersion() {
    return "Database version 1.0";
  }
}

class MySqlConnection extends DatabaseConnection {
  @override
  String connect() {
    return "Connected to MySQL database";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final MySqlConnection connection = MySqlConnection();

  @override
  Widget build(BuildContext context) {
    final result = '''
${connection.connect()}
${connection.getVersion()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 14')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:48] Zex: 
[05.05.2026 23:50] Zex: import 'package:flutter/material.dart';

abstract class Employee {
  double getSalary();
}

class Developer extends Employee {
  @override
  double getSalary() => 3000;
}

class Manager extends Employee {
  @override
  double getSalary() => 5000;
}

class Designer extends Employee {
  @override
  double getSalary() => 2500;
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final List<Employee> employees = [
    Developer(),
    Manager(),
    Designer(),
  ];

  @override
  Widget build(BuildContext context) {
    final result = employees
        .map((employee) => 'Salary: ${employee.getSalary()}')
        .join('\n');

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 15')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:50] Zex: 
[05.05.2026 23:51] Zex: import 'package:flutter/material.dart';

abstract class MyComparable {
  int compare(MyComparable other);
}

abstract class ComparableObject implements MyComparable {
  int value;

  ComparableObject(this.value);
}

class NumberObject extends ComparableObject {
  NumberObject(int value) : super(value);

  @override
  int compare(MyComparable other) {
    if (other is NumberObject) {
      return value.compareTo(other.value);
    }

    return 0;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final NumberObject a = NumberObject(10);
  final NumberObject b = NumberObject(20);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 16')),
        body: Center(
          child: Text(
            'Результат сравнения: ${a.compare(b)}',
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:51] Zex: 
[05.05.2026 23:58] Zex: import 'package:flutter/material.dart' hide Container;

abstract class Container<T> {
  void add(T item);
  T get(int index);
}

class ListContainer<T> implements Container<T> {
  final List<T> _items = [];

  @override
  void add(T item) {
    _items.add(item);
  }

  @override
  T get(int index) {
    return _items[index];
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final ListContainer<String> container = ListContainer<String>();

  @override
  Widget build(BuildContext context) {
    container.add("Apple");
    container.add("Banana");

    final result = '''
Первый элемент: ${container.get(0)}
Второй элемент: ${container.get(1)}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 17')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:58] Zex: 
[05.05.2026 23:58] Zex: import 'package:flutter/material.dart';

abstract class Printable {
  String printInfo();
}

abstract class Savable {
  String save();
}

class Document implements Printable, Savable {
  @override
  String printInfo() {
    return "Printing document";
  }

  @override
  String save() {
    return "Saving document";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Document document = Document();

  @override
  Widget build(BuildContext context) {
    final result = '''
${document.printInfo()}
${document.save()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 18')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:58] Zex: 
[05.05.2026 23:58] Zex: import 'package:flutter/material.dart';

abstract class EditableName {
  String get name;
  set name(String value);
}

class User implements EditableName {
  String _name;

  User(this._name);

  @override
  String get name => _name;

  @override
  set name(String value) {
    _name = value;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final User user = User("Alice");

  @override
  Widget build(BuildContext context) {
    final oldName = user.name;
    user.name = "Bob";
    final newName = user.name;

    final result = '''
Старое имя: $oldName
Новое имя: $newName
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 19')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:58] Zex: 
[05.05.2026 23:59] Zex: import 'package:flutter/material.dart';

class Student {
  int id;
  String name;

  Student(this.id, this.name);

  @override
  bool operator ==(Object other) {
    return other is Student && other.id == id;
  }

  @override
  int get hashCode => id.hashCode;
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Student student1 = Student(1, "Alex");
  final Student student2 = Student(1, "Maria");
  final Student student3 = Student(2, "Ivan");

  @override
  Widget build(BuildContext context) {
    final result = '''
student1 == student2: ${student1 == student2}
student1 == student3: ${student1 == student3}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 20')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:59] Zex: 
[05.05.2026 23:59] Zex: import 'package:flutter/material.dart';

abstract class Math {
  static int add(int a, int b) {
    return a + b;
  }

  static int square(int number) {
    return number * number;
  }

  static double circleArea(double radius) {
    return 3.14 * radius * radius;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    final result = '''
5 + 3 = ${Math.add(5, 3)}
4² = ${Math.square(4)}
Площадь круга = ${Math.circleArea(5)}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 21')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:59] Zex: 
[05.05.2026 23:59] Zex: import 'package:flutter/material.dart';

abstract class A {
  String methodA();
}

abstract class B implements A {
  String methodB();
}

class C implements B {
  @override
  String methodA() {
    return "Method A";
  }

  @override
  String methodB() {
    return "Method B";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final C object = C();

  @override
  Widget build(BuildContext context) {
    final result = '''
${object.methodA()}
${object.methodB()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 22')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[05.05.2026 23:59] Zex: 
[05.05.2026 23:59] Zex: import 'package:flutter/material.dart';

abstract class Parser {
  dynamic parse(String input);
}

class IntParser implements Parser {
  @override
  int parse(String input) {
    int? result = int.tryParse(input);

    if (result == null) {
      throw FormatException("Cannot parse int: $input");
    }

    return result;
  }
}

class DoubleParser implements Parser {
  @override
  double parse(String input) {
    double? result = double.tryParse(input);

    if (result == null) {
      throw FormatException("Cannot parse double: $input");
    }

    return result;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final List<Parser> parsers = [
    IntParser(),
    DoubleParser(),
  ];

  @override
  Widget build(BuildContext context) {
    final List<String> results = [];

    for (Parser parser in parsers) {
      try {
        results.add('Result: ${parser.parse("123")}');
      } catch (error) {
        results.add('Error: $error');
      }
    }

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 23')),
        body: Center(
          child: Text(
            results.join('\n'),
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[06.05.2026 0:00] Zex: 
[06.05.2026 0:00] Zex: import 'package:flutter/material.dart';

abstract class Report {
  String generate() {
    return '''
${_prepare()}
${build()}
''';
  }

  String _prepare() {
    return "Preparing report...";
  }

  String build();
}

class SalesReport extends Report {
  @override
  String build() {
    return "Building sales report...";
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final SalesReport report = SalesReport();

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 24')),
        body: Center(
          child: Text(
            report.generate(),
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}
[06.05.2026 0:00] Zex: 
[06.05.2026 0:00] Zex: import 'package:flutter/material.dart';

abstract class Shape {
  double getArea();

  factory Shape.fromString(String type) {
    if (type == "circle") {
      return Circle(5);
    } else if (type == "rectangle") {
      return Rectangle(4, 6);
    } else {
      throw ArgumentError("Unknown shape type");
    }
  }
}

class Circle implements Shape {
  double radius;

  Circle(this.radius);

  @override
  double getArea() {
    return 3.14 * radius * radius;
  }
}

class Rectangle implements Shape {
  double width;
  double height;

  Rectangle(this.width, this.height);

  @override
  double getArea() {
    return width * height;
  }
}

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  MyApp({super.key});

  final Shape shape1 = Shape.fromString("circle");
  final Shape shape2 = Shape.fromString("rectangle");

  @override
  Widget build(BuildContext context) {
    final result = '''
Circle area: ${shape1.getArea()}
Rectangle area: ${shape2.getArea()}
''';

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: const Text('Задача 25')),
        body: Center(
          child: Text(
            result,
            textAlign: TextAlign.center,
            style: const TextStyle(fontSize: 24),
          ),
        ),
      ),
    );
  }
}

```
