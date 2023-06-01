# C# Quick Reference Guide

> Discovering csharp through code samples. 😉

## Table of Contents

- [Hello World](#hello-world)
- [Comments](#comments)
- [Variables](#variables)
- [By Feature](#by-feature)
- [Type Conversion](#type-conversion)
- [Sizeof](#sizeof)
- [Operators](#operators)
- [Decision Making](#decision-making)
- [Loops](#loops)
- [Methods](#methods)
- [Nullables](#nullables)
- [Arrays](#arrays)
- [Strings](#strings)
- [Structures](#structures)
- [Enums](#enums)
- [Classes](#classes)
- [Polymorphism](#polymorphism)
- [Inheritance](#inheritance)
- [Abstract](#abstract)
- [Interface](#interface)
- [Exception Handling](#exception-handling)
- [Checked](#checked-and-unchecked)
- [Delegate](#delegate)
- [Event](#event)
- [Explicit](#explicit)
- [Extern](#extern)
- [Fixed](#fixed)
- [Goto](#goto)
- [Implicit](#implicit)
- [Access Modifiers](#access-modifiers)
- [Is](#is)
- [Lock](#lock)
- [Override](#override)
- [Readonly](#readonly)
- [Method Parameters](#method-parameters)
- [Sealed](#sealed)
- [Stackalloc](#stackalloc)
- [Static](#static)
- [This](#this)
- [Typeof](#typeof)
- [Unsafe](#unsafe)
- [Using static](#using-static)
- [Virtual](#virtual)
- [Volatile](#volatile)
- [Generics](#generics)
- [C# Keywords](#csharp-keywords)
- [Contextual Keywords](#contextual-keywords)
- [Contributing](#contributing)
- [License](#license)

## By Version

- <a name="csharp-2"></a>C# 2.0

  - [Generics](#generics)
  - [Partial types](#partial-types)
  - [Anonymous methods](#anonymous-methods)
  - [Iterators](#iterators)
  - [Nullable types](#nullables)
  - [Getter and setter separate accessibility](#getter-and-setter-separate-accessibility)
  - [Method group conversions (delegates)](#method-group-conversions)
  - [Covariance and Contravariance for delegates](#covariance-and-contravariance-for-delegates)
  - [Static classes](#static)
  - [Delegate inference](#delegate-inference)
  - Namespace alias (TODO)

- <a name="csharp-3"></a>C# 3.0
  - [Implicitly typed local variables](#implicitly-typed-local-variables)
  - [Object and collection initializers](#object-and-collection-initializers)
  - [Auto-Implemented properties](#auto-implemented-properties)
  - [Anonymous types](#anonymous-types)
  - [Extension methods](#extension-methods)
  - [Query expressions](#query-expressions)
  - [Lambda expressions](#lambda-expressions)
  - [Expression trees](#expression-trees)
  - [Partial methods](#partial-methods)
- <a name="csharp-4"></a>C# 4.0
  - [Dynamic binding](#dynamic-binding)
  - [Named and optional arguments](#named-and-optional-arguments)
  - [Generic co and contravariance](#generic-co-and-contravariance)
- <a name="csharp-5"></a>C# 5.0

  - [Asynchronous methods](#asynchronous-methods)
  - [Caller info attributes](#caller-info-attributes)

- <a name="csharp-6"></a>C# 6.0

  - [Compiler as a service Roslyn](#compiler-as-a-service-roslyn)
  - [Import of static type members into namespace](#import-of-static-type-members-into-namespace)
  - [Exception filters](#exception-handling)
  - [Await in catch finally blocks](#await-in-catch-finally-blocks)
  - [Auto property initializers](#auto-property-initializers)
  - [Default values for getter only properties](#default-values-for-getter-only-properties)
  - [Expression-bodied members](#expression-bodied-members)
  - [Null propagator (null-conditional operator, succinct null checking)](<#null-propagator-(null-conditional-operator,-succinct-null-checking)>)
  - [String interpolation](#string-interpolation)
  - [nameof operator](#nameof-operator)
  - [Dictionary initializer](#dictionary-initializer)

- <a name="csharp-7"></a>C# 7.0

  - [Out variables](#method-parameters)
  - [Tuples](#tuples)
  - [Discards](#discards)
  - [Pattern matching](#pattern-matching)
  - [Deconstruction](#deconstruction)
  - [Ref returns and locals](#ref-returns-and-locals)
  - [Local functions](#local-functions)
  - [More expression-bodied members](#more-expression-bodied-members)
  - [throw Expressions](#throw-expressions)
  - [Generalized async return types](#generalized-async-return-types)
  - [Numeric literal syntax improvements](#numeric-literal-syntax-improvements)

- <a name="csharp-71"></a>C# 7.1

  - [Async main](#async-main)
  - Default literal expressions (TODO)
  - [Inferred tuple element names](#inferred-tuple-element-names)

- <a name="csharp-72"></a>C# 7.2
  - Reference semantics with value types (TODO)
  - [Non-trailing named arguments](#non-trailing-named-arguments)
  - Leading underscores in numeric literals (TODO)
  - [private protected access modifier](#private-protected-access-modifier)
- <a name="csharp-73"></a>C# 7.3
  - More efficient safe code (TODO)
  - Existing features better (TODO)
- <a name="csharp-8"></a>C# 8.0

  - [Readonly members](#readonly-members)
  - [Default interface members](#default-interface-members)
  - [Pattern matching enhancements](#pattern-matching-enhancements)
  - [Using declarations](#using-declarations)
  - [Static local functions](#static-local-functions)
  - [Disposable ref structs](#disposable-ref-structs)
  - [Nullable reference types](#nullable-reference-types)
  - [Asynchronous streams](#asynchronous-streams)
  - [Indices and ranges](#indices-and-ranges)

- <a name="csharp-9"></a>C# 9.0
  - [Record types](#record-types)
  - [Init only setters](#init-only-setters)
  - [Top-level statements](#top-level-statements)
  - [Pattern matching enhancements](#pattern-matching-enhancements)
  - [Performance and interop](#performance-and-interop)
  - [Fit and finish features](#fit-and-finish-features)
  - [Support for code generators](#support-for-code-generators)

- <a name="csharp-10"></a>C# 10.0
  - [Global using directives](#global-using-directives)
  - [File-scoped Namespace Declaration](#file-scoped-namespace-declaration)
  - [Implicit Using statements](#implicit-using-statements)
  - [Custom Interpolated String Handlers](#custom-interpolated-string-handlers)
  - [Extended Property Patterns](#extended-property-patterns)
  - [Improvements of Structure Types](#improvements-of-structure-types)
  - [Lambda Expression Improvements](#lambda-expression-improvements)
  - [Constant Interpolated Strings](#constant-interpolated-strings)
  - [Record Types Can Seal ToString](#record-types-can-seal-tostring)
  - [Assignment Declaration in the Same Deconstruction](#assignment-declaration-in-the-same-deconstruction)
  - [DateOnly](#dateonly)
  - [TimeOnly](#timeonly)
  - [Check Strings for Null](#check-strings-for-null)
  - [Process Data in Chunks](#process-data-in-chunks)
  - [LINQ Extensions](#linq-extensions)
  - [PriorityQueue](#priorityqueue)

- <a name="csharp-11"></a>C# 11.0
  - [Require Members](#require-members)
  - [Raw string literals](#raw-string-literals)
  - [Generic Attributes](#generic-attributes)
  - [Extended nameof scope](#extended-nameof-scope)
  - [Pattern match on a constant string](#pattern-match-on-a-constant-string)
  - [Auto-default struct](#auto-default-struct)
  - [List patterns](#list-patterns)
  - [UTF-8 string literals](#utf-8-string-literals)

**[⬆ back to top](#table-of-contents)**

## Hello World

<sup>[[Run example](https://repl.it/@andredarcie/Hello-World)]</sup>

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

## Top-level statements

<sup>[[C# 9.0](#csharp-9)]</sup>

```csharp
System.Console.WriteLine("Hello World");
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

<sup>[[Run example](https://repl.it/@andredarcie/Variables)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/types)]</sup>

```csharp
class MainClass {

  // Value type
  enum myEnum { Zero, One };

  static void Main () {

    // Value types
    bool myBool = true; // True or false
    byte myByte = 255; // 0 to 255
    char myChar = 'a'; // U +0000 to U +ffff
    decimal myDecimal = 1m; // 128-bit decimal values
    double myDouble = 1d; // 64-bit double-precision
    float myFloat = 1f; // 32-bit single-precision
    int myInt = 1; // -2,147,483,648 to 2,147,483,647
    long myLong = 1L; // 64-bit signed integer type
    sbyte mySbyte = 1; // -128 to 127
    short myShort = 1; // -32,768 to 32,767
    uint myUint = 1; // 0 to 4,294,967,295
    ulong myUlong = 1; // 0 to 18,446,744,073,709,551,615
    ushort myUshort = 1; // 0 to 65,535

    // Reference types
    dynamic myDynamic = 1; // Bypass compile-time type checking
    object myObject = new myClass();
    string myString = "test";

    // Pointer types
    /*
    unsafe {
      int* myIntVariable; // Int variable address
    }
    */
  }

  // Reference type
  class myClass { };
  interface myInterface { };
  delegate void myDelegate();
}
```

**[⬆ back to top](#table-of-contents)**

## Type Conversion

```csharp
Convert.ToBoolean(x);    // Converts a type to a Boolean value
Convert.ToByte(x);       // Converts a type to a byte
Convert.ToChar(x);       // Converts a type to a single Unicode character
Convert.ToDateTime(x);   // Converts a type (integer or string type) to date-time structures
Convert.ToDecimal(x);    // Converts a floating point or integer type to a decimal type
Convert.ToDouble(x);     // Converts a type to a double type
Convert.ToInt16(x);      // Converts a type to a 16-bit integer
Convert.ToInt32(x);      // Converts a type to a 32-bit integer
Convert.ToInt64(x);      // Converts a type to a 64-bit integer
Convert.ToSbyte(x);      // Converts a type to a signed byte type
Convert.ToSingle(x);     // Converts a type to a small floating point number
Convert.ToString(x);     // Converts a type to a string
Convert.ToType(x);       // Converts a type to a specified type
Convert.ToUInt16(x);     // Converts a type to an unsigned int type
Convert.ToUInt32(x);     // Converts a type to an unsigned long type
Convert.ToUInt64(x);     // Converts a type to an unsigned big integer
```

- As

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

- Arithmetic Operators

```csharp
x + y   // Adds two operands
x - y   // Subtracts second operand from the first
x * y   // Multiplies both operands
x / y   // Divides numerator by de-numerator
x % y   // Modulus Operator and remainder of after an integer division
x++     // Increment operator increases integer value by one
x--     // Decrement operator decreases integer value by one
```

- Relational Operators

```csharp
(x == y)   // Checks if the values of two operands are equal
(x != y)   // Checks if the values of two operands are equal or not
(x > y)    // Checks if the value of left operand is greater than the value of right operand
(x < y)    // Checks if the value of left operand is less than the value of right operand
(x >= y)   // Checks if the value of left operand is greater than or equal to the value of right operand
(x <= y)   // Checks if the value of left operand is less than or equal to the value of right operand
```

- Logical Operators

```csharp
(x && y)   // Logical AND operator
(x || y)   // Logical OR Operator
!(x || y)  // Logical NOT Operator
```

- Overload a built-in operator  
  <sup>[[Run example](https://repl.it/@andredarcie/Overload-a-built-in-operator)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/operator)]</sup>

```csharp
using System;

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

    // user-defined conversion from Fraction to double
    public static implicit operator double(Fraction f)
    {
        return (double)f.num / f.den;
    }

    static void Main () {
        Fraction x = new Fraction(1, 2);
        Fraction y = new Fraction(3, 4);

        Console.WriteLine ((double)x + y);
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Decision Making

- If statement  
  <sup>[[Run example](https://repl.it/@diguifi/Decision-Making-1)]</sup>

```csharp
if(boolean_expression)
{
   /* boolean expression is true */
}
```

- If else statements  
  <sup>[[Run example](https://repl.it/@diguifi/Decision-Making-2)]</sup>

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

- If, else if, else statements  
  <sup>[[Run example](https://repl.it/@diguifi/Decision-Making-3)]</sup>

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

- Nested if statements  
  <sup>[[Run example](https://repl.it/@diguifi/Decision-Making-4)]</sup>

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

- Switch statement  
  <sup>[[Run example](https://repl.it/@diguifi/Decision-Making-5)]</sup>

```csharp
switch(place)
{
   case 1  :
      Console.WriteLine("First!");
      break;
   case 2  :
      Console.WriteLine("Second!");
      break;
   default : /* Optional */
      Console.WriteLine("Invalid place!");
      break;
}
```

**[⬆ back to top](#table-of-contents)**

## Loops

- While loop  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-1)]</sup>

```csharp
while(condition)
{
   Console.WriteLine("Hello!");
}
```

- For loop  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-2)]</sup>

```csharp
for (int x = 0; x < 10; x++)
{
   Console.WriteLine($"value of x: {x}");
}
```

- Do...while loop  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-3)]</sup>

```csharp
int x = 0;

do
{
   Console.WriteLine($"value of x: {x}");
   x++;
}
while (x < 10);
```

- Nested loops  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-4)]</sup>

```csharp
for (int x = 0; x < 10; x++)
{
   for (int y = 0; y < 10; y++)
   {
      Console.WriteLine($"x: {x}, y: {y}");
   }
}
```

- Break Statement  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-5)]</sup>

```csharp
int x = 0;

while (x < 10)
{
   Console.WriteLine($"value of x: {x}");
   x++;
   if (x > 5)
   {
      /* terminate the loop using break statement */
      break;
   }
}
```

- Continue Statement  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-6)]</sup>

```csharp
int x = 0;

do
{
   if (x == 5)
   {
      x++;
      /* skips printing 6 */
      continue;
   }
   x++;
   Console.WriteLine($"value of x: {x}");
}
while (x < 10);
```

- Foreach, in  
  <sup>[[Run example](https://repl.it/@diguifi/Loops-7)]</sup>

```csharp
ArrayList numbers = new ArrayList();
numbers.Add(1);
numbers.Add(2);
numbers.Add(3);

Console.WriteLine($"Count: {numbers.Count}");

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

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
int? x = null;
int? y = 2;

int? variableName = null;
double? variableName = null;
bool? variableName = null;
int?[] arr = new int?[10];

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

- Exception filters
  <sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
try
  {
    throw new Exception("Exception 1");
  }
  catch(Exception ex) when(ex.Message == "Exception 2")
  {
    Console.WriteLine("caught Exception 2");
  }
  catch(Exception ex) when(ex.Message == "Exception 1")
  {
    Console.WriteLine("caught Exception 1");
  }
```

**[⬆ back to top](#table-of-contents)**

## Checked and Unchecked

- Checked

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

- Unchecked

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

- Params

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

- Ref

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

- Out
  <sup>[[C# 7.0](#csharp-7)]</sup>

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
using static System.Console; // Designates a type whose static members you can
                             // access without specifying a type name.

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

<sup>[[C# 2.0](#csharp-2)]</sup>

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

## Partial Types

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
// Declare first partial class
public partial class MyClass
{
    int x;
}

// Declare second partial class
public partial class MyClass
{
    int y;
}

// Declare third partial class
public partial class MyClass
{
    public MyClass()
    {
          this.x = 10;
          this.y = 20;
    }
}

// The three partials will generate just one class after compiled
```

**[⬆ back to top](#table-of-contents)**

## Anonymous methods

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
// Declare a delegate.
delegate void Printer(string s);

// Instantiate the delegate type using an anonymous method.
Printer p = delegate(string j)
{
   System.Console.WriteLine(j);
};

// Results from the anonymous delegate call.
p("The delegate using the anonymous method is called.");

// Output: The delegate using the anonymous method is called.
```

**[⬆ back to top](#table-of-contents)**

## Iterators

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
// Iterator can be used to step through collections such as lists and arrays
class Department
{
   private List<Employees> _employees;

   public IEnumerator<Employees> GetEnumerator()
   {
      foreach (Employees emp in _employees)
      yield return emp;
   }
}

static void Main(string[] args)
{
   Department dept = new Department("MyDepartment");
   foreach (Employees emp in dept)
   {
      //...
   }
}
```

**[⬆ back to top](#table-of-contents)**

## Getter and setter separate accessibility

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
class Customer
{ // Different accessibility on get and set accessors using accessor-modifier
   public string Name { get; protected set; }
}
```

**[⬆ back to top](#table-of-contents)**

## Method group conversions

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
// suppose we have a method called RemoveSpaces(string s) and a delegate called Del
// to assign a method to the delegate:
Del d = RemoveSpaces;
```

## Covariance and Contravariance for delegates

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
static object GetObject() { return null; }
static void SetObject(object obj) { }

static string GetString() { return “”; }
static void SetString(string str) { }

// Covariance. A delegate specifies a return type as object,
// but I can assign a method that returns a string.
Func<object> del = GetString;

// Contravariance. A delegate specifies a parameter type as string,
// but I can assign a method that takes an object.
Action<string> del2 = SetObject;
```

**[⬆ back to top](#table-of-contents)**

## Delegate inference

<sup>[[C# 2.0](#csharp-2)]</sup>

```csharp
//create a delegate instance without the new keyword part
delegate void SomeAction();
SomeAction newStyle = SayHello;
```

**[⬆ back to top](#table-of-contents)**

## Implicitly typed local variables

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// compiled as an int
var foo = 5;

// compiled as a string
var foo = "Hello";

// compiled as int[]
var foo = new[] { 0, 1, 2 };

// expr is compiled as IEnumerable<Customer> or perhaps IQueryable<Customer>
var foo =
    from c in customers
    where c.City == "London"
    select c;

// compiled as an anonymous type
var foo = new { Name = "Terry", Age = 34 };

// compiled as List<int>
var foo = new List<int>();
```

**[⬆ back to top](#table-of-contents)**

## Object and collection initializers

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// Object initializer
class Customer
{
   public string Name { get; set; }
   public int Age { get; set; }
}

Customer foo = new Customer { Name = "Spock", Age = 21 };

// Anonymous object initializer
var bar = new  { Name = "Spock", Age = 21 };

// Collection initializer
List<Customer> foos = new List<Customer>
{
    new Customer { Name = "John", Age = 21 };
    new Customer { Name = "Ringo", Age = 32 };
    new Customer { Name = "Paul", Age = 43 };
};
```

**[⬆ back to top](#table-of-contents)**

## Auto-Implemented properties

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
class Customer
{
    // Auto-Implemented properties for trivial get and set
   public int CustomerID { get; set; }
   public string Name { get; set; }
}
```

**[⬆ back to top](#table-of-contents)**

## Anonymous Types

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// Anonymous types provide a convenient way to encapsulate a set of read-only
// properties into a single object without having to explicitly define a type first

var v = new { Amount = 108, Message = "Hello" };
Console.WriteLine(v.Amount + v.Message);

// Anonymous types typically are used in the select clause of a query expression
// to return a subset of the properties from each object in the source sequence

var productQuery =
    from prod in products
    select new { prod.Color, prod.Price };

```

**[⬆ back to top](#table-of-contents)**

## Extension Methods

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// Extension methods enable you to "add" methods to existing types without
// creating a new derived type, recompiling, or otherwise modifying the original type

namespace ExtensionMethods
{
    public static class MyExtensions
    {
        public static int WordCount(this String str)
        {
            return str.Split(new char[] { ' ', '.', '?' },
                             StringSplitOptions.RemoveEmptyEntries).Length;
        }
    }
}

string s = "Hello Extension Methods";
// Extension methods are defined as static methods but are called by using instance method syntax
int i = s.WordCount();
```

**[⬆ back to top](#table-of-contents)**

## Lambda expressions

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// A lambda expression is an anonymous function that you
// can use to create delegates or expression tree types.
delegate int del(int i);
static void Main(string[] args)
{
    del myDelegate = x => x * x;
    int j = myDelegate(5); //j = 25

    Expression<del> myET = x => x * x;
}
```

**[⬆ back to top](#table-of-contents)**

## Expression trees

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// Create an expression using expression lambda
Expression<Func<int, int, int>> expression = (num1, num2) => num1 + num2;

// Compile the expression
Func<int, int, int> compiledExpression = expression.Compile();

// Execute the expression.
int result = compiledExpression(3, 4); //return 7
```

**[⬆ back to top](#table-of-contents)**

## Partial methods

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
 partial class MyClass
 {
     partial void OnSomethingHappened(string s);
 }

 // This part can be in a separate file.
 partial class MyClass
 {
     // Comment out this method and the program
     // will still compile.
     partial void OnSomethingHappened(String s)
     {
         Console.WriteLine("Something happened: {0}", s);
     }
 }
```

**[⬆ back to top](#table-of-contents)**

## Query expressions

<sup>[[C# 3.0](#csharp-3)]</sup>

```csharp
// A query is a set of instructions that describes what data to retrieve from a given
// data source (or sources) and what shape and organization the returned data should have.

// Data source.
int[] scores = { 90, 71, 82, 93, 75, 82 };

// Query Expression.
IEnumerable<int> scoreQuery = //query variable
  from score in scores //required
  where score > 80 // optional
  orderby score descending // optional
  select score; //must end with select or group

// Execute the query to produce the results
foreach (int testScore in scoreQuery)
{
  Console.WriteLine(testScore);
}
```

**[⬆ back to top](#table-of-contents)**

## Dynamic binding

<sup>[[C# 4.0](#csharp-4)]</sup>

```csharp
// Dynamic binding refers to delaying the process of type resolution from compile time to runtime.

// Static binding
Person obj = new Person();
obj.Run(); // Compiler will try to find a method named Run
           // If not found the compiler will generate an error

// Dynamic binding
dynamic obj = new Person();
obj.Run(); // Resolves binding on runtime instead of compile time.

```

**[⬆ back to top](#table-of-contents)**

## Named and optional arguments

<sup>[[C# 4.0](#csharp-4)]</sup>

```csharp
 // Example method
 public static int Sum(int firstNumber, int secondNumber = 1)
{
    return firstNumber+ secondNumber;
}

// Passing parameters using the normal way
Sum(10, 20);

// Passing parameters using named parameter
Sum(firstNumber: 10, secondNumber: 20);

// Passing parameters using default value
Sum(10);

// Example method using optional parameters
public int Sum(int firstNumber, [Optional] int secondNumber)
{
   return firstNumber + secondNumber;
}

// Example method using params keyword
public int Sum(int firstNumber, params int[] numbers)
{
   int total = 0;
   foreach (int number in numbers)
   {
       number += number;
   }
   return total + firstNumber;
}
```

**[⬆ back to top](#table-of-contents)**

## Generic co and contravariance

<sup>[[C# 4.0](#csharp-4)]</sup>

- Covariance

```csharp
// Enables you to use a more derived type than originally specified
IEnumerable<Derived> d = new List<Derived>();
IEnumerable<Base> b = d;
```

- Contravariance

```csharp
// Enables you to use a more generic (less derived) type than originally specified
Action<Base> b = (target) => { Console.WriteLine(target.GetType().Name); };
Action<Derived> d = b;
d(new Derived());
```

**[⬆ back to top](#table-of-contents)**

## Caller info attributes

<sup>[[C# 5.0](#csharp-5)]</sup>

```csharp
public void DoProcessing()
{
    TraceMessage("Something happened.");
}

public void TraceMessage(string message,
        [CallerMemberName] string memberName = "",
        [CallerFilePath] string sourceFilePath = "",
        [CallerLineNumber] int sourceLineNumber = 0)
{
    Trace.WriteLine("message: " + message); // message: Something happened
    Trace.WriteLine("member name: " + memberName); // member name: DoProcessing
    Trace.WriteLine("file path: " + sourceFilePath); // file path: c:\Users\username\Documents\Form1.cs
    Trace.WriteLine("source line number: " + sourceLineNumber); // source line number: 31
}
```

**[⬆ back to top](#table-of-contents)**

## Asynchronous methods

<sup>[[C# 5.0](#csharp-5)]</sup>

```csharp
// For I/O-bound code, you await an operation which returns a Task or Task<T> inside of an async method.
private readonly HttpClient _httpClient = new HttpClient();

downloadButton.Clicked += async (o, e) =>
{
    // This line will yield control to the UI as the request
    // from the web service is happening.
    //
    // The UI thread is now free to perform other work.
    var stringData = await _httpClient.GetStringAsync(URL);
    DoSomethingWithData(stringData);
};

// For CPU-bound code, you await an operation which is started on a background thread with the Task.Run method.
private DamageResult CalculateDamageDone()
{
    // Code omitted:
    //
    // Does an expensive calculation and returns
    // the result of that calculation.
}


calculateButton.Clicked += async (o, e) =>
{
    // This line will yield control to the UI while CalculateDamageDone()
    // performs its work.  The UI thread is free to perform other work.
    var damageResult = await Task.Run(() => CalculateDamageDone());
    DisplayDamage(damageResult);
};
```

**[⬆ back to top](#table-of-contents)**

## Compiler as a service Roslyn

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
// Roslyn provides open-source C# and Visual Basic compilers with rich code analysis APIs.

const string programText =
@"using System;
using System.Collections;
using System.Linq;
using System.Text;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(""Hello, World!"");
        }
    }
}";

// Syntax analysis traversing trees
// Build the syntax tree
SyntaxTree tree = CSharpSyntaxTree.ParseText(programText);
CompilationUnitSyntax root = tree.GetCompilationUnitRoot(); // Retrieve the root node of that tree

// Examine the nodes in the tree.
WriteLine($"The tree is a {root.Kind()} node.");
WriteLine($"The tree has {root.Members.Count} elements in it.");
WriteLine($"The tree has {root.Usings.Count} using statements. They are:");
foreach (UsingDirectiveSyntax element in root.Usings)
    WriteLine($"\t{element.Name}");

// Semantic analysis Querying symbols
var compilation = CSharpCompilation.Create("HelloWorld")
    .AddReferences(MetadataReference.CreateFromFile(
        typeof(string).Assembly.Location))
    .AddSyntaxTrees(tree);

// Querying the semantic model
SemanticModel model = compilation.GetSemanticModel(tree);

// Use the syntax tree to find "using System;"
UsingDirectiveSyntax usingSystem = root.Usings[0];
NameSyntax systemName = usingSystem.Name;

// Use the semantic model for symbol information:
SymbolInfo nameInfo = model.GetSymbolInfo(systemName);
```

**[⬆ back to top](#table-of-contents)**

## Import of static type members into namespace

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
// Without using static
using System;
Math.PI

// Using static directive designates a type whose static members you can access without specifying a type name.
using static System.Math;
Math.PI
```

**[⬆ back to top](#table-of-contents)**

## Await in catch finally blocks

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
try
{
  await ThatMayThrowAsync();
}
catch (ExpectedException ex)
{
  await Logger.LogAsync(ex);
}
```

**[⬆ back to top](#table-of-contents)**

## Auto property initializers

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
public decimal Price { get; set; } = 0.50m;
public string Name { get; set; } = "John";
```

**[⬆ back to top](#table-of-contents)**

## Nameof operator

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
class Person {
   public string Name { get; set; }
}

var person = new Person();

int number = 0;
string text = "lorem ipsum";
Console.WriteLine(nameof(number)); // number
Console.WriteLine(nameof(text)); // text
Console.WriteLine(nameof(person.Name)); // Name
```

**[⬆ back to top](#table-of-contents)**

## String interpolation

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
Console.WriteLine($"Hello, {name}! Today is {date.DayOfWeek}, it's {date:HH:mm} now.");
```

**[⬆ back to top](#table-of-contents)**

## Expression-bodied members

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
class Person {
  public string FirstName { get; set; }
  public string LastName { get; set; }
  public string GetFullName() => FirstName + " " + LastName;
}

var person = new Person();
person.FirstName = "John";
person.LastName = "Doe";
Console.WriteLine(person.GetFullName());
```

**[⬆ back to top](#table-of-contents)**

## Dictionary initializer

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
var dictionary = new Dictionary<string, int>
{
    ["one"] = 1,
    ["two"] = 2,
    ["three"] = 3
};
```

**[⬆ back to top](#table-of-contents)**

## Null propagator (null-conditional operator, succinct null checking)

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
int? length = customers?.Length; // null if customers is null
Customer first = customers?[0];  // null if customers is null
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null
```

**[⬆ back to top](#table-of-contents)**

## Default values for getter only properties

<sup>[[C# 6.0](#csharp-6)]</sup>

```csharp
public class Dog
{
    public string Name { get; set; }

    // DogCreationTime is immutable
    public DateTime DogCreationTime { get; } = DateTime.Now;

    public Dog(string name)
    {
        Name = name;
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Pattern Matching

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/pattern-matching)]</sup>

Patterns test that a value has a certain shape, and can extract information from the value when it has the matching shape.

```csharp
public static void SwitchPattern(object o)
{
    switch (o)
    {
        case null:
            Console.WriteLine("it's a constant pattern");
            break;
        case int i:
            Console.WriteLine("it's an int");
            break;
        case Person p when p.FirstName.StartsWith("A"):
            Console.WriteLine($"a A person {p.FirstName}");
            break;
        case Person p:
            Console.WriteLine($"any other person {p.FirstName}");
            break;
        case var x:
            Console.WriteLine($"it's a var pattern with the type {x?.GetType().Name} ");
            break;
        default:
            break;
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Tuples

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-7#tuples)]</sup>

Tuples are lightweight data structures that contain multiple fields to represent the data members.

```csharp
// You can create a tuple by assigning a value to each member
(string Alpha, string Beta) namedLetters = ("a", "b");
Console.WriteLine($"{namedLetters.Alpha}, {namedLetters.Beta}");

// You can also specify the names of the fields on the right-hand side of the assignment
var alphabetStart = (Alpha: "a", Beta: "b");
Console.WriteLine($"{alphabetStart.Alpha}, {alphabetStart.Beta}");
```

### Deconstruction

```csharp
// There may be times when you want to unpackage the members of a tuple that were returned from a method
(int max, int min) = Range(numbers);
Console.WriteLine(max);
Console.WriteLine(min);
```

**[⬆ back to top](#table-of-contents)**

## Discards

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/functional/discards)]</sup>

Discards, which are placeholder variables that are intentionally unused in application code. Discards are equivalent to unassigned variables; they don't have a value. A discard communicates intent to the compiler and others that read your code: You intended to ignore the result of an expression. You may want to ignore the result of an expression, one or more members of a tuple expression, an out parameter to a method, or the target of a pattern matching expression.

Discards make the intent of your code clear. A discard indicates that our code never uses the variable. They enhance its readability and maintainability.

You indicate that a variable is a discard by assigning it the underscore (\_) as its name.

```csharp
using System;

namespace Discards
{
    public class Person
    {
        public string FirstName { get; set; }
        public string MiddleName { get; set; }
        public string LastName { get; set; }
        public string City { get; set; }
        public string State { get; set; }

        public Person(string fname, string mname, string lname,
                      string cityName, string stateName)
        {
            FirstName = fname;
            MiddleName = mname;
            LastName = lname;
            City = cityName;
            State = stateName;
        }

        // Return the first and last name.
        public void Deconstruct(out string fname, out string lname)
        {
            fname = FirstName;
            lname = LastName;
        }

        public void Deconstruct(out string fname, out string mname, out string lname)
        {
            fname = FirstName;
            mname = MiddleName;
            lname = LastName;
        }

        public void Deconstruct(out string fname, out string lname,
                                out string city, out string state)
        {
            fname = FirstName;
            lname = LastName;
            city = City;
            state = State;
        }
    }
    class Example
    {
        public static void Main()
        {
            var p = new Person("John", "Quincy", "Adams", "Boston", "MA");

            // Deconstruct the person object.
            var (fName, _, city, _) = p;
            Console.WriteLine($"Hello {fName} of {city}!");
            // The example displays the following output:
            //      Hello John of Boston!
        }
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Ref returns and locals

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/ref-returns)]</sup>

A reference return value allows a method to return a reference to a variable, rather than a value, back to a caller.

The caller can then choose to treat the returned variable as if it were returned by value or by reference. The caller can create a new variable that is itself a reference to the returned value, called a ref local.

**Defining a ref return value**

A method that returns a reference return value must satisfy the following two conditions:

    The method signature includes the ref keyword in front of the return type.
    Each return statement in the method body includes the ref keyword in front of the name of the returned instance.

**Consuming a ref return value**

The ref return value is an alias to another variable in the called method's scope. You can interpret any use of the ref return as using the variable it aliases:

    When you assign its value, you are assigning a value to the variable it aliases.
    When you read its value, you are reading the value of the variable it aliases.
    If you return it by reference, you are returning an alias to that same variable.
    If you pass it to another method by reference, you are passing a reference to the variable it aliases.
    When you make a ref local alias, you make a new alias to the same variable.

```csharp
using System;

class NumberStore
{
    int[] numbers = { 1, 3, 7, 15, 31, 63, 127, 255, 511, 1023 };

    public ref int FindNumber(int target)
    {
        for (int ctr = 0; ctr < numbers.Length; ctr++)
        {
            if (numbers[ctr] >= target)
                return ref numbers[ctr];
        }
        return ref numbers[0];
    }

    public override string ToString() => string.Join(" ", numbers);
}

var store = new NumberStore();
Console.WriteLine($"Original sequence: {store.ToString()}");
int number = 16;
ref var value = ref store.FindNumber(number);
value *= 2;
Console.WriteLine($"New sequence:      {store.ToString()}");
// The example displays the following output:
//       Original sequence: 1 3 7 15 31 63 127 255 511 1023
//       New sequence:      1 3 7 15 62 63 127 255 511 1023
```

**[⬆ back to top](#table-of-contents)**

## Local functions

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-7#local-functions)]</sup>

Local functions enable you to declare methods inside the context of another method.

```csharp
public static void Main()
{
    Console.WriteLine(Sum(1,1));
}

public static string Sum(int x, int y) {
    return DisplayResult(x + y);

    string DisplayResult(int result) {
        return result.ToString();
    }
}
```

**[⬆ back to top](#table-of-contents)**

## More expression-bodied members

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/statements-expressions-operators/expression-bodied-members)]</sup>

Expression body definitions let you provide a member's implementation in a very concise, readable form.
You can use an expression body definition whenever the logic for any supported member, such as a method or property, consists of a single expression.

An expression body definition has the following general syntax: **member => expression;**

```csharp
// Methods
using System;

public class Person
{
   public Person(string firstName, string lastName)
   {
      fname = firstName;
      lname = lastName;
   }

   private string fname;
   private string lname;

   public override string ToString() => $"{fname} {lname}".Trim();
   public void DisplayName() => Console.WriteLine(ToString());
}

class Example
{
   static void Main()
   {
      Person p = new Person("Mandy", "Dejesus");
      Console.WriteLine(p);
      p.DisplayName();
   }
}

// Read-only properties
public class Location
{
   private string locationName;

   public Location(string name)
   {
      locationName = name;
   }

   public string Name => locationName;
}

// Properties
public class Location
{
   private string locationName;

   public Location(string name) => Name = name;

   public string Name
   {
      get => locationName;
      set => locationName = value;
   }
}

// Constructors
public class Location
{
   private string locationName;

   public Location(string name) => Name = name;

   public string Name
   {
      get => locationName;
      set => locationName = value;
   }
}

// Finalizers
public class Destroyer
{
   public override string ToString() => GetType().Name;

   ~Destroyer() => Console.WriteLine($"The {ToString()} finalizer is executing.");
}

// Indexers
using System;
using System.Collections.Generic;

public class Sports
{
   private string[] types = { "Baseball", "Basketball", "Football",
                              "Hockey", "Soccer", "Tennis",
                              "Volleyball" };

   public string this[int i]
   {
      get => types[i];
      set => types[i] = value;
   }
}
```

**[⬆ back to top](#table-of-contents)**

## throw Expressions

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/throw#the-throw-expression)]</sup>

Starting with C# 7.0, throw can be used as an expression as well as a statement. This allows an exception to be thrown in contexts that were previously unsupported.

```csharp
// the conditional operator
private static void DisplayFirstNumber(string[] args)
{
   string arg = args.Length >= 1 ? args[0] :
                              throw new ArgumentException("You must supply an argument");
   if (Int64.TryParse(arg, out var number))
      Console.WriteLine($"You entered {number:F0}");
   else
      Console.WriteLine($"{arg} is not a number.");
}

// the null-coalescing operator
public string Name
{
    get => name;
    set => name = value ??
        throw new ArgumentNullException(paramName: nameof(value), message: "Name cannot be null");
}

// an expression-bodied lambda or method
DateTime ToDateTime(IFormatProvider provider) =>
         throw new InvalidCastException("Conversion to a DateTime is not supported.");
```

**[⬆ back to top](#table-of-contents)**

## Generalized async return types

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/async-return-types#generalized-async-return-types-and-valuetasktresult)]</sup>

Generalized async return types enable the compiler to generate async methods that return different types.

Generalized async return types enabled performance improvements in the .NET libraries. Because Task and Task<TResult> are reference types, memory allocation in performance-critical paths, particularly when allocations occur in tight loops, can adversely affect performance.

Support for generalized return types means that you can return a lightweight value type instead of a reference type to avoid additional memory allocations.

```csharp
class Program
{
    static readonly Random s_rnd = new Random();

    static async Task Main() =>
        Console.WriteLine($"You rolled {await GetDiceRollAsync()}");

    static async ValueTask<int> GetDiceRollAsync()
    {
        Console.WriteLine("Shaking dice...");

        int roll1 = await RollAsync();
        int roll2 = await RollAsync();

        return roll1 + roll2;
    }

    static async ValueTask<int> RollAsync()
    {
        await Task.Delay(500);

        int diceRoll = s_rnd.Next(1, 7);
        return diceRoll;
    }
}
// Example output:
//    Shaking dice...
//    You rolled 8
```

**[⬆ back to top](#table-of-contents)**

## Numeric literal syntax improvements

<sup>[[C# 7.0](#csharp-7)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-7.0/digit-separators)]</sup>

C# 7.0 allows \_ to occur as a digit separator inside number literals:

```csharp
// decimal notation
var balance = 2_435_951.68;
balance += 227_652;
Debug.WriteLine($"Balance = {balance}.");

// hexadecimal notation
var num = 0x01_00;
num += 1;
Debug.WriteLine($"num = {num}.");

// binary notation
var num2 = 0b1_0000_0000;
num2 += 1;
Debug.WriteLine($"num2 = {num2}.");
```

**[⬆ back to top](#table-of-contents)**

## Async main

<sup>[[C# 7.1](#csharp-71)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/program-structure/main-command-line)]</sup>

When you declare an async return value for Main, the compiler generates the boilerplate code for calling asynchronous methods in Main.

```csharp
static async Task<int> Main(string[] args)
{
    return await AsyncConsoleWork();
}
```

**[⬆ back to top](#table-of-contents)**

## Inferred tuple element names

<sup>[[C# 7.1](#csharp-71)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-7.1/infer-tuple-names)]</sup>

When you declare an async return value for Main, the compiler generates the boilerplate code for calling asynchronous methods in Main.

```csharp
// in 7.0
public static void Demo()
{
    var count = 5;
    var type = "Orange";

    var tuple = (Count: count, Type: type);
}

// In 7.1
public static void Demo()
{
    var count = 5;
    var type = "Orange";

    var tuple = (count, type);
}
```

**[⬆ back to top](#table-of-contents)**

## Non-trailing named arguments

<sup>[[C# 7.2](#csharp-72)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-7.2/non-trailing-named-arguments)]</sup>

An argument with an argument-name is referred to as a named argument, whereas an argument without an argument name is a positional argument. The named arguments free you from matching the order of parameters in the parameter lists of called methods.

    The parameter for each argument can be specified by parameter name.

    Before C# 7.2, when you call a method with named arguments or optional parameters, all the named arguments must be specified at the end of the method signature after all the required arguments.

    It was not allowed to appear a positional argument after a named argument in an argument list.

```csharp
private static void PrintEmployeeInfo(string name, int age, string address, bool isActive = default, bool isManager = default)
{
    Console.WriteLine("Name: {0}, Age: {1}, Address: {2}, Is Active: {3}, Is Manager: {4}", name, age, address, isActive, isManager);
}

public static void Example()
{
    PrintEmployeeInfo("Mark", 24, "22 Ashdown close");
    PrintEmployeeInfo("John", 31, "9 Ashdown close", true, false);
    PrintEmployeeInfo(name:"Stella", age:29, address:"32 burak town", isActive:true, isManager:true);
    PrintEmployeeInfo(age:27, address:"81 wall street", name: "Andy", isManager: true, isActive: true);
}
```

**[⬆ back to top](#table-of-contents)**

## private protected access modifier

<sup>[[C# 7.2](#csharp-72)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/private-protected)]</sup>

The private protected keyword combination is a member access modifier. A private protected member is accessible by types derived from the containing class, but only within its containing assembly.

```csharp
public class BaseClass
{
    private protected int myValue = 0;
}

public class DerivedClass1 : BaseClass
{
    void Access()
    {
        var baseObject = new BaseClass();

        // Error CS1540, because myValue can only be accessed by
        // classes derived from BaseClass.
        // baseObject.myValue = 5;

        // OK, accessed through the current derived class instance
        myValue = 5;
    }
}

// Assembly2.cs
// Compile with: /reference:Assembly1.dll
class DerivedClass2 : BaseClass
{
    void Access()
    {
        // Error CS0122, because myValue can only be
        // accessed by types in Assembly1
        // myValue = 10;
    }
}
```

**[⬆ back to top](#table-of-contents)**

## Readonly members

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#readonly-members)]</sup>

You can apply the readonly modifier to members of a struct. It indicates that the member doesn't modify state. It's more granular than applying the readonly modifier to a struct declaration.

```csharp
public class SamplePoint
{
    public int x;
    // Initialize a readonly field
    public readonly int y = 25;
    public readonly int z;

    public SamplePoint()
    {
        // Initialize a readonly instance field
        z = 24;
    }

    public SamplePoint(int p1, int p2, int p3)
    {
        x = p1;
        y = p2;
        z = p3;
    }

    public static void Main()
    {
        SamplePoint p1 = new SamplePoint(11, 21, 32);   // OK
        Console.WriteLine($"p1: x={p1.x}, y={p1.y}, z={p1.z}");
        SamplePoint p2 = new SamplePoint();
        p2.x = 55;   // OK
        Console.WriteLine($"p2: x={p2.x}, y={p2.y}, z={p2.z}");
    }
    /*
     Output:
        p1: x=11, y=21, z=32
        p2: x=55, y=25, z=24
    */
}
```

**[⬆ back to top](#table-of-contents)**

## Default interface members

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#default-interface-methods)]</sup>

You can now add members to interfaces and provide an implementation for those members. This language feature enables API authors to add methods to an interface in later versions without breaking source or binary compatibility with existing implementations of that interface. Existing implementations inherit the default implementation. This feature also enables C# to interoperate with APIs that target Android or Swift, which support similar features. Default interface methods also enable scenarios similar to a "traits" language feature.

```csharp
// Version 1:
public decimal ComputeLoyaltyDiscount()
{
    DateTime TwoYearsAgo = DateTime.Now.AddYears(-2);
    if ((DateJoined < TwoYearsAgo) && (PreviousOrders.Count() > 10))
    {
        return 0.10m;
    }
    return 0;
}
SampleCustomer c = new SampleCustomer("customer one", new DateTime(2010, 5, 31))
{
    Reminders =
    {
        { new DateTime(2010, 08, 12), "childs's birthday" },
        { new DateTime(1012, 11, 15), "anniversary" }
    }
};

SampleOrder o = new SampleOrder(new DateTime(2012, 6, 1), 5m);
c.AddOrder(o);

o = new SampleOrder(new DateTime(2103, 7, 4), 25m);
c.AddOrder(o);

// Check the discount:
ICustomer theCustomer = c;
Console.WriteLine($"Current discount: {theCustomer.ComputeLoyaltyDiscount()}");

// Check the discount:
ICustomer theCustomer = c;
Console.WriteLine($"Current discount: {theCustomer.ComputeLoyaltyDiscount()}");
```

**[⬆ back to top](#table-of-contents)**

## Pattern matching enhancements

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#more-patterns-in-more-places)]</sup>

C# 8.0 expands this vocabulary so you can use more pattern expressions in more places in your code. Consider these features when your data and functionality are separate. Consider pattern matching when your algorithms depend on a fact other than the runtime type of an object. These techniques provide another way to express designs.

In addition to new patterns in new places, C# 8.0 adds recursive patterns. Recursive patterns are patterns that can contain other patterns.

```csharp
// switch
public enum Rainbow
{
    Red,
    Orange,
    Yellow,
    Green,
    Blue,
    Indigo,
    Violet
}

public static RGBColor FromRainbow(Rainbow colorBand) =>
    colorBand switch
    {
        Rainbow.Red    => new RGBColor(0xFF, 0x00, 0x00),
        Rainbow.Orange => new RGBColor(0xFF, 0x7F, 0x00),
        Rainbow.Yellow => new RGBColor(0xFF, 0xFF, 0x00),
        Rainbow.Green  => new RGBColor(0x00, 0xFF, 0x00),
        Rainbow.Blue   => new RGBColor(0x00, 0x00, 0xFF),
        Rainbow.Indigo => new RGBColor(0x4B, 0x00, 0x82),
        Rainbow.Violet => new RGBColor(0x94, 0x00, 0xD3),
        _              => throw new ArgumentException(message: "invalid enum value", paramName: nameof(colorBand)),
    };

// Property patterns
public static decimal ComputeSalesTax(Address location, decimal salePrice) =>
    location switch
    {
        { State: "WA" } => salePrice * 0.06M,
        { State: "MN" } => salePrice * 0.075M,
        { State: "MI" } => salePrice * 0.05M,
        // other cases removed for brevity...
        _ => 0M
    };

// Tuple patterns
public static string RockPaperScissors(string first, string second)
    => (first, second) switch
    {
        ("rock", "paper") => "rock is covered by paper. Paper wins.",
        ("rock", "scissors") => "rock breaks scissors. Rock wins.",
        ("paper", "rock") => "paper covers rock. Paper wins.",
        ("paper", "scissors") => "paper is cut by scissors. Scissors wins.",
        ("scissors", "rock") => "scissors is broken by rock. Rock wins.",
        ("scissors", "paper") => "scissors cuts paper. Scissors wins.",
        (_, _) => "tie"
    };

// Positional patterns
public class Point
{
    public int X { get; }
    public int Y { get; }

    public Point(int x, int y) => (X, Y) = (x, y);

    public void Deconstruct(out int x, out int y) =>
        (x, y) = (X, Y);
}

public enum Quadrant
{
    Unknown,
    Origin,
    One,
    Two,
    Three,
    Four,
    OnBorder
}

static Quadrant GetQuadrant(Point point) => point switch
{
    (0, 0) => Quadrant.Origin,
    var (x, y) when x > 0 && y > 0 => Quadrant.One,
    var (x, y) when x < 0 && y > 0 => Quadrant.Two,
    var (x, y) when x < 0 && y < 0 => Quadrant.Three,
    var (x, y) when x > 0 && y < 0 => Quadrant.Four,
    var (_, _) => Quadrant.OnBorder,
    _ => Quadrant.Unknown
};
```

**[⬆ back to top](#table-of-contents)**

## Using declarations

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#using-declarations)]</sup>

A using declaration is a variable declaration preceded by the using keyword. It tells the compiler that the variable being declared should be disposed at the end of the enclosing scope.

```csharp
static int WriteLinesToFile(IEnumerable<string> lines)
{
    using var file = new System.IO.StreamWriter("WriteLines2.txt");
    int skippedLines = 0;
    foreach (string line in lines)
    {
        if (!line.Contains("Second"))
        {
            file.WriteLine(line);
        }
        else
        {
            skippedLines++;
        }
    }
    // Notice how skippedLines is in scope here.
    return skippedLines;
    // file is disposed here
}

static int WriteLinesToFile(IEnumerable<string> lines)
{
    using (var file = new System.IO.StreamWriter("WriteLines2.txt"))
    {
        int skippedLines = 0;
        foreach (string line in lines)
        {
            if (!line.Contains("Second"))
            {
                file.WriteLine(line);
            }
            else
            {
                skippedLines++;
            }
        }
        return skippedLines;
    } // file is disposed here
}
```

**[⬆ back to top](#table-of-contents)**

## Static local functions

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#static-local-functions)]</sup>

You can now add the static modifier to local functions to ensure that local function doesn't capture (reference) any variables from the enclosing scope. Doing so generates CS8421, "A static local function can't contain a reference to <variable>."

```csharp
// before
int M()
{
    int y;
    LocalFunction();
    return y;

    void LocalFunction() => y = 0;
}

// after
int M()
{
    int y = 5;
    int x = 7;
    return Add(x, y);

    static int Add(int left, int right) => left + right;
}
```

**[⬆ back to top](#table-of-contents)**

## Disposable ref structs

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#disposable-ref-structs)]</sup>

A struct declared with the ref modifier may not implement any interfaces and so can't implement IDisposable. Therefore, to enable a ref struct to be disposed, it must have an accessible void Dispose() method. This feature also applies to readonly ref struct declarations.

```csharp

```

**[⬆ back to top](#table-of-contents)**

## Nullable reference types

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-reference-types)]</sup>

Nullable reference types are available beginning with C# 8.0, in code that has opted in to a nullable aware context. Nullable reference types, the null static analysis warnings, and the null-forgiving operator are optional language features. All are turned off by default. A nullable context is controlled at the project level using build settings, or in code using pragmas.

In a nullable aware context:

    A variable of a reference type T must be initialized with non-null, and may never be assigned a value that may be null.
    A variable of a reference type T? may be initialized with null or assigned null, but is required to be checked against null before de-referencing.
    A variable m of type T? is considered to be non-null when you apply the null-forgiving operator, as in m!.

The distinctions between a non-nullable reference type T and a nullable reference type T? are enforced by the compiler's interpretation of the preceding rules. A variable of type T and a variable of type T? are represented by the same .NET type.

```csharp

```

**[⬆ back to top](#table-of-contents)**

## Asynchronous streams

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#asynchronous-streams)]</sup>

Starting with C# 8.0, you can create and consume streams asynchronously. A method that returns an asynchronous stream has three properties:

    It's declared with the async modifier.
    It returns an IAsyncEnumerable<T>.
    The method contains yield return statements to return successive elements in the asynchronous stream.

Consuming an asynchronous stream requires you to add the await keyword before the foreach keyword when you enumerate the elements of the stream. Adding the await keyword requires the method that enumerates the asynchronous stream to be declared with the async modifier and to return a type allowed for an async method. Typically that means returning a Task or Task<TResult>. It can also be a ValueTask or ValueTask<TResult>. A method can both consume and produce an asynchronous stream, which means it would return an IAsyncEnumerable<T>.

```csharp
public static async System.Collections.Generic.IAsyncEnumerable<int> GenerateSequence()
{
    for (int i = 0; i < 20; i++)
    {
        await Task.Delay(100);
        yield return i;
    }
}

await foreach (var number in GenerateSequence())
{
    Console.WriteLine(number);
}
```

**[⬆ back to top](#table-of-contents)**

## Indices and ranges

<sup>[[C# 8.0](#csharp-8)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#indices-and-ranges)]</sup>

Indices and ranges provide a succinct syntax for accessing single elements or ranges in a sequence.

This language support relies on two new types, and two new operators:

    System.Index represents an index into a sequence.
    The index from end operator ^, which specifies that an index is relative to the end of the sequence.
    System.Range represents a sub range of a sequence.
    The range operator .., which specifies the start and end of a range as its operands.

```csharp
var words = new string[]
{
                // index from start    index from end
    "The",      // 0                   ^9
    "quick",    // 1                   ^8
    "brown",    // 2                   ^7
    "fox",      // 3                   ^6
    "jumped",   // 4                   ^5
    "over",     // 5                   ^4
    "the",      // 6                   ^3
    "lazy",     // 7                   ^2
    "dog"       // 8                   ^1
};              // 9 (or words.Length) ^0

Console.WriteLine($"The last word is {words[^1]}");
// writes "dog"

var quickBrownFox = words[1..4];

var lazyDog = words[^2..^0];

var allWords = words[..]; // contains "The" through "dog".
var firstPhrase = words[..4]; // contains "The" through "fox"
var lastPhrase = words[6..]; // contains "the", "lazy" and "dog"

// You can also declare ranges as variables
Range phrase = 1..4;

// The range can then be used inside the [ and ] characters
var text = words[phrase];
```

**[⬆ back to top](#table-of-contents)**

## Record types

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#record-types)]</sup>

You use the record keyword to define a reference type that provides built-in functionality for encapsulating data.

```csharp
public record Person(string FirstName, string LastName);

public static void Main()
{
    Person person = new("Nancy", "Davolio");
    Console.WriteLine(person);
    // output: Person { FirstName = Nancy, LastName = Davolio }
}
```

**[⬆ back to top](#table-of-contents)**

## Init only setters

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#init-only-setters)]</sup>

Init only setters provide consistent syntax to initialize members of an object. Property initializers make it clear which value is setting which property. The downside is that those properties must be settable. Starting with C# 9.0, you can create init accessors instead of set accessors for properties and indexers. Callers can use property initializer syntax to set these values in creation expressions, but those properties are readonly once construction has completed. Init only setters provide a window to change state. That window closes when the construction phase ends. The construction phase effectively ends after all initialization, including property initializers and with-expressions have completed.

```csharp
public struct WeatherObservation
{
    public DateTime RecordedAt { get; init; }
    public decimal TemperatureInCelsius { get; init; }
    public decimal PressureInMillibars { get; init; }

    public override string ToString() =>
        $"At {RecordedAt:h:mm tt} on {RecordedAt:M/d/yyyy}: " +
        $"Temp = {TemperatureInCelsius}, with {PressureInMillibars} pressure";
}

var now = new WeatherObservation
{
    RecordedAt = DateTime.Now,
    TemperatureInCelsius = 20,
    PressureInMillibars = 998.0m
};
```

**[⬆ back to top](#table-of-contents)**

## Pattern matching enhancements

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#pattern-matching-enhancements)]</sup>

C# 9 includes new pattern matching improvements:

    Type patterns match an object matches a particular type
    Parenthesized patterns enforce or emphasize the precedence of pattern combinations
    Conjunctive and patterns require both patterns to match
    Disjunctive or patterns require either pattern to match
    Negated not patterns require that a pattern doesn't match
    Relational patterns require the input be less than, greater than, less than or equal, or greater than or equal to a given constant.

```csharp
public static bool IsLetter(this char c) =>
    c is >= 'a' and <= 'z' or >= 'A' and <= 'Z';

public static bool IsLetterOrSeparator(this char c) =>
    c is (>= 'a' and <= 'z') or (>= 'A' and <= 'Z') or '.' or ',';

if (e is not null)
{
    // ...
}
```

**[⬆ back to top](#table-of-contents)**

## Performance and interop

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#performance-and-interop)]</sup>

Three new features improve support for native interop and low-level libraries that require high performance: native sized integers, function pointers, and omitting the localsinit flag.

```csharp

```

**[⬆ back to top](#table-of-contents)**

## Fit and finish features

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#fit-and-finish-features)]</sup>

Many of the other features help you write code more efficiently. In C# 9.0, you can omit the type in a new expression when the created object's type is already known.

```csharp
private List<WeatherObservation> _observations = new();

public WeatherForecast ForecastFor(DateTime forecastDate, WeatherForecastOptions options)

var forecast = station.ForecastFor(DateTime.Now.AddDays(2), new());

WeatherStation station = new() { Location = "Seattle, WA" };
```

**[⬆ back to top](#table-of-contents)**

## Support for code generators

<sup>[[C# 9.0](#csharp-9)]</sup> <sup>[[Oficial docs](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9#support-for-code-generators)]</sup>

```csharp

```

**[⬆ back to top](#table-of-contents)**

## Global using directives

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/using-directive#global-modifier)]</sup>

Adding the global modifier to a using directive means that using is applied to all files in the compilation (typically a project). 

A global using directive can appear at the beginning of any source code file. All global using directives in a single file must appear before:

    All using directives without the global modifier.
    All namespace and type declarations in the file.

You may add global using directives to any source file. Typically, you'll want to keep them in a single location. The order of global using directives doesn't matter, either in a single file, or between files.

The global modifier may be combined with the static modifier. The global modifier may be applied to a using alias directive. In both cases, the directive's scope is all files in the current compilation. 

```csharp
global using static System.Math;
```

## File-scoped Namespace Declaration

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#file-scoped-namespace-declaration)]</sup>

You can use a new form of the namespace declaration to declare that all declarations that follow are members of the declared namespace:

```csharp
// Namespace without parentheses but with a semicolon
namespace Medium;
public class Program 
{
	public static void Main() {
		Console.WriteLine(new Person( "Mac", "PC"));
	} 
}

public record Person(string firstName, string lastName);

```

## Implicit Using statements

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://devblogs.microsoft.com/dotnet/welcome-to-csharp-10/)]</sup>

The Implicit usings feature automatically adds common global using directives for the type of project you are building. To enable implicit usings set the ImplicitUsings property in your .csproj file:

For new projects, this is automatically active.

```xml
<PropertyGroup>
    <!-- Other properties like OutputType and TargetFramework -->
    <ImplicitUsings>enable</ImplicitUsings>
</PropertyGroup>
```

Note: You can always check which implicit usings are being generated for your project by navigating to your projects obj directory and finding the generated file named: [Your Projects Name].GlobalUsings.g.cs.

## Custom Interpolated String Handlers

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#interpolated-string-handler)]</sup>

An interpolated string handler is a type that processes the placeholder expression in an interpolated string. Without a custom handler, placeholders are processed similar to String.Format. Each placeholder is formatted as text, and then the components are concatenated to form the resulting string.

```csharp

// Initial Implementation
public enum LogLevel
{
    Off,
    Critical,
    Error,
    Warning,
    Information,
    Trace
}

public class Logger
{
    public LogLevel EnabledLevel { get; init; } = LogLevel.Error;

    public void LogMessage(LogLevel level, string msg)
    {
        if (EnabledLevel < level) return;
        Console.WriteLine(msg);
    }
}

```
```csharp
// Implement the handler pattern

[InterpolatedStringHandler]
public ref struct LogInterpolatedStringHandler
{
    // Storage for the built-up string
    StringBuilder builder;

    public LogInterpolatedStringHandler(int literalLength, int formattedCount)
    {
        builder = new StringBuilder(literalLength);
        Console.WriteLine($"\tliteral length: {literalLength}, formattedCount: {formattedCount}");
    }

    public void AppendLiteral(string s)
    {
        Console.WriteLine($"\tAppendLiteral called: {{{s}}}");
        
        builder.Append(s);
        Console.WriteLine($"\tAppended the literal string");
    }

    public void AppendFormatted<T>(T t)
    {
        Console.WriteLine($"\tAppendFormatted called: {{{t}}} is of type {typeof(T)}");

        builder.Append(t?.ToString());
        Console.WriteLine($"\tAppended the formatted object");
    }

    internal string GetFormattedText() => builder.ToString();
}

public void LogMessage(LogLevel level, LogInterpolatedStringHandler builder)
{
    if (EnabledLevel < level) return;
    Console.WriteLine(builder.GetFormattedText());
}

var logger = new Logger() { EnabledLevel = LogLevel.Warning };
var time = DateTime.Now;

logger.LogMessage(LogLevel.Error, $"Error Level. CurrentTime: {time}. This is an error. It will be printed.");
logger.LogMessage(LogLevel.Trace, $"Trace Level. CurrentTime: {time}. This won't be printed.");
logger.LogMessage(LogLevel.Warning, "Warning Level. This warning is a string, not an interpolated string expression.");

```

## Extended Property Patterns

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#extended-property-patterns)]</sup>

You can reference nested properties or fields within a property pattern.

https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/extended-property-patterns

https://code-maze.com/csharp-extended-property-patterns/
```csharp
record Order(Payment Payment, Customer Customer);
record Payment(Price Price, DateTime? PaymentDate = null);
record Price(string Currency, decimal Amount);
record Customer(string Name, string Group);
```

Allow property subpatterns to reference nested members, for instance:
```csharp
static class OrderProcessorFactory
{
    public static string Get(Order order) => order switch
    {
        { Payment.Price.Currency: "BTC" } => "CryptoOrderProcessor",
        { Customer.Group: "Banking", Payment.Price.Currency: "JPY" } => "JapaneseBankingProcessor",
        { Payment.Price.Amount: >= 500000 } or { Customer.Group: "VIP" } => "ImportantOrderProcessor",
        _ => "DefaultOrderProcessor"
    };
}
```
Instead of:
```csharp
public static string GetPreCSharp10Syntax(Order order) => order switch
{
    { Payment: {  Price: { Currency: "BTC" } } } => "CryptoOrderProcessor",
    { Customer: { Group: "Banking" }, Payment: { Price: { Currency: "JPY" } } } => "JapaneseBankingProcessor",
    { Payment: { Price: { Amount: > 5000000} } } or { Customer: { Group: "VIP" } } => "ImportantOrderProcessor",
    _ => "DefaultOrderProcessor"
};
```

**[⬆ back to top](#table-of-contents)**

## Improvements of Structure Types

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#improvements-of-structure-types)]</sup>

You can declare an instance parameterless constructor in a structure type and initialize an instance field or property at its declaration. For more information, see the Struct initialization and default values section of the Structure types article.

A left-hand operand of the with expression can be of any structure type or an anonymous (reference) type.

https://code-maze.com/csharp-10-new-features/

```csharp
public struct Maze
{
    // Parameterless constructor with property initialization 
    public Maze()
    {
        Size = 10;
    }
    
    // Initialization of the property at its declaration
    public int Size { get; set; } = 10;
}
```

## Lambda Expression Improvements

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#lambda-expression-improvements)]</sup>


Lambda expressions may have a natural type, where the compiler can infer a delegate type from the lambda expression or method group.

Lambda expressions may declare a return type when the compiler can't infer it.

Attributes can be applied to lambda expressions.

These features make lambda expressions more similar to methods and local functions. They make it easier to use lambda expressions without declaring a variable of a delegate type, and they work more seamlessly with the new ASP.NET Core Minimal APIs.

```csharp
var lambda = [DebuggerStepThrough]() => "Hello world";

// isEven is implicitly of type Func<int, bool>
var isEven = (int n) => n % 2 == 0;

var oneTwoThreeArray = () => new[]{1, 2, 3}; // inferred type is Func<int[]>
var oneTwoThreeList = IList<int> () => new[]{1, 2, 3}; // same body, but inferred type is now Func<IList<int>>

```

## Constant Interpolated Strings

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#constant-interpolated-strings)]</sup>

const strings may be initialized using string interpolation if all the placeholders are themselves constant strings. String interpolation can create more readable constant strings as you build constant strings used in your application. The placeholder expressions can't be numeric constants because those constants are converted to strings at run time. The current culture may affect their string representation. 

```csharp
// https://code-maze.com/csharp-10-new-features/
const string constantAttribute = "awesome";
const string constantMessage = $"Code maze is {constantAttribute}.";
```

## Record Types Can Seal ToString

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#record-types-can-seal-tostring)]</sup>

You can add the sealed modifier when you override ToString in a record type. Sealing the ToString method prevents the compiler from synthesizing a ToString method for any derived record types. A sealed ToString ensures all derived record types use the ToString method defined in a common base record type. You can learn more about this feature in the article on records.

```csharp
public record Article(string Author, string Title)
{
    public sealed override string ToString()
    {
        return $"{Author}: {Title}";
    }
}
```

## Assignment Declaration in the Same Deconstruction

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10#assignment-and-declaration-in-same-deconstruction)]</sup>

This change removes a restriction from earlier versions of C#. Previously, a deconstruction could assign all values to existing variables, or initialize newly declared variables:

```csharp
// Initialization:
(int x, int y) = point;

// assignment:
int x1 = 0;
int y1 = 0;
(x1, y1) = point;
```
C# 10 removes this restriction:
```csharp
int x = 0;
(x, int y) = point;
```

**[⬆ back to top](#table-of-contents)**

## DateOnly

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/standard/datetime/how-to-use-dateonly-timeonly#the-dateonly-structure)]</sup>

The DateOnly structure represents a specific date, without time. Since it has no time component, it represents a date from the start of the day to the end of the day. This structure is ideal for storing specific dates, such as a birth date, an anniversary date, or business-related dates.

Although you could use DateTime while ignoring the time component, there are a few benefits to using DateOnly over DateTime:

* The DateTime structure may roll into the previous or next day if it's offset by a time zone. DateOnly can't be offset by a time zone, and it always represents the date that was set.

* Serializing a DateTime structure includes the time component, which may obscure the intent of the data. Also, DateOnly serializes less data.

* When code interacts with a database, such as SQL Server, whole dates are generally stored as the date data type, which doesn't include a time. DateOnly matches the database type better.

DateOnly has a range from 0001-01-01 through 9999-12-31, just like DateTime. You can specify a specific calendar in the DateOnly constructor. However, a DateOnly object always represents a date in the proleptic Gregorian calendar, regardless of which calendar was used to construct it. 

```csharp
// Add or subtract days, months, years
var theDate = new DateOnly(2015, 10, 21);

var nextDay = theDate.AddDays(1);
var previousDay = theDate.AddDays(-1);
var decadeLater = theDate.AddYears(10);
var lastMonth = theDate.AddMonths(-1);

Console.WriteLine($"Date: {theDate}");
Console.WriteLine($" Next day: {nextDay}");
Console.WriteLine($" Previous day: {previousDay}");
Console.WriteLine($" Decade later: {decadeLater}");
Console.WriteLine($" Last month: {lastMonth}");

/* This example produces the following output:
 * 
 * Date: 10/21/2015
 *  Next day: 10/22/2015
 *  Previous day: 10/20/2015
 *  Decade later: 10/21/2025
 *  Last month: 9/21/2015
*/

// Parse and format DateOnly
var theDate = DateOnly.ParseExact("21 Oct 2015", "dd MMM yyyy", CultureInfo.InvariantCulture);  // Custom format
var theDate2 = DateOnly.Parse("October 21, 2015", CultureInfo.InvariantCulture);

Console.WriteLine(theDate.ToString("m", CultureInfo.InvariantCulture));     // Month day pattern
Console.WriteLine(theDate2.ToString("o", CultureInfo.InvariantCulture));    // ISO 8601 format
Console.WriteLine(theDate2.ToLongDateString());

/* This example produces the following output:
 * 
 * October 21
 * 2015-10-21
 * Wednesday, October 21, 2015
*/

// Compare DateOnly
var theDate = DateOnly.ParseExact("21 Oct 2015", "dd MMM yyyy", CultureInfo.InvariantCulture);  // Custom format
var theDate2 = DateOnly.Parse("October 21, 2015", CultureInfo.InvariantCulture);
var dateLater = theDate.AddMonths(6);
var dateBefore = theDate.AddDays(-10);

Console.WriteLine($"Consider {theDate}...");
Console.WriteLine($" Is '{nameof(theDate2)}' equal? {theDate == theDate2}");
Console.WriteLine($" Is {dateLater} after? {dateLater > theDate} ");
Console.WriteLine($" Is {dateLater} before? {dateLater < theDate} ");
Console.WriteLine($" Is {dateBefore} after? {dateBefore > theDate} ");
Console.WriteLine($" Is {dateBefore} before? {dateBefore < theDate} ");

/* This example produces the following output:
 * 
 * Consider 10/21/2015
 *  Is 'theDate2' equal? True
 *  Is 4/21/2016 after? True
 *  Is 4/21/2016 before? False
 *  Is 10/11/2015 after? False
 *  Is 10/11/2015 before? True
*/

```

## TimeOnly

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/standard/datetime/how-to-use-dateonly-timeonly#the-timeonly-structure)]</sup>

The TimeOnly structure represents a time-of-day value, such as a daily alarm clock or what time you eat lunch each day. TimeOnly is limited to the range of 00:00:00.0000000 - 23:59:59.9999999, a specific time of day.

Prior to the TimeOnly type being introduced, programmers typically used either the DateTime type or the TimeSpan type to represent a specific time. However, using these structures to simulate a time without a date may introduce some problems, which TimeOnly solves:

* TimeSpan represents elapsed time, such as time measured with a stopwatch. The upper range is more than 29,000 years, and its value can be negative to indicate moving backwards in time. A negative TimeSpan doesn't indicate a specific time of the day.

* If TimeSpan is used as a time of day, there's a risk that it could be manipulated to a value outside of the 24-hour day. TimeOnly doesn't have this risk. For example, if an employee's work shift starts at 18:00 and lasts for 8 hours, adding 8 hours to the TimeOnly structure rolls over to 2:00

* Using DateTime for a time of day requires that an arbitrary date be associated with the time, and then later disregarded. It's common practice to choose DateTime.MinValue (0001-01-01) as the date, however, if hours are subtracted from the DateTime value, an OutOfRange exception might occur. TimeOnly doesn't have this problem as the time rolls forwards and backwards around the 24-hour timeframe.

* Serializing a DateTime structure includes the date component, which may obscure the intent of the data. Also, TimeOnly serializes less data.


```csharp
// Add or subtract time
var theTime = new TimeOnly(7, 23, 11);

var hourLater = theTime.AddHours(1);
var minutesBefore = theTime.AddMinutes(-12);
var secondsAfter = theTime.Add(TimeSpan.FromSeconds(10));
var daysLater = theTime.Add(new TimeSpan(hours: 21, minutes: 200, seconds: 83), out int wrappedDays);
var daysBehind = theTime.AddHours(-222, out int wrappedDaysFromHours);

Console.WriteLine($"Time: {theTime}");
Console.WriteLine($" Hours later: {hourLater}");
Console.WriteLine($" Minutes before: {minutesBefore}");
Console.WriteLine($" Seconds after: {secondsAfter}");
Console.WriteLine($" {daysLater} is the time, which is {wrappedDays} days later");
Console.WriteLine($" {daysBehind} is the time, which is {wrappedDaysFromHours} days prior");

/* This example produces the following output:
 * 
 * Time: 7:23 AM
 *  Hours later: 8:23 AM
 *  Minutes before: 7:11 AM
 *  Seconds after: 7:23 AM
 *  7:44 AM is the time, which is 1 days later 
 *  1:23 AM is the time, which is -9 days prior
*/

// Parse and format TimeOnly
var theTime = TimeOnly.ParseExact("5:00 pm", "h:mm tt", CultureInfo.InvariantCulture);  // Custom format
var theTime2 = TimeOnly.Parse("17:30:25", CultureInfo.InvariantCulture);

Console.WriteLine(theTime.ToString("o", CultureInfo.InvariantCulture));     // Round-trip pattern.
Console.WriteLine(theTime2.ToString("t", CultureInfo.InvariantCulture));    // Long time format
Console.WriteLine(theTime2.ToLongTimeString());

/* This example produces the following output:
 * 
 * 17:00:00.0000000
 * 17:30
 * 5:30:25 PM
*/

```

## Check Strings for Null

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/api/system.argumentnullexception.throwifnull?view=net-7.0)]</sup>

```csharp
public bool DoSomething(string id, string name, string data)
{
    ArgumentNullException.ThrowIfNull(id);
    ArgumentNullException.ThrowIfNull(name);
    ArgumentNullException.ThrowIfNull(data);
}
```

## Process Data in Chunks

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.chunk?view=net-7.0)]</sup>

Processing a list in small chunks

```csharp
sing System;

class Program
{
	public static void Main()
	{
		// Iterate with chunks 
		var list = Enumerable.Range(1, 30);
		const int size = 10;
		int chunkCounter = 0;
		
		foreach (var chunk in list.Chunk(size))
		{
			Console.WriteLine($"CHUNK: #{chunkCounter++}");
			foreach (var item in chunk)
			{
				Console.WriteLine($"-> {item}");
			}
		}
	}
}
```

## LINQ Extensions

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs]()]</sup>

New extension methods have been added to LINQ as well including MaxBy, MinBy, DistinctBy, IntersectBy, ExceptBy, and UnionBy.

```csharp
// https://keyholesoftware.com/2021/12/16/linq-improvements-new-features-in-c-10/
public class Character 
{
    public int Id {get;set;}
    public string Name {get;set;}
    public int Age {get;set;}
}
 
 
List<Character> newHopeCharacters =
    new()
    {
        new() { Id = 1, Name = "Luke Skywalker", Age = 19 },
        new() { Id = 2, Name = "Leia Organa", Age = 19 },
        new() { Id = 3, Name = "Han Solo", Age = 32 },
        new() { Id = 4, Name = "Darth Vader", Age = 45 },
    };
 
List<Character> empireStrikesBackCharacters =
    new()
    {
        new() { Id = 1, Name = "Luke Skywalker", Age = 19 },
        new() { Id = 2, Name = "Leia Organa", Age = 19 },
        new() { Id = 3, Name = "Han Solo", Age = 32 },
        new() { Id = 4, Name = "Darth Vader", Age = 45 },
        new() { Id = 5, Name = "Emperor Palpatine", Age = 88 },
        new() { Id = 6, Name = "Boba Fett", Age = 35 }
    };

// MaxBy
var maxByAge = newHopeCharacters.MaxBy(character => character.Age);

// MinBy
var minAge = newHopeCharacters.Min(character => character.Age);

// DistinctBy
var distinctCharacters = newHopeCharacters.DistinctBy(character => character.Age);

// IntersectBy
var intersection = newHopeCharacters.IntersectBy(empireStrikesBackCharacters.Select(character => character.Id), character => character.Id);

// ExceptBy
var exceptions = empireStrikesBackCharacters.ExceptBy(newHopeCharacters.Select(character => character.Id), character => character.Id);

// UnionBy
var union = empireStrikesBackCharacters.UnionBy(newHopeCharacters, character => character.Age);

// Defining default value
var found = newHopeCharacters.FirstOrDefault(x => x.Id == 1, new() { Id = 1, Name = "Not a character", Age = 0 });

```

**[⬆ back to top](#table-of-contents)**

## PriorityQueue

<sup>[[C# 10.0](#csharp-10)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.priorityqueue-2?view=net-7.0)]</sup>

PriorityQueue, each element is provided with information about its priority.

If an element is to be fetched from the queue, a check is made to determine which of the elements has the highest priority, and this is delivered, irrespective of when it was added to the queue.

```csharp
// https://medium.com/codex/the-most-important-new-features-of-c-10-and-how-to-use-them-9d8a8519c0c4
using System;

class Program
{
	public static void Main()
	{
		var queue = new PriorityQueue<string, int>();
		
		queue.Enqueue("Element 1", 9);
		queue.Enqueue("Element 2", 11);
		queue.Enqueue("Element 3", 27);
		queue.Enqueue("Element 4", 7);
		queue.Enqueue("Element 5", 13);
		queue.Enqueue("Element 6", 0);
		
		while (queue.TryDequeue(out string element, out int priority))
			Console.WriteLine($"element: {element} - priority: {priority}");
	}
}
```

**[⬆ back to top](#table-of-contents)**

## Require Members

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#required-members)]</sup>

You can add the required modifier to properties and fields to enforce constructors and callers to initialize those values. The System.Diagnostics.CodeAnalysis.SetsRequiredMembersAttribute can be added to constructors to inform the compiler that a constructor initializes all required members.

```csharp
public class Person
{
    public Person() { }

    [SetsRequiredMembers]
    public Person(string firstName, string lastName) =>
        (FirstName, LastName) = (firstName, lastName);

    public required string FirstName { get; init; }
    public required string LastName { get; init; }

    public int? Age { get; set; }
}

public class Student : Person
{
    public Student() : base()
    {
    }

    [SetsRequiredMembers]
    public Student(string firstName, string lastName) :
        base(firstName, lastName)
    {
    }

    public double GPA { get; set; }
}
```

**[⬆ back to top](#table-of-contents)**

## Raw string literals

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#raw-string-literals)]</sup>

Raw string literals are a new format for string literals. Raw string literals can contain arbitrary text, including whitespace, new lines, embedded quotes, and other special characters without requiring escape sequences. A raw string literal starts with at least three double-quote (""") characters. It ends with the same number of double-quote characters. Typically, a raw string literal uses three double quotes on a single line to start the string, and three double quotes on a separate line to end the string. The newlines following the opening quote and preceding the closing quote aren't included in the final content:

```csharp
string longMessage = """
    This is a long message.
    It has several lines.
        Some are indented
                more than others.
    Some should start at the first column.
    Some have "quoted text" in them.
    """;
```
Any whitespace to the left of the closing double quotes will be removed from the string literal. Raw string literals can be combined with string interpolation to include braces in the output text. Multiple $ characters denote how many consecutive braces start and end the interpolation:

```csharp
var location = $$"""
   You are at {{{Longitude}}, {{Latitude}}}
   """;
```
The preceding example specifies that two braces start and end an interpolation. The third repeated opening and closing brace are included in the output string.

Other exmaples:
```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#raw-string-literals
// C# 10
string name = "Shehryar";
string surname = "Khan";

string jsonString = 
  $@"
  {{
    'Name': {name},
    'Surname': {surname}
  }}
  ";

// C# 11
string name = "Shehryar";
string surname = "Khan";

string jsonString = 
  $$"""
  {
    "Name": {{name}},
    "Surname": {{surname}}
  }
  """;
```

**[⬆ back to top](#table-of-contents)**

## Generic Attributes

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#generic-attributes)]</sup>

You can declare a generic class whose base class is System.Attribute. This feature provides a more convenient syntax for attributes that require a System.Type parameter. 

```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#generic-attributes
// C# 10
class MyType 
{ }

class MyAttribute : Attribute
{
  private Type type;
  
  public MyAttribute(Type type)
  {
    _type = type;
  }
}

[MyAttribute(typeof(MyType))] 
class Myclass {}

// C# 11
class MyType
{ }

class GenericAttribute<T> : Attribute
  where T : MyType
{
  private T _type;
}

[GenericAttribute<MyType>] 
class MyClass
{ }

```

**[⬆ back to top](#table-of-contents)**

## Extended nameof scope

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#extended-nameof-scope)]</sup>

Type parameter names and parameter names are now in scope when used in a nameof expression in an attribute declaration on that method. This feature means you can use the nameof operator to specify the name of a method parameter in an attribute on the method or parameter declaration. This feature is most often useful to add attributes for nullable analysis.

You can specify the name of a method parameter in an attribute on the parameter declaration or method.

This can be used in adding attributes for code analysis.

```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#extended-nameof-scope
public class MyAttr : Attribute
{
  private readonly string _paramName; 
  
  public MyAttr(string paramName)
  { 
    _paramName = paramName;
  }
}

public class MyClass
{
  [MyAttr(nameof(param))]
  public void Method(int param, [MyAttr(nameof(param))] int anotherParam)
  { }
}
```

**[⬆ back to top](#table-of-contents)**

## Pattern match on a constant string

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#pattern-match-spanchar-or-readonlyspanchar-on-a-constant-string)]</sup>

You've been able to test if a string had a specific constant value using pattern matching for several releases. Now, you can use the same pattern matching logic with variables that are Span<char> or ReadOnlySpan<char>.

```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#pattern-match-spanchar-on-a-constant-string
// C# 10
ReadOnlySpan<char> strSpan = "SK".AsSpan();
if (strSpan == "SK")
{
  Console.WriteLine("Hey, SK");
}

// C# 11
ReadOnlySpan<char> strSpan = "SK".AsSpan();
if (strSpan is "SK")
{
  Console.WriteLine("Hey, SK");
}
```

**[⬆ back to top](#table-of-contents)**

## Auto-default struct

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#auto-default-struct)]</sup>

The C# 11 compiler ensures that all fields of a struct type are initialized to their default value as part of executing a constructor. This change means any field or auto property not initialized by a constructor is automatically initialized by the compiler. Structs where the constructor doesn't definitely assign all fields now compile, and any fields not explicitly initialized are set to their default value.

```csharp
public readonly struct Measurement
{
    public Measurement(double value)
    {
        Value = value;
    }

    public Measurement(double value, string description)
    {
        Value = value;
        Description = description;
    }

    public Measurement(string description)
    {
        Description = description;
    }

    public double Value { get; init; }
    public string Description { get; init; } = "Ordinary measurement";

    public override string ToString() => $"{Value} ({Description})";
}

public static void Main()
{
    var m1 = new Measurement(5);
    Console.WriteLine(m1);  // output: 5 (Ordinary measurement)

    var m2 = new Measurement();
    Console.WriteLine(m2);  // output: 0 ()

    var m3 = default(Measurement);
    Console.WriteLine(m3);  // output: 0 ()
}
```

**[⬆ back to top](#table-of-contents)**

## List patterns

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#list-patterns)]</sup>

List patterns extend pattern matching to match sequences of elements in a list or an array. For example, sequence is [1, 2, 3] is true when the sequence is an array or a list of three integers (1, 2, and 3). You can match elements using any pattern, including constant, type, property and relational patterns. The discard pattern (_) matches any single element, and the new range pattern (..) matches any sequence of zero or more elements.

```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#list-patterns
var numbers = new [] { 1, 2, 3, 4 };
// List and constant patterns 
Console.WriteLine(numbers is [1, 2, 3, 4]); // True 
Console.WriteLine(numbers is [1, 2, 4]); // False
// List and discard patterns 
Console.WriteLine(numbers is [_, 2, _, 4]); // True 
Console.WriteLine(numbers is [.., 3, _]); // True
// List and logical patterns 
Console.WriteLine(numbers is [_, >=2, _, _]); // True
```

**[⬆ back to top](#table-of-contents)**

## UTF-8 string literals

<sup>[[C# 11.0](#csharp-11)]</sup> <sup>[[Oficial docs](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11#utf-8-string-literals)]</sup>

You can specify the u8 suffix on a string literal to specify UTF-8 character encoding. If your application needs UTF-8 strings, for HTTP string constants or similar text protocols, you can use this feature to simplify the creation of UTF-8 strings.

```csharp
// https://dottutorials.net/whats-new-csharp-11-features/#utf-8-string-literals
// C# 10
byte[] array = Encoding.UTF8.GetBytes("Hello World");

// C# 11
byte[] array = "Hello World";
```

**[⬆ back to top](#table-of-contents)**

## Keywords

```csharp
abstract       // Indicates that the thing being modified has a missing or incomplete implementation
as             // Performs certain types of conversions between compatible reference types or nullable type
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
else           // Identifies which statement to run based on the value of a Boolean expression
enum           // Distinct type that consists of a set of named constants called the enumerator list
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
if             // Identifies which statement to run based on the value of a Boolean expression
implicit       // Used to declare an implicit user-defined type conversion operator
in             // (generic modifier) specifies that the type parameter is contravariant
int            // Denotes an integral type
interface      // Contains only the signatures of methods, properties, events or indexers
internal       // Access modifier fortypes or members are accessible only within files in the same assembly
is             // Checks if an object is compatible with a given type
lock           // Marks a statement block as a critical section by obtaining the mutual-exclusion lock
               // for a given object, executing a statement, and then releasing the lock
long           // Denotes an integral type
namespace      // Keyword is used to declare a scope that contains a set of related objects
new            // Keyword can be used as an operator, a modifier, or a constraint
               // Operator - create objects and invoke constructors
               // Modifier - hide an inherited member from a base class member
               // Constraint - restrict types that might be used as arguments for a type parameter
               //              in a generic declaration
null           // Is a literal that represents a null reference, one that does not refer to any object
object         // All types, predefined and user-defined, reference types and value types, inherit
               // directly or indirectly from Object
operator       // To overload a built-in operator or to provide a user-defined conversion in a class
               // or struct declaration.
out            // As a parameter modifier, which lets you pass an argument to a method by reference
               // rather than by value.
               // Generic type parameter declarations for interfaces and delegates, which specifies that a type
               // parameter is covariant
out            // (generic modifier) Enables you to use a more derived type than that specified
               // by the generic parameter
override       // Modifier is required to extend or modify the abstract or virtual implementation of
               // an inherited method, property, indexer, or event
params         // You can specify a method parameter that takes a variable number of arguments
private        // Is a member access modifier the least permissive access level
protected      // Is a member access modifier accessible within its class and by derived class instances
public         // Is an access modifier for types and type members, the most permissive access level
readonly       // Assignments can only occur as part of the declaration or in a constructor in the same class
ref            // Indicates a value that is passed by reference
return         // Terminates execution of the method in which it appears and returns control to the calling method
sbyte          // An integral type, signed 8-bit integer
sealed         // Prevents other classes from inheriting from it
short          // An integral type, signed 16-bit integer
sizeof         // Obtain the size in bytes for an unmanaged type
stackalloc     // Is used in an unsafe code context to allocate a block of memory on the stack
static         // Modifier to declare a static member, which belongs to the type itself rather than
               // to a specific object
string         // Represents a sequence of zero or more Unicode characters
struct         // Is a value type that is typically used to encapsulate small groups of related variables
switch         // Is a selection statement that chooses a single switch section to execute from a
               // list of candidates based on a pattern match with the match expression
this           // Refers to the current instance of the class and is also used as a modifier of
               // the first parameter of an extension method
throw          // Signals the occurrence of an exception during program execution
true           // Represents the boolean value true
try            // Is followed by one or more catch clauses, which specify handlers for different exceptions
typeof         // Used to obtain the System.Type object for a type
uint           // An integral type, unsigned 32-bit integer
ulong          // Denotes an integral type, unsigned 64-bit integer
unchecked      // Is used to suppress overflow-checking for integral-type arithmetic operations and conversions
unsafe         // Denotes an unsafe context, which is required for any operation involving pointers
ushort         // An integral type, unsigned 16-bit integer
using          // As a directive, when it is used to create an alias for a namespace or to import types
               // defined in other namespace. As a statement, when it defines a scope at the end of which
               // an object will be disposed
using static   // Designates a type whose static members you can access without specifying a type name
virtual        // Is used to modify a method, property, indexer, or event declaration and allow for it to
               // be overridden in a derived class
void           // Specifies that the method doesn't return a value.
volatile       // Indicates that a field might be modified by multiple threads that are executing at the same time
while          // Executes a statement or a block of statements until a specified expression evaluates to false
```

**[⬆ back to top](#table-of-contents)**

## Contextual Keywords

```csharp
add            // Define a custom event accessor that is invoked when client code subscribes to your event
alias          // Reference two versions of assemblies that have the same fully-qualified type names
ascending      // Used in the orderby clause in query expressions to specify that the sort order is from smallest to largest
async          // Specify that a method, lambda expression, or anonymous method is asynchronous
await          // Applied to a task in an asynchronous method to insert a suspension point in the execution of the method until the
               // awaited task completes
descending     // Used in the orderby clause in query expressions to specify that the sort order is from largest to smallest
dynamic        // Enables the operations in which it occurs to bypass compile-time type checking
from           // A query expression must begin with a from clause
get            // Defines an accessor method in a property or indexer that returns the property value or the indexer element
global         // Refers to the global namespace
group          // Sequence of IGrouping<TKey,TElement> objects that contain zero or more items that match the key value for the group
into           // Used to create a temporary identifier to store the results of a group, join or select clause into a new identifier
join           // Useful for associating elements from different source sequences that have no direct relationship in the object model
let            // Useful to store the result of a sub-expression in order to use it in subsequent clauses
nameof         // Used to obtain the simple (unqualified) string name of a variable, type, or member
orderby        // Causes the returned sequence or subsequence (group) to be sorted in either ascending or descending order
partial        // (type) Allow for the definition of a class, struct, or interface to be split into multiple files
partial        // (method) A partial method has its signature defined in one part of a partial type, and its implementation defined in
               // another part of the type
remove         // Used to define a custom event accessor that is invoked when client code unsubscribes from your event
select         // Specifies the type of values that will be produced when the query is executed
set            // Accessor method in a property or indexer that assigns a value to the property or the indexer element
value          // Used in the set accessor in ordinary property declarations.
var            // Variables that are declared at method scope can have an implicit "type" var
when           // Used as catch statement of a try/catch or try/catch/finally block or label of a switch statement
where          // (generic type constraint) Specify constraints on the types that can be used as arguments for a type parameter defined
               // in a generic declaration
where          // Specify which elements from the data source will be returned in the query expression
yield          // You indicate that the method, operator, or get accessor in which it appears is an iterator
```

**[⬆ back to top](#table-of-contents)**

## Contributing

Feel free to open tickets or send pull requests with improvements. Thanks in
advance for your help!

### How to Contribute?

Just follow the [contribution guidelines](https://github.com/andredarcie/csharp-guide/blob/master/CONTRIBUTING.md).

## License

The andredarcie/csharp-guide is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
