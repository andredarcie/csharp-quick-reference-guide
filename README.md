# C# Guide

## Table of Contents

* [Hello World](#hello-world-example)
* [Variables](#variables)

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
