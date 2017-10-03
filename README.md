# C# Guide

> Discovering csharp through code samples. 😉

## Table of Contents

* [Hello World](#hello-world-example)
* [Variables](#variables)
* [Type Conversion](#type-conversion)
* [Operators](#operators)
* [Decision Making](#decision-making)
* [Loops](#loops)
* [Methods](#methods)
* [Nullables](#nullables)
* [Arrays](#arrays)
* [Strings](#strings)
* [Structures](#structures)
* [Enums](#enums)
* [Classes](#classes)
* [Polymorphism](#polymorphism)
* [Inheritance](#inheritance)
* [Abstract](#abstract)
* [Interface](#interface)
* [Exception Handling](#exception-handling)
* [Collections](#collections)
* [Contributing](#contributing)
* [License](#license)

## Hello World Example

```csharp
using System;
namespace HelloWorldApplication
{
   class HelloWorld
   {
      static void Main(string[] args)
      {
         Console.WriteLine("Hello World");
      }
   }
}
```
**[⬆ back to top](#table-of-contents)**

## Variables

```csharp
bool bo = true; // True or false
byte by = 255; // 0 to 255
char ch = 'a'; // U +0000 to U +ffff
decimal de = 1m; // 128-bit precise decimal values
double do = 1d; // 64-bit double-precision floating point type
float fl = 1f; // 32-bit single-precision floating point type
int in = 1; // -2,147,483,648 to 2,147,483,647
long lo = 1l; // 64-bit signed integer type
sbyte sb = 1; // -128 to 127
short sh = 1; // -32,768 to 32,767
uint ui = 1; // 0 to 4,294,967,295
ulong ul = 1; // 0 to 18,446,744,073,709,551,615
ushort us = 1; // 0 to 65,535
```
**[⬆ back to top](#table-of-contents)**

## Type Conversion

```csharp
x.ToBoolean(); // Converts a type to a Boolean value
x.ToByte(); // Converts a type to a byte
x.ToChar(); // Converts a type to a single Unicode character
x.ToDateTime(); // Converts a type (integer or string type) to date-time structures
x.ToDecimal(); // Converts a floating point or integer type to a decimal type
x.ToDouble(); // Converts a type to a double type
x.ToInt16(); // Converts a type to a 16-bit integer
x.ToInt32(); // Converts a type to a 32-bit integer
x.ToInt64(); // Converts a type to a 64-bit integer
x.ToSbyte(); // Converts a type to a signed byte type
x.ToSingle(); // Converts a type to a small floating point number
x.ToString(); // Converts a type to a string
x.ToType(); // Converts a type to a specified type
x.ToUInt16(); // Converts a type to an unsigned int type
x.ToUInt32(); // Converts a type to an unsigned long type
x.ToUInt64(); // Converts a type to an unsigned big integer
```
**[⬆ back to top](#table-of-contents)**

## Operators

* Arithmetic Operators
```csharp
x + y; // Adds two operands
x - y; // Subtracts second operand from the first
x * y; // Multiplies both operands
x / y; // Divides numerator by de-numerator
x % y; // Modulus Operator and remainder of after an integer division
x++; // Increment operator increases integer value by one
x--; // Decrement operator decreases integer value by one
```

* Relational Operators
```csharp
(x == y); // Checks if the values of two operands are equal
(x != y); // Checks if the values of two operands are equal or not
(x > y); // Checks if the value of left operand is greater than the value of right operand
(x < y); // Checks if the value of left operand is less than the value of right operand
(x >= y); // Checks if the value of left operand is greater than or equal to the value of right operand
(x <= y); // Checks if the value of left operand is less than or equal to the value of right operand
```

* Logical Operators
```csharp
(x && y); // Logical AND operator
(x || y); // Logical OR Operator
!(x || y); // Logical NOT Operator
```
**[⬆ back to top](#table-of-contents)**

## Decision Making

* If statement
```csharp
if(boolean_expression)
{
   /* boolean expression is true */
}
```

* If else statement
```csharp
if(boolean_expression)
{
   /* boolean expression is true */
}
else
{
   /* expression is false */
}
```

* If else statement
```csharp
if(boolean_expression1)
{
   /* boolean expression 1 is true */
}
else if (boolean_expression2)
{
   /* boolean expression 2 is true */
}
else
{
   /* expression 1 and 2 are false */
}
```

* Nested if statements
```csharp
if( boolean_expression1)
{
   /* boolean expression 1 is true */
   if(boolean_expression2)
   {
      /* expression 2 is true */
   }
}
```

* Switch statement
```csharp
switch(place) {
   case 1  :
      Console.WriteLine("First!");
      break; 
   case 2  :
      Console.WriteLine("Second!");
      break; 
   default : /* Optional */
      Console.WriteLine("Invalid place!");
}
```
**[⬆ back to top](#table-of-contents)**

## Loops

* While loop
```csharp
while(condition)
{
   Console.WriteLine("Hello!");
}
```

* For loop
```csharp
for (int x = 0; x < 10; x++)
{
   Console.WriteLine("value of x: {0}", x);
}
```

* Do...while loop
```csharp
int x = 0;

do
{
   Console.WriteLine("value of x: {0}", x);
   x++;
} 
while (x < 10);
```

* Nested loops
```csharp
for (int x = 0; x < 10; x++)
{
   for (int y = 0; y < 10; y++) 
   {
      Console.WriteLine("x: {0}, y: {1}", x, y);
   }
}
```

* Break Statement
```csharp
int x = 0;

while (x < 10)
{
   Console.WriteLine("value of x: {0}", x);
   x++;
   if (x > 5)
   {
      /* terminate the loop using break statement */
      break;
   }
}
```

* Continue Statement
```csharp
int x = 0;

do
{
   if (x == 5)
   {
      x++;
      /* skip the iteration */
      continue;
   }
   Console.WriteLine("value of x: {0}", x);
   x++;
} 
```
**[⬆ back to top](#table-of-contents)**

## Methods
```csharp
using System;
namespace CalculatorApplication
{
   class Calculator
   {
      public int Sum(int x, int y)
      {
         return x + y;
      }
      static void Main(string[] args)
      {
         var result = Sum(2, 2);
         Console.WriteLine("result: {0}", result);
      }
   }
}
```
**[⬆ back to top](#table-of-contents)**

## Nullables
```csharp
int? x = null;
int? y = 2;

var z = x ?? 10; // Null Coalescing Operator
```
**[⬆ back to top](#table-of-contents)**

## Arrays
```csharp
double[] balance = new double[10]; // Initializing an Array
double[] marks = { 1, 2, 3 }; // Assigning Values to an Array

balance[0] = 10;

var first = balance[0];
```
**[⬆ back to top](#table-of-contents)**

## Strings
```csharp
string name = "John doe";
Console.WriteLine("Name: {0}", name);
```
**[⬆ back to top](#table-of-contents)**

## Structures
```csharp
struct Books
{
   public string title;
   public string author;
   public string subject;
   public int book_id;
}; 

Books Book1;   /* Declare Book1 of type Book */
Book1.title = "Csharp Programming";
Console.WriteLine( "Book 1 title : {0}", Book1.title);
```
**[⬆ back to top](#table-of-contents)**

## Enums
```csharp
enum Days { Sun, Mon, tue, Wed, thu, Fri, Sat };

Console.WriteLine("Monday: {0}", (int)Days.Mon);
```
**[⬆ back to top](#table-of-contents)**

## Classes
```csharp
class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
    
    public Person(int age, string name)
    {
        Age = age;
        Name = name;
    }

    public int Talk()
    {
        return "Hello!";
    }
}

public class Application
{
    static void Main()
    {
      Person person = new Person("Bill", 42);
      Console.WriteLine("person Name = {0} Age = {1}", person.Name, person.Age);
    }
}
```
**[⬆ back to top](#table-of-contents)**

## Polymorphism
```csharp
public class Shape
{
    // A few example members
    public int X { get; private set; }
    public int Y { get; private set; }
    public int Height { get; set; }
    public int Width { get; set; }
   
    // Virtual method
    public virtual void Draw()
    {
        Console.WriteLine("Performing base class drawing tasks");
    }
}

class Circle : Shape
{
    public override void Draw()
    {
        // Code to draw a circle...
        Console.WriteLine("Drawing a circle");
        base.Draw();
    }
}
class Rectangle : Shape
{
    public override void Draw()
    {
        // Code to draw a rectangle...
        Console.WriteLine("Drawing a rectangle");
        base.Draw();
    }
}
```
**[⬆ back to top](#table-of-contents)**

## Inheritance
```csharp
class Shape 
{
   public void setWidth(int w)
   {
      width = w;
   }
   public void setHeight(int h)
   {
      height = h;
   }
   protected int width;
   protected int height;
}

// Derived class
class Rectangle: Shape
{
   public int getArea()
   { 
      return (width * height); 
   }
}
```
**[⬆ back to top](#table-of-contents)**

## Abstract
```csharp
abstract class BaseClass
{
    protected int _x = 100;
    protected int _y = 150;
    public abstract void AbstractMethod();
}

class DerivedClass : BaseClass
{
    public override void AbstractMethod()
    {
        _x++;
        _y++;
    }
}
```
**[⬆ back to top](#table-of-contents)**

## Interface 
```csharp
public interface IPerson
{
    // interface members
    public int Talk();
}

class Person : IPerson
{
    public string Name { get; set; }
    public int Age { get; set; }
    
    public Person(int age, string name)
    {
        Age = age;
        Name = name;
    }

    public int Talk()
    {
        return "Hello!";
    }
}
```
**[⬆ back to top](#table-of-contents)**

## Exception Handling
```csharp
try
{
   // statements causing exception
}
catch( ExceptionName e1 )
{
   // error handling code
}
catch( ExceptionName e2 )
{
   // error handling code
}
catch( ExceptionName eN )
{
   // error handling code
}
finally
{
   // statements to be executed
}
```
**[⬆ back to top](#table-of-contents)**

## Collections

### Classes
* ArrayList
```csharp
ArrayList numbers = new ArrayList();
numbers.Add(1);
numbers.Add(2);
numbers.Add(3);

Console.WriteLine("Count: {0}", numbers.Count);

foreach (int number in numbers)
{
   Console.Write(number + " ");
}
```

* Hashtable
```csharp
Hashtable list = new Hashtable();
list.Add("01", "Emma");
list.Add("02", "William");
list.Add("03", "Mia");

if (list.ContainsValue("Mia"))
{
   Console.WriteLine("This name is already in the list");
}

ICollection keys = list.Keys;
         
foreach (string key in keys)
{
   Console.WriteLine(key + ": " + list[key]);
}
```

* SortedList
```csharp
SortedList list = new SortedList();
list.Add("01", "Emma");
list.Add("02", "William");
list.Add("03", "Mia");

ICollection keys = list.Keys;

foreach (string key in keys)
{
   Console.WriteLine(key + ": " + list[key]);
}
```

* Stack
```csharp
Stack st = new Stack();
         
st.Push('A');
st.Push('M');
st.Push('G');

foreach (char c in st)
{
   Console.Write(c + " ");
}

st.Pop();
st.Pop();
st.Pop();
```

* Queue
```csharp
Queue queue = new Queue();
         
queue.Enqueue('A');
queue.Enqueue('M');
queue.Enqueue('G');

foreach (char item in queue)
{
   Console.WriteLine(item + " ");
}

char removedValue = (char)queue.Dequeue();
```

* BitArray
```csharp
bool[] array = new bool[4];
array[0] = true;
array[1] = false;
array[2] = true;
array[3] = false;

BitArray bitArray = new BitArray(array);

foreach (bool bit in bitArray)
{
   Console.WriteLine(bit);
}
```
**[⬆ back to top](#table-of-contents)**

## Contributing

Feel free to open tickets or send pull requests with improvements. Thanks in
advance for your help!

### How to Contribute?

Just follow the [contribution guidelines](https://github.com/andredarcie/csharp-guide/blob/master/CONTRIBUTING.md).

## License

The andredarcie/csharp-guide is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
