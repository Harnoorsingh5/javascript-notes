# javascript-notes

# Arithmetic Operators
An arithmetic operator takes numeric values (either literals or variables) as its operands and returns a single numeric value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/). Other arithmetic operators are remainder (%), unary negation (-), unary plus (+), increment (++), decrement (--), and exponentiation (**).
1. Addition (+)
We use this operator in the form operand1 + operand_2. For example:
```
2 + 3 // evaluates to 5
4 + 10 // evaluates to 14
```

2. Subtraction (-)
We use this operator in the form operand1 - operand2. For example:
```
3 - 2 // evaluates to 1
4 - 10 // evaluates to -6
```

3. Multiplication (*)
We use this operator in the form operand1 * operand2. For example:
```
3 * 2 // evaluates to 6
4 * 10 // evaluates to 40
```

4. Division (/)
We use this operator in the form operand1 / operand2. For example:
```
6 / 3 // evaluates to 2
3 / 2 // evaluates to 1.5
4 / 10 // evaluates to 0.4
```

5. Remainder (%)
We use this operator in the form operand1 % operand2. For example:
```
6 % 3 // evaluates to 0
3 % 2 // evaluates to 1
4 % 10 // evaluates to 4
```

6. Exponentiation (**)
We use this operator in the form operand1 ** operand2. This operator is a part of ECMAScript2016 feature set. For example:
```
2 ** 3 // evaluates to 8
3 ** 2 // evaluates to 9
5 ** 4 // evaluates to 625
```
7. Unary Negation (-)
We use this operator in the form -operand. For example:
```
-4 // evaluates to -4
-(-5) // evaluates to 5 (not --5)
```
8. Unary Plus (+)
We use this operator in the form +operand. For example:
```
+4 // evaluates to 4
+(-4) // evaluates to -4
```
9. Increment (++)
We use this operator in the prefix and postfix forms, forms ++operand and operand++. The prefix form, ++operand, increments the operand by  and then returns the value of the operand. The postfix form, operand++, returns the value of the operand and then increments the operand's value by . For example:
```
var a = input;
    // Print the value of 'a' and the preincremented value of 'a':
    console.log("a(" + a + "), ++a(" + ++a + ")");
    // Assign the current value of 'a' to 'b' and then postincrement 'a':
    var b = a++;
    // Print the values of 'a' once and 'b' twice, then postincrement the 2nd 'b':
    console.log("a(" + a + "), b(" + b + "), b++(" + b++ + ")");
    // Print the final values of 'a' and 'b':
    console.log("a(" + a + "), b(" + b + ")");
```
```
a(4), ++a(5)
a(6), b(5), b++(5)
a(6), b(6)
```

10. Decrement (--)
We use this operator in the prefix and postfix forms, forms --operand and operand--. The prefix form, --operand, decrements the operand by  and then returns the value of the operand. The postfix form, operand--, returns the value of the operand and then decrements the operand's value by . For example:

```
var a = input;
    // Print the value of 'a' and the predecremented value of 'a':
    console.log("a(" + a + "), --a(" + --a + ")");
    // Assign the current value of 'a' to 'b' and then postdecrement 'a':
    var b = a--;
    // Print the values of 'a' once and 'b' twice, then postdecrement the 2nd 'b':
    console.log("a(" + a + "), b(" + b + "), b--(" + b-- + ")");
    // Print the final values of 'a' and 'b':
    console.log("a(" + a + "), b(" + b + ")");
```
```
a(4), --a(3)
a(2), b(3), b--(3)
a(2), b(2)
```

# Variable Declaration Keywords
1. var
* We use the var keyword to declare variables. 
* The scope of a variable declared using this keyword is within the context wherever it was declared.
* For variables declared outside any function, this means they are globally available throughout the program.
* For variables declared within a function, this means they are only available within the function itself.
```
function main(input) {
    var a = input;

    // If 'a' is odd:
    if (a % 2 == 1) {
        var a = input + 1;
        console.log("if(a): " + a);
    }

    console.log("main(a): " + a);
}
OUTPUT:
if(a): 12
main(a): 12
```
2. let
* We use the let keyword to declare variables that are limited in scope to the block, statement, or expression in which they are used.
* This is unlike the var keyword, which defines a variable globally or locally to an entire function regardless of block scope.
```
function main(input) {
    let a = input;

    // If 'a' is odd:
    if (a % 2 == 1) {
        // Increment 'a' by 1
        let a = input + 1; //block scope
        console.log("if(a): " + a);
    }

    console.log("main(a): " + a);
}
OUTPUT:
if(a): 12
main(a): 11
```

3. const
* We use the const keyword to create a read-only reference to a value, meaning the value referenced by this variable cannot be reassigned.
* Because the value referenced by a constant variable cannot be reassigned, JavaScript requires that constant variables always be initialized.

