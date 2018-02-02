# C# Guide

> Discovering csharp through code samples. 😉

## Table of Contents

* [Hello World](#hello-world-example)
* [Comments](#comments)
* [Variables](#variables)
* [C# Keywords](#csharp-keywords)
* [Type Conversion](#type-conversion)
* [Sizeof](#sizeof)   
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
* [Checked](#checked-and-unchecked)
* [Delegate](#delegate)
* [Event](#event)
* [Explicit](#explicit)       
* [Extern](#extern)
* [Fixed](#fixed)
* [Goto](#goto)
* [Implicit](#implicit)      
* [Access Modifiers](#access-modifiers)
* [Is](#is)
* [Lock](#lock)
* [Object](#object)         
* [Override](#override)   
* [Readonly](#readonly)
* [Method Parameters](#method-parameters)
* [Sealed](#sealed)      
* [Stackalloc](#stackalloc)     
* [Static](#static)
* [This](#this)   
* [Typeof](#typeof)              
* [Unsafe](#unsafe)         
* [Using static](#using-static)
* [Virtual](#virtual)    
* [Volatile](#volatile)
* [Generics](#generics)  
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

## Comments

```csharp
/* The 
multiline
comments */

// Single-line comments
```
**[⬆ back to top](#table-of-contents)**

## Variables

```csharp
bool bo = true;   // True or false
byte by = 255;    // 0 to 255
char ch = 'a';    // U +0000 to U +ffff
decimal de = 1m;  // 128-bit precise decimal values
double do = 1d;   // 64-bit double-precision floating point type
float fl = 1f;    // 32-bit single-precision floating point type
int in = 1;       // -2,147,483,648 to 2,147,483,647
long lo = 1l;     // 64-bit signed integer type
sbyte sb = 1;     // -128 to 127
short sh = 1;     // -32,768 to 32,767
uint ui = 1;      // 0 to 4,294,967,295
ulong ul = 1;     // 0 to 18,446,744,073,709,551,615
ushort us = 1;    // 0 to 65,535

const int x = 0;  // Constant fields and locals aren't variables and may not be modified
```
**[⬆ back to top](#table-of-contents)**

## Csharp Keywords

```csharp
abstract       // Indicates that the thing being modified has a missing or incomplete implementation.
as             // Performs certain types of conversions between compatible reference types or nullable types. 
base           // Access members of the base class from within a derived class
bool           // Used to declare variables to store the Boolean values, true and false
break          // Terminates the closest enclosing loop or switch statement in which it appears
byte           // Denotes an integral type
case           // Chooses a single switch section to execute from a list of candidates based on a pattern match
catch          // Specify handlers for different exceptions
char           // Represent a Unicode character
checked        // Used to explicitly enable overflow checking for integral-type arithmetic 
               // operations and conversions
class          // Create your own custom types by grouping together variables of other types, methods and events
const          // Declare a constant field or a constant local
continue       // Passes control to the next iteration
decimal        // Indicates a 128-bit data type
default        // Can be used in the switch statement or in a default value expression
delegate       // Type that can be used to encapsulate a named or an anonymous method
do             // Executes a statement or a block of statements repeatedly until 
               // a specified expression evaluates to false
double         // Simple type that stores 64-bit floating-point values
else           // Identifies which statement to run based on the value of a Boolean expression.
enum           // Distinct type that consists of a set of named constants called the enumerator list.
event          // Used to declare an event in a publisher class
explicit       // User-defined type conversion operator that must be invoked with a cast
extern         // Modifier is used to declare a method that is implemented externally
false          // Represents boolean false
finally        // Can clean up any resources that are allocated in a try block
fixed          // Prevents the garbage collector from relocating a movable variable
float          // Signifies a simple type that stores 32-bit floating-point values
for            // Run a statement or a block of statements repeatedly until 
               // a specified expression evaluates to false
foreach, in    // Repeats a group of embedded statements for each element in an array or an object collection 
goto           // Transfers the program control directly to a labeled statement
if             // Identifies which statement to run based on the value of a Boolean expression.
implicit       // Used to declare an implicit user-defined type conversion operator
in             // (generic modifier) 
int            //
interface      //
internal       //
is             //
lock           //
long           //
namespace      //
new            //
null           //
object         //
operator       //
out            //
out            // (generic modifier)
override       //
params         //
private        //
protected      //
public         //
readonly       //
ref            //
return         //
sbyte          //
sealed         //
short          //
sizeof         //
stackalloc     //
static         //
string         //
struct         //
switch         //
this           //
throw          //
true           //
try            //
typeof         //
uint           //
ulong          //
unchecked      //
unsafe         //
ushort         //
using          //
using static   //
virtual        //
void           //
volatile       //
while          //
```
**[⬆ back to top](#table-of-contents)**

## Type Conversion

```csharp
x.ToBoolean();    // Converts a type to a Boolean value
x.ToByte();       // Converts a type to a byte
x.ToChar();       // Converts a type to a single Unicode character
x.ToDateTime();   // Converts a type (integer or string type) to date-time structures
x.ToDecimal();    // Converts a floating point or integer type to a decimal type
x.ToDouble();     // Converts a type to a double type
x.ToInt16();      // Converts a type to a 16-bit integer
x.ToInt32();      // Converts a type to a 32-bit integer
x.ToInt64();      // Converts a type to a 64-bit integer
x.ToSbyte();      // Converts a type to a signed byte type
x.ToSingle();     // Converts a type to a small floating point number
x.ToString();     // Converts a type to a string
x.ToType();       // Converts a type to a specified type
x.ToUInt16();     // Converts a type to an unsigned int type
x.ToUInt32();     // Converts a type to an unsigned long type
x.ToUInt64();     // Converts a type to an unsigned big integer
```

* As
```csharp
SomeType x = y as SomeType;
if (x != null)
{
  // Do something
}
```

**[⬆ back to top](#table-of-contents)**

## Sizeof

```csharp
// Constant value 4:  
int intSize = sizeof(int); 
```

**[⬆ back to top](#table-of-contents)**

## Operators

* Arithmetic Operators
```csharp
x + y;   // Adds two operands
x - y;   // Subtracts second operand from the first
x * y;   // Multiplies both operands
x / y;   // Divides numerator by de-numerator
x % y;   // Modulus Operator and remainder of after an integer division
x++;     // Increment operator increases integer value by one
x--;     // Decrement operator decreases integer value by one
```

* Relational Operators
```csharp
(x == y);   // Checks if the values of two operands are equal
(x != y);   // Checks if the values of two operands are equal or not
(x > y);    // Checks if the value of left operand is greater than the value of right operand
(x < y);    // Checks if the value of left operand is less than the value of right operand
(x >= y);   // Checks if the value of left operand is greater than or equal to the value of right operand
(x <= y);   // Checks if the value of left operand is less than or equal to the value of right operand
```

* Logical Operators
```csharp
(x && y);   // Logical AND operator
(x || y);   // Logical OR Operator
!(x || y);  // Logical NOT Operator
```

* Overload a built-in operator
```csharp
class Fraction
{
    int num, den;
    public Fraction(int num, int den)
    {
        this.num = num;
        this.den = den;
    }

    // overload operator +
    public static Fraction operator +(Fraction a, Fraction b)
    {
        return new Fraction(a.num * b.den + b.num * a.den,
           a.den * b.den);
    }
}
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

* Foreach, in
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

Books book1;   /* Declare Book1 of type Book */
book1.title = "Csharp Programming";
Console.WriteLine( "Book 1 title : {0}", Book1.title);

Books book2 = new Books() {title = "Hamlet", author = "William Shakespeare", subject = "tragedy", book_id = 1};
Console.WriteLine( "Book 1 title : {0}", Book2.title);
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

## Checked and Unchecked 

* Checked
```csharp
// The following statements are checked by default at compile time. They do not
// compile.
int1 = 2147483647 + 10;
int1 = ConstantMax + 10;

// If the previous sum is attempted in a checked environment, an 
// OverflowException error is raised.

// Checked expression.
Console.WriteLine(checked(2147483647 + ten));
```

* Unchecked
```csharp
// The following statements compile and run.
unchecked
{
   int1 = 2147483647 + 10;
}
```

**[⬆ back to top](#table-of-contents)**

## Delegate

```csharp
// Declare delegate, defines required signature:
delegate double MathAction(double num);

class DelegateTest
{
    // Regular method that matches signature:
    static double Double(double input)
    {
        return input * 2;
    }

    static void Main()
    {
        // Instantiate delegate with named method:
        MathAction multByTwo = Double;

        // Invoke delegate multByTwo:
        Console.WriteLine(multByTwo(4.5)); // 9

        // Instantiate delegate with anonymous method:
        MathAction square = delegate(double input)
        {
            return input * input;
        };

        Console.WriteLine(square(5)); // 25

        // Instantiate delegate with lambda expression
        MathAction cube = s => s * s * s;

        Console.WriteLine(cube(4.375)); // 83.740234375
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Event

```csharp
public class SampleEventArgs
{
    public SampleEventArgs(string s) { Text = s; }
    public String Text {get; private set;} // readonly
}
public class Publisher
{
    // Declare the delegate (if using non-generic pattern).
    public delegate void SampleEventHandler(object sender, SampleEventArgs e);

    // Declare the event.
    public event SampleEventHandler SampleEvent;

    // Wrap the event in a protected virtual method
    // to enable derived classes to raise the event.
    protected virtual void RaiseSampleEvent()
    {
        // Raise the event by using the () operator.
        if (SampleEvent != null)
            SampleEvent(this, new SampleEventArgs("Hello"));
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Explicit

```csharp
// Must be defined inside a class called Fahrenheit:
public static explicit operator Celsius(Fahrenheit fahr)
{
    return new Celsius((5.0f / 9.0f) * (fahr.degrees - 32));
}

Fahrenheit fahr = new Fahrenheit(100.0f);
Console.Write("{0} Fahrenheit", fahr.Degrees);
Celsius c = (Celsius)fahr;
```

**[⬆ back to top](#table-of-contents)**

## Extern

```csharp
// Used to declare a method that is implemented externally
[DllImport("avifil32.dll")]  
private static extern void AVIFileInit(); 
```

**[⬆ back to top](#table-of-contents)**

## Fixed

```csharp
class Point 
{ 
   public int x;
   public int y; 
}

// Fixed prevents the garbage collector from relocating a movable variable
// The fixed statement is only permitted in an unsafe context
unsafe static void TestMethod()
{
    // Variable pt is a managed variable, subject to garbage collection.
    Point pt = new Point();

    // Using fixed allows the address of pt members to be taken,
    // and "pins" pt so that it is not relocated.

    fixed (int* p = &pt.x)
    {
        *p = 1;
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Goto

```csharp
// Transfers the program control directly to a labeled statement
switch (option)
{
   case 1:
       Console.WriteLine("Case 1.");
       break;
   case 2:
       Console.WriteLine("Case 2.");
       goto case 1;
   case 3:
       Console.WriteLine("Case 3.");
       goto case 1;
   default:
       Console.WriteLine("Invalid selection.");
       break;
}

for (int i = 0; i < 10; i++)
{
    if (i = 5)
    {
        goto Found;
    }
}

Found:
   Console.WriteLine("Found 5!");
```

**[⬆ back to top](#table-of-contents)**

## Implicit

```csharp
class Digit
{
    public Digit(double d) { val = d; }
    public double val;
    // ...other members

    // User-defined conversion from Digit to double
    public static implicit operator double(Digit d)
    {
        return d.val;
    }
    //  User-defined conversion from double to Digit
    public static implicit operator Digit(double d)
    {
        return new Digit(d);
    }
}

// Use
// Implicit "double" operator
double num = dig;

// Implicit "Digit" operator
Digit dig2 = 12;
```

**[⬆ back to top](#table-of-contents)**

## Access Modifiers

```csharp
public // Access is not restricted

protected // Access is limited to the containing class or types derived from the containing class

internal // Access is limited to the current assembly

protected internal // Access is limited to the current assembly or types derived from the containing class

private // Access is limited to the containing type

private protected // Access is limited to the containing class or types derived from the containing class   
// within the current assembly
```

**[⬆ back to top](#table-of-contents)**

## Is

```csharp
if (obj is Person) { // Checks if an object is compatible with a given type
   // Do something if obj is a Person.
}
```

**[⬆ back to top](#table-of-contents)**

## Lock

```csharp
class Account  
{  
    decimal balance;  
    private Object thisLock = new Object();  

    public void Withdraw(decimal amount)  
    {  
        lock (thisLock) // Ensures that one thread does not enter a critical section of code 
                        // while another thread is in the critical section.
        {  
            if (amount > balance)  
            {  
                throw new Exception("Insufficient funds");  
            }  
            balance -= amount;  
        }  
    }  
} 
```

**[⬆ back to top](#table-of-contents)**

## Object

```csharp
// All types, predefined and user-defined, reference types and value types, 
// inherit directly or indirectly from Object
// You can assign values of any type to variables of type object

object bo = true;   // True or false
object by = 255;    // 0 to 255
object ch = 'a';    // U +0000 to U +ffff
object de = 1m;  // 128-bit precise decimal values
```

**[⬆ back to top](#table-of-contents)**

## Override

```csharp
abstract class ShapesClass
{
    abstract public int Area(); // Abstract method to override
}
class Square : ShapesClass
{
    int side = 0;
    public Square(int n)
    {
        side = n;
    }
    // Area method is required to avoid
    // a compile-time error.
    public override int Area() // Overridden implementation
    {
        return side * side;
    } 
}
```

**[⬆ back to top](#table-of-contents)**

## Readonly

```csharp
class Age
{
    readonly int _year;
    Age(int year)
    {
        _year = year;
    }
    void ChangeYear()
    {
        //_year = 1967; // Compile error if uncommented.
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Method Parameters

* Params
```csharp
public static void UseParams(params object[] list) // Variable number of arguments.
{
  for (int i = 0; i < list.Length; i++)
  {
      Console.Write(list[i] + " ");
  }
}

UseParams(1, 'a', "test");
```

* Ref
```csharp
class RefExample
{
    static void Method(ref int i)
    {
        i = i + 44;
    }

    static void Main()
    {
        int val = 1;
        Method(ref val);
        Console.WriteLine(val); // 45
    }
}
```

* Out
   - Parameter modifier
   ```csharp
   class OutExample
   {
      static void Method(out int i)
      {
         i = 44;
      }

      static void Main()
      {
         int value;
         Method(out value);
         Console.WriteLine(value);     // value is now 44
      }
   }
   ```
   - Generic type parameter declarations 
   ```csharp
   // Covariant interface.
   interface ICovariant<out R> { }

   // Extending covariant interface.
   interface IExtCovariant<out R> : ICovariant<R> { }

   // Implementing covariant interface.
   class Sample<R> : ICovariant<R> { }

   class Program
   {
       static void Test()
       {
           ICovariant<Object> iobj = new Sample<Object>();
           ICovariant<String> istr = new Sample<String>();

           // You can assign istr to iobj because
           // the ICovariant interface is covariant.
           iobj = istr;
       }
   }
   ```

**[⬆ back to top](#table-of-contents)**

## Sealed

```csharp
class A {}      
sealed class B : A {} // No class can inherit from class B

class X
{
    protected virtual void F() { Console.WriteLine("X.F"); }
    protected virtual void F2() { Console.WriteLine("X.F2"); }
}
class Y : X
{
    sealed protected override void F() { Console.WriteLine("Y.F"); }
    protected override void F2() { Console.WriteLine("Y.F2"); }
}
class Z : Y
{
    // Attempting to override F causes compiler error CS0239.
    // protected override void F() { Console.WriteLine("C.F"); }

    // Overriding F2 is allowed.
    protected override void F2() { Console.WriteLine("Z.F2"); }
}
```

**[⬆ back to top](#table-of-contents)**

## Stackalloc

```csharp
class Fibonacci
{
    static unsafe void Main() // Unsafe code context
    {
        const int arraySize = 20;
        int* fib = stackalloc int[arraySize]; // Allocate a block of memory on the stack
        int* p = fib;
        // The sequence begins with 1, 1.
        *p++ = *p++ = 1;
        for (int i = 2; i < arraySize; ++i, ++p)
        {
            // Sum the previous two numbers.
            *p = p[-1] + p[-2];
        }
        for (int i = 0; i < arraySize; ++i)
        {
            Console.WriteLine(fib[i]);
        }

        // Keep the console window open in debug mode.
        System.Console.WriteLine("Press any key to exit.");
        System.Console.ReadKey();
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Static 

```csharp
// Declare a static member, which belongs to the type itself rather than to a specific object. 
static class CompanyEmployee
{
    public static void DoSomething() { /*...*/ }
    public static void DoSomethingElse() { /*...*/  }
}

CompanyEmployee.DoSomething();
CompanyEmployee.DoSomethingElse();

class Employee
{
   public static string name;
}

Employee.name
```

**[⬆ back to top](#table-of-contents)**

## This

```csharp
// Use to qualify members hidden by similar names
public Employee(string name)
{
    this.name = name;
}

// Use to pass an object as a parameter to other methods
CalcTax(this);

// Use to declare indexers
public int this[int param]
{
    get { return array[param]; }
    set { array[param] = value; }
}
```

**[⬆ back to top](#table-of-contents)**

## Typeof

```csharp
System.Type type = typeof(int); // System.Int32
```

**[⬆ back to top](#table-of-contents)**

## Unsafe

```csharp
unsafe static void FastCopy(byte[] src, byte[] dst, int count)  
{  
    // Unsafe context: can use pointers here.  
}  
```

**[⬆ back to top](#table-of-contents)**

## Using static

```csharp
using static System.Console; // Designates a type whose static members you can access without specifying a type name. 

class Program 
{ 
    static void Main() 
    { 
        WriteLine("Hello world!"); // Without specifying Console
    } 
}
```

**[⬆ back to top](#table-of-contents)**

## Virtual

```csharp
class MyBaseClass
{
    // virtual auto-implemented property. Overrides can only
    // provide specialized behavior if they implement get and set accessors.
    public virtual string Name { get; set; }

    // ordinary virtual property with backing field
    private int num;
    public virtual int Number
    {
        get { return num; }
        set { num = value; }
    }
}


class MyDerivedClass : MyBaseClass
{
    private string name;

   // Override auto-implemented property with ordinary property
   // to provide specialized accessor behavior.
    public override string Name
    {
        get
        {
            return name;
        }
        set
        {
            if (value != String.Empty)
            {
                name = value;
            }
            else
            {
                name = "Unknown";
            }
        }
    }

}
```

**[⬆ back to top](#table-of-contents)**

## Volatile

```csharp
class VolatileTest
{
    public volatile int i; // Indicates that a field might be modified by multiple 
                           // threads that are executing at the same time

    public void Test(int _i)
    {
        i = _i;
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Generics 

```csharp
// Declare the generic class.
public class GenericList<T>
{
    void Add(T input) { }
}
class TestGenericList
{
    private class ExampleClass { }
    static void Main()
    {
        // Declare a list of type int.
        GenericList<int> list1 = new GenericList<int>();

        // Declare a list of type string.
        GenericList<string> list2 = new GenericList<string>();

        // Declare a list of type ExampleClass.
        GenericList<ExampleClass> list3 = new GenericList<ExampleClass>();
    }
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
