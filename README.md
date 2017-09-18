# C# Guide

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

## Nullables
```csharp
int? x = null;
int? y = 2;

var z = x ?? 10; // Null Coalescing Operator
```

## Arrays
```csharp
double[] balance = new double[10]; // Initializing an Array
double[] marks = { 1, 2, 3}; // Assigning Values to an Array

balance[0] = 10;

var first = double[0];
```

## Contributing

Feel free to open tickets or send pull requests with improvements. Thanks in
advance for your help!

### How to Contribute?

Just follow the [contribution guidelines](https://github.com/andredarcie/csharp-guide/blob/master/CONTRIBUTING.md).

## License

The andredarcie/csharp-guide is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