```
function main(input) {
    const a = input;

    // This will throw "SyntaxError: Missing initializer in const declaration"
    const b; 

    console.log(a);
}
OUTPUT:
Error
```


# Loops

1. For: The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by one or more statements that will be executed in the loop.
```
  for (var i = 1; i <= input; i++) {
        console.log(i + " ");
    }
```
```
var i=1
  for (; i <= input; i++) {
        console.log (i + " ");
    }
```
```
for (var i = 1;; i++) {
        if (i > input) {
            break;
        }
        console.log (i + " ");
    }
```
```
var i = 1;
    for (;;) {
        if (i > input) {
            break;
        }
        console.log(i + " ");
        i++;
    }
```

2. While: The while statement creates a loop that executes its internal statement(s) as long as the specified condition evaluates to true. The condition is evaluated before executing the statement.

```
var i = 1;
    while (i <= input) {
        console.log(i + " ");
        i++;
    }
```





3. do-while: The do-while statement creates a loop that executes its internal statement(s) until the specified condition evaluates to false. The condition is evaluated after executing the internal statement(s), so the contents of the loop always execute at least once.
```
    var i = 1;
    do {
        console.log(i + " ");
        i++;
    } while (i <= input);
```

4. for-in: This loop iterates (in an arbitrary order) over the name of each enumerable property in an object, allowing statements to be executed for each distinct property.
```
var actress = {
    firstName: "Julia",
    lastName: "Roberts",
    dateOfBirth: "October 28, 1967",
    nationality: "American",
    firstMovie: "Satisfaction"
};

for (var property in actress) {
    console.log("actress." + property + " = " + actress[property]);
}
```
```
class Monster {
    constructor(name, home, description) {
        this.name = name;
        this.home = home;
        this.description = description;
    }
}

function main(input) {
    var monster = new Monster(input[0], input[1], input[2]);

    // Print array
    console.log(monster);

    // Print each of its elements on a new line
    for (let property in monster) {
        console.log(property + ": " + monster[property]);
    }
}
```

5. for-of: This loop iterates over iterable objects such as an Array, Map, Set, String, TypedArray, arguments object, etc. It essentially iterates over the value of each distinct property in the structure, such as each letter in a word or each element in an array.

```
function main(input) {
    // Split the words read as input into an array of words
    var array = input.split(new RegExp("[ \n]+"));

    // Print array
    console.log(array);

    // Print each of its elements on a new line
    for (let value of array) {
        console.log(value);
    }
}
```
# Arrays
The JavaScript Array object is a global object that is used in the construction of arrays; which are high-level, list-like objects.
```
var a = ['first', 'second'];

console.log('a\'s contents:', a);
console.log('a\'s length:', a.length);
// first = 'first'
let first = a[0]; 

// last = 'second'
let last = a[a.length - 1]; 

console.log('a[0]:', first);
console.log('a[a.length - 1]:', last);
```
* Loop Over an Array
```
var a = ['first', 'second'];

a.forEach(function(e, i, array) {
    // 'i' is the index
    // 'e' is the element
    console.log(i + ' ' + e);
});
```

* Append to the End of an Array
```
var a = ['first', 'second'];

// Append 'third' to array 'a'
a.push('third');

console.log('a:', a);
```



* Remove From the end of an Array
```
var a = ['first', 'second', 'third'];
console.log('Original Array:', a);

// Remove the last element from the array
let removed = a.pop();

console.log('Modified Array:', a);
console.log('Removed Element:', removed);
```

* Remove From the Front of an Array
```
var a = ['first', 'second', 'third'];
console.log('Original Array:', a);

// Remove the first element from the array
let removed = a.shift();

console.log('Modified Array:', a);
console.log('Removed Element:', removed);
```

* Add to the Front of an Array
```
var a = ['first', 'second', 'third'];
console.log('Original Array:', a);

// Insert element at the beginning of the array
a.unshift('fourth');

console.log('Modified Array:', a);
```

* Remove an Item by Index Position
```
var a = ['first', 'second', 'third', 'fourth', 'fifth'];
console.log('Original Array:', a);

let position = 1;
let elementsToRemove = 2;
// Remove 'elementsToRemove' element(s) starting at 'position'
a.splice(position, elementsToRemove);

console.log('Modified Array:', a);
```

# Objects in JavaScript
## Object Basics
We define the following:
* Object: A collection of properties.
* Property: An association between a name (i.e., key) and a value. Note that when the value associated with a key is a function, we call the property a method. A property name can be any valid string, or anything that can be converted into a string (including the empty string).
An object has properties associated with it, and we explain an object's properties as variables that are part of the object. We can think of an object's properties as a set of regular variables specific to that object that define its characteristics.
Let's say we have an object named ObjectName and a property named propertyName. We can access this property in the following ways:
1.	Dot Notation: Call objectName.propertyName.
2.	Bracket Notation: Call objectName['propertyName']. Note that propertyName must be enclosed in string quotes and is case-sensitive. Any property name that's not a valid JavaScript identifier (e.g., starts with a number, contains a space or hyphen, etc.) can only be accessed using bracket notation. This type of notation is also good to use when property names are dynamically determined (i.e., not known until runtime).

