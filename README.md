# C# Guide

## Table of Contents

* [Hello World](#hello-world-example)
* [Variables](#variables)
* [Type Conversion](#type-conversion)
* [Operators](#operators)

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

```csharp
// Arithmetic Operators
var r = x + y; // Adds two operands
var r = x - y; // Subtracts second operand from the first
var r = x * y; // Multiplies both operands
var r = x / y; // Divides numerator by de-numerator
var r = x % y; // Modulus Operator and remainder of after an integer division
var r = x++; // Increment operator increases integer value by one
var r = x--; // Decrement operator decreases integer value by one

// Relational Operators
bool r = (x == y); // Checks if the values of two operands are equal
bool r = (x != y); // Checks if the values of two operands are equal or not
bool r = (x > y); // Checks if the value of left operand is greater than the value of right operand
bool r = (x < y); // Checks if the value of left operand is less than the value of right operand
bool r = (x >= y); // Checks if the value of left operand is greater than or equal to the value of right operand
bool r = (x <= y); // Checks if the value of left operand is less than or equal to the value of right operand

// Logical Operators
bool r = (x && y); // Logical AND operator
bool r = (x || y); // Logical OR Operator
bool r = !(x || y); // Logical NOT Operator
```