```
var actor = {
    Name: 'Julia Roberts', 
    Age: 36
};

// Print the object
console.log('The \'actor\' object:', actor);

// Access object's properties using bracket notation
console.log('The \'Name\' property:', actor['Name']);
console.log('The \'Age\' property:', actor['Age']);

// Access object's properties using dot notation
console.log('The \'Name\' property:', actor.Name);
console.log('The \'Age\' property:', actor.Age);

// Add a new property called 'EyeColor'
actor.EyeColor = 'Brown';

// Print the object
console.log('The updated \'actor\' object:', actor);

// Trying to access undefined property results in 'undefined'
console.log('Attempt to access an undefined property (\'HairColor\'):', 
    actor.HairColor);
```
```
Output:
The 'actor' object: { Name: 'Julia Roberts', Age: 36 }
The 'Name' property: Julia Roberts
The 'Age' property: 36
The 'Name' property: Julia Roberts
The 'Age' property: 36
The updated 'actor' object: { Name: 'Julia Roberts', Age: 36, EyeColor: 'Brown' }
Attempt to access an undefined property ('HairColor'): undefined
```

## Creating Objects
We can create objects using an object initializer, or we can first create a constructor function and then instantiate an object using that function's name in conjunction with the new operator.
1. Using Object Initializers
We can initialize an object using new Object(), Object.create(), or by using the literal (or initializer) notation. An object initializer is a comma-separated list of zero or more property name-value pairs defining an object, enclosed in curly braces (i.e., {}).

* Using Initializer Notation
```
var a = 3;
var b = 'Rome';
var c = false;

var o = {a, b, c};

console.log('Object \'o\':', o);

var p = {
    a: 3, 
    b: 'Rome', 
    c: false
};

console.log('Object \'p\':', p);

var q = {};
console.log('Object \'q\' (Initial):', q);
q.a = a;
q.b = b;
q.c = c;
console.log('Object \'q\' (Updated):', q);
```

* Using new Object()

```
var o = new Object();

o.a = 4;
o.b = 'Rome';
o.c = true;

console.log('Object \'o\':', o);
```

* Using Object.create()

```
var x = {
    a: 5, 
    foo: function() {
        return this.a * this.a;
    }
};

var o = Object.create(x);

console.log('\'x\':', x);
console.log('Object \'o\':', o);
console.log('Property \'o.a\':', o.a);
console.log('Method \'o.foo()\':', o.foo());

o.a = 7;

console.log('Property \'o.a\':', o.a);
console.log('Method \'o.foo()\':', o.foo());
```

# Classes in JavaScript
## Functional Classes
In this section, we'll discuss some of the ways we can use functions to simulate the behavior of classes.
Using Functions
1.	Define a normal JavaScript function.
2.	Create an object by using the new keyword.
3.	Define properties and methods for a created object using the this keyword.

```
'use strict';

function Fruit (type) {
    this.type = type;
    this.color = 'unknown';
    this.getInformation = getFruitInformation;
}

function getFruitInformation() {
    return 'This ' + this.type + ' is ' + this.color + '.';
}

let lime = new Fruit('Mexican lime');
console.log(lime.getInformation());

lime.color = 'green';
console.log(lime.getInformation());
```
Output:
```
This Mexican lime is unknown.
This Mexican lime is green.
```

## Classes
JavaScript classes, introduced in ECMAScript 6, are essentially syntactic sugar over JavaScript's existing prototype-based inheritance that don't actually introduce a new object-oriented inheritance model. This syntax is a means of more simply and clearly creating objects and deal with inheritance.
We define classes in two ways:
Class Declarations
One way to define a class is using a class declaration. To declare a class, we use the class keyword and follow it with the class' name. Ideally, we always write class names in TitleCase.

```
class Polygon {
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
}

let p = new Polygon(1, 2);
console.log('Polygon p:', p);
```

## Class Expressions
Class expressions are another way to define a class, and they can be either named or unnamed. The name given to a named class expression is local to the class' body.
Unnamed Class Expression
```
let Polygon = class {
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
};

console.log('Polygon:', Polygon);
let p = new Polygon(1, 2);
console.log('p:', p);
```

Named Class Expression
```
let Polygon = class Polygon {
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
};

console.log('Polygon:', Polygon);
let p = new Polygon(1, 2);
console.log('p:', p);
```

## The Constructor Method
* The constructor method is a special method we use to create and initialize objects of a class.
* A class can only have one special method with the name constructor, and attempting to write a class containing more than one constructor method will throw a SyntaxError.
* To implement inheritance, we can use the super keyword in a constructor to call a parent class constructor.
```
'use strict';

class Polygon {
    constructor(height, width) {
        this.height = height;
        this.width = width;
    }
    getArea() {
        return this.height * this.width;
    }
}

const square = new Polygon(10, 10);

console.log(square.getArea());

```
## Static Methods
Static methods are methods relevant to all instances of a class — not just any one instance. These methods receive information from their arguments and not a class instance, which allows us to invoke a class' static methods without creating an instance of the class. In fact, we actually can't call a static method on an instantiated class object (attempting to do so throws a TypeError).
We define a class' static methods using the static keyword. We typically use these methods to create utility functions for applications, as they can't be called on class objects.

```
'use strict';

class Point {
    constructor(x, y) {
        this.x = x;
        this.y = y;
    }
    static distance(a, b) {
        const dx = a.x - b.x;
        const dy = a.y - b.y;
        return Math.sqrt(dx * dx + dy * dy);
    }
}

const p1 = new Point(5, 5);
const p2 = new Point(10, 10);

// The correct way to call a static method
console.log(Point.distance(p1, p2));

// Attempt to call a static method on an instance of the class
try {
    console.log(p1.distance(p1, p2));
}
catch (exception) {
    console.log(exception.name + ': ' + exception.message);
}
```

## Inheritance
In essence, this construct allows us to create an object prototype or class that's an extension of another object prototype or class. A class inheriting from some other class (referred to as a superclass or parent class) is called a subclass (or child class). The subclass inherits the superclass' methods and behaviors, but it can also declare new ones or even override existing ones.
Subclassing with the extends Keyword
We use the extends keyword in class declarations or class expressions to create a child class (i.e., subclass).

```
'use strict';

class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        console.log(this.name, 'speaks.');
    }
}

class Dog extends Animal {
    speak() {
        console.log(this.name, 'barks.');
    }
}

let spot = new Dog('Spot');
spot.speak();

spot = new Animal('Spot');
spot.speak();
```

We can also extend functional classes:
```
'use strict';

function Animal(name) {
    this.name = name;
}

Animal.prototype.speak = function() {
    console.log(this.name, 'speaks.');
}

class Dog extends Animal {
    speak() {
        console.log(this.name, 'barks.');
    }
}

let spot = new Dog('Spot');
spot.speak();

spot = new Animal('Spot');
spot.speak();
```

Superclass Calls Using the super Keyword
We use the super keyword to call functions on an object's parent.
```
'use strict';

class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        console.log(this.name, 'speaks.');
    }
}

class Dog extends Animal {
    speak() {
        super.speak();
        console.log(this.name, 'barks.');
    }
}

let spot = new Dog('Spot');
spot.speak();
```

## Extending an Object
The ability to extend multiple classes from the same superclass (or model multiple object types after the same prototype) is powerful because it provides us with certain implied guarantees about the basic functionality of the subclasses; as extensions of the parent class, subclasses are guaranteed to (at minimum) have the superclass' fields, methods, and functions.



# Arrow Functions in JavaScript
## Arrow Functions
These expressions lexically bind the this value while using less syntax than a typical function expression. Arrow functions are always anonymous.
Here are some basic examples of arrow function syntax:
(parameter) => {statements}
parameter => {statements}
parameter => expression
parameter => {return expression}

(param1, param2, ..., paramN) => {statements}
(param1, param2, ..., paramN) => expression
(param1, param2, ..., paramN) => {return expression}

```
'use strict';

const makeArray = (...values) => { return values };
console.log('Array:', makeArray(1, 2, 3, 4));
console.log('Array:', makeArray(1, 2, 3, 4, 5, 6));

const getSum = (a, b) => { return a + b };
console.log('1 + 2 =', getSum(1, 2));

const greeting = 'Hello, World.';
const capitalize = (myString) => { return myString.toUpperCase() };
console.log(greeting, '=>', capitalize(greeting));
```

## Using Arrow Functions
Let's look at some ways we can use arrow functions to make our code shorter.
Sum the Elements of an Array
While we can certainly iterate over an array and sum each value, we can also use the reduce function.


```
'use strict';
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce(function (a, b) {
    return a + b;
}, 0);
console.log('Array:', arr);
console.log('Sum:', sum);
```
Now, let's reduce the length of our code using an arrow function:
```
'use strict';
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((a, b) => { return a + b }, 0);
console.log('Array:', arr);
console.log('Sum:', sum);
```
Let's further reduce it by getting rid of the return:

```
'use strict';
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((a, b) => a + b, 0);
console.log('Array:', arr);
console.log('Sum:', sum);
```


