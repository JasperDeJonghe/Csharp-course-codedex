# Learn C# Basics in 45 Minutes

## Introduction

Are you ready to learn C#? C# is a powerful programming language developed by Microsoft. It's widely used for building applications across various platforms, including desktop, web, mobile, and gaming.

In this tutorial, we'll cover the fundamentals of C# programming, including variables, data types, control structures, and functions. By the end of this tutorial, you'll have a solid understanding of the basics of C# and be ready to start building your own applications!

## Setting Up Your Environment

Before we get started, let's make sure you have everything you need to write and run C# code.

### Prerequisites
You can choose if you want to use Visual Studio or Fiddle, Fiddle is an online code editor that can be used for C#.

- https://dotnetfiddle.net
- Visual Studio: Download and install Visual Studio (community edition), which is a powerful integrated development environment (IDE) for C# development.
  (https://visualstudio.microsoft.com)
- .NET SDK: Install the .NET SDK, which includes everything you need to build and run C# applications.

- Optional: Basic knowledge of any other programming language (even scratch).
- Optional: Basic knowledge of algorithms.

Once you have Visual Studio and the .NET SDK installed or you are using Fiddle, you're ready to start writing C# code!

## Getting Started

Let's create a new C# console application in Visual Studio to get started.

1. Open Visual Studio.
2. Click on "Create a new project."
3. Select "Console App (.NET)" from the list of project templates.
4. Enter a name for your project and click "Create."

Now, you should see a new C# console application project in Visual Studio.

## Your First C# Program

In the `Program.cs` file, you'll see the following code:

```csharp
using System;
					
public class Program
{
	public static void Main()
	{
		Console.WriteLine("Hello World");
	}
}
```

This is the basic ‘hello world’ project, Let's dismantle and explain each line of this C# code:
Sure! Let's dismantle and explain each line of this C# code:

```csharp
using System;
```
- This line tells the compiler to include the `System` namespace. Namespaces in C# are used to organize classes and other types, and the `System` namespace contains fundamental classes for basic operations such as input/output.
```csharp
public class Program
{
```
- This line declares a public class named `Program`. In C#, a class is a blueprint for creating objects. The keyword `public` makes this class accessible from other classes and assemblies.
```csharp
    public static void Main()
    {
```
- This line declares a method named `Main` which is the entry point of a C# application. 
- `public` means this method can be accessed from outside the class.
- `static` means this method belongs to the class itself rather than an instance of the class.
- `void` indicates that this method does not return any value.
- `Main()` is a special method in C# that serves as the entry point of the program. The execution of the program starts from this method.
```csharp
        Console.WriteLine("Hello World");
```
- This line is a statement that calls the `WriteLine` method of the `Console` class to output the string `"Hello World"` to the console.
- `Console` is a class in the `System` namespace that represents the standard input, output, and error streams for console applications.
- `WriteLine` is a method of the `Console` class that writes a line of text to the output stream.
```csharp
    }
}
```
- These lines close the `Main` method and the `Program` class definitions, respectively. In C#, curly braces `{}` are used to define the beginning and end of blocks of code.

Note: In C# you need to place a `;` after every line of code.

## Variables and Data Types

In C#, variables are used to store data. Let's declare some variables and explore different data types in C#.

```csharp
int intNum = 9;
long longNum = 9999999;
float floatNum = 9.99F;
double doubleNum = 99.999;
char letter = 'D'; //a char only works with single quotes
bool myBool = true;
string site = "codedex.io";

var num = 999;
var str = "999";
var bo = false;
```

### Arithmetic Operations:

1. **Addition (`+`):** Adds two operands.

   ```csharp
   int sum = 5 + 3; // sum is 8
   ```

2. **Subtraction (`-`):** Subtracts the second operand from the first.

   ```csharp
   int difference = 8 - 3; // difference is 5
   ```

3. **Multiplication (`*`):** Multiplies two operands.

   ```csharp
   int product = 4 * 2; // product is 8
   ```

4. **Division (`/`):** Divides the first operand by the second.

   ```csharp
   int quotient = 10 / 2; // quotient is 5
   ```

5. **Modulus (`%`):** Returns the remainder of the division operation.
   ```csharp
   int remainder = 10 % 3; // remainder is 1
   ```
   With this operator you can check if a number is odd or even.
   ```csharp
   int even = 8%2 // output will be 0 so it's even
   int odd = 7%2 // output will be 1 so it's odd
   ```

These are some of the basic operations you'll encounter frequently in C# programming. They're used extensively for calculations, comparisons, and logical evaluations.

## Ask Input

To ask the user a question, You need to store the answer in a variable.
To do this you need to ask the question first:

```csharp
Console.WriteLine("What's your name?");
```

To read the next line we need to learn some new syntax.
Here the program is reading the line, when the user presses enter.
Then the answers gets stored in a variable as a string.

```csharp
string name = Console.ReadLine();
```

Note: You probably get some green lines under `Console.ReadLine()`, You will learn more about this later.

So to use this in context we can do this:

```csharp
Console.WriteLine("What's your name?");
string name = Console.ReadLine();
Console.WriteLine("Hello "+name);
```

or

```csharp
Console.WriteLine("What's your name?");
string name = Console.ReadLine();
Console.WriteLine($"Hello {name}!");
```

In the second example you can see a `$`. This is a string interpolation.
This allows you to embed expressions directly within string literals.

Or in simple words. You can directly use variables in your string when placing them between curly braces `{}`

Now we will get to the green lines under `Console.ReadLine()`.
This isn't an error but it's an recommendation.
The program is saying that the variable isn't `nullable`.

In our previous example `name` is declared as `string`, which means it can only hold string values.
If the user enters nothing (presses enter), `name` will be an empty string (`""`).
So in C# we mostly make a nullable variable.

```csharp
Console.WriteLine("What's your name?");
string? name = Console.ReadLine();
Console.WriteLine($"Hello {name}!");
```

Here, name is declared as `string?`, indicating that it can hold either a string value or `null`.

## Control Structures

Control structures allow you to control the flow of your program based on conditions. Let's look at some common control structures in C#.

### Relational Operations:

1. **Equal To (`==`):** Checks if two operands are equal.

   ```csharp
   bool isEqual = (5 == 5); // isEqual is true
   ```

2. **Not Equal To (`!=`):** Checks if two operands are not equal.

   ```csharp
   bool isNotEqual = (5 != 3); // isNotEqual is true
   ```

3. **Greater Than (`>`):** Checks if the left operand is greater than the right.

   ```csharp
   bool isGreaterThan = (5 > 3); // isGreaterThan is true
   ```

4. **Less Than (`<`):** Checks if the left operand is less than the right.

   ```csharp
   bool isLessThan = (3 < 5); // isLessThan is true
   ```

5. **Greater Than or Equal To (`>=`):** Checks if the left operand is greater than or equal to the right.

   ```csharp
   bool isGreaterOrEqual = (5 >= 5); // isGreaterOrEqual is true
   ```

6. **Less Than or Equal To (`<=`):** Checks if the left operand is less than or equal to the right.
   ```csharp
   bool isLessOrEqual = (3 <= 5); // isLessOrEqual is true
   ```

### Logical Operations:

1. **Logical AND (`&&`):** Returns true if both operands are true.

   ```csharp
   bool result = (true && false); // result is false
   bool result2 = (true && true); // result is true
   ```

2. **Logical OR (`||`):** Returns true if at least one of the operands is true.

   ```csharp
   bool result = (true || false); // result is true
   ```

3. **Logical NOT (`!`):** Negates the result of the operand.
   ```csharp
   bool result = !true; // result is false
   ```

### if Statement

```csharp
int num = 10;
if (num > 0)
{
    Console.WriteLine("Positive number");
}
else if (num < 0)
{
    Console.WriteLine("Negative number");
}
else
{
    Console.WriteLine("Zero");
}
```

```csharp
string name = "Sonny";
string secondName = "Li";
if (name == "Sonny" && secondName = "Li") {
    Console.WriteLine("It's the codédex founder!")
}
else {
    Console.WriteLine("Who are you??")
}
```

## extra information - Parsing/Casting:

To parse different data types to other data types in C#, you typically use conversion methods or casting. Here are some common scenarios:

1. **Parsing a string to a numeric type:**

   ```csharp
   string str = "10";
   int intValue = int.Parse(str);
   float floatValue = float.Parse(str);
   ```

2. **Casting between numeric types:**

   ```csharp
   int intValue = 10;
   float floatValue = (float)intValue; // Casting int to float
   double doubleValue = (double)intValue; // Casting int to double
   ```

3. **Parsing a string to a boolean:**

   ```csharp
   string boolString = "True";
   bool boolValue = bool.Parse(boolString);
   ```

4. **Casting boolean to string:**
   ```csharp
   bool boolValue = true;
   string boolString = boolValue.ToString(); // "True"
   ```

Always ensure that the data being parsed or casted is in a format that can be successfully converted to the target type, otherwise, it might throw exceptions or produce unexpected results.

### Time for an excercise!

Write a C# console application that asks the user for their age and greets them accordingly. Here's what the program should do:

1. Display a message asking the user to enter their age.
2. Read the age input from the user.
3. Based on the age input, display one of the following messages:
   - If the age is less than 18, display: "Hello [Name], you are underage."
   - If the age is between 18 and 65 (inclusive), display: "Hello [Name], welcome!"
   - If the age is greater than 65, display: "Hello [Name], enjoy your retirement! 😉"

What the code needs to contain:

- The `name` variable needs to be a nullable variable.
- You need to use string interpolation to include the name in the greeting message.

### switch Statement

```csharp
char grade = 'B';
switch (grade)
{
    case 'A':
        Console.WriteLine("Excellent");
        break;
    case 'B':
        Console.WriteLine("Good");
        break;
    case 'C':
        Console.WriteLine("Fair");
        break;
    default:
        Console.WriteLine("Needs improvement");
        break;
}
```

### operations

### for Loop

```csharp
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);
}
```

### while Loop

```csharp
int count = 0;
while (count < 5)
{
    Console.WriteLine(count);
    count++;
}
```

### Time for an excercise!

Example:

```csharp
string content = "";

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        content += "x";
    }
    content += "\r\n";
}

Console.WriteLine(content);
```

Output:

```
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
xxxxxxxxxx
```

This code creates a string variable named `content` and initializes it to an empty string.

Then, it has two nested loops. The outer loop runs from 0 to 9, and the inner loop also runs from 0 to 9. In each iteration of the inner loop, the code appends the character "x" to the `content` string.

After the inner loop finishes, the code appends the characters "\r\n" to `content`, which represents a newline in Windows-style line endings.

This process repeats 10 times (from 0 to 9) for both loops, so in total, "x" is added 100 times.

So the `i` for loop is for the rows.
and the `j` for loop is for the collumns.

Finally, the `content` string is printed using `Console.WriteLine()`, which displays the content on the console. The result is a 10x10 grid of "x" characters.

## It's your time!

Write similar code with the output of:

```
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
```

When you've done this write code with this output:

```
XOOOOOOOOO
XXOOOOOOOO
XXXOOOOOOO
XXXXOOOOOO
XXXXXOOOOO
XXXXXXOOOO
XXXXXXXOOO
XXXXXXXXOO
XXXXXXXXXO
XXXXXXXXXX
```

Feel free to try out some other patterns. Such as:

```
XOOOOOOOOX
OXOOOOOOXO
OOXOOOOXOO
OOOXOOXOOO
OOOOXXOOOO
OOOOXXOOOO
OOOXOOXOOO
OOXOOOOXOO
OXOOOOOOXO
XOOOOOOOOX
```

```
XXXXXXXXXX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XXXXXXXXXX
```

## Functions

Functions allow you to organize your code into reusable blocks. Let's define a simple function in C#.

```csharp
int Add(int a, int b)
{
    return a + b;
}
```

You can call this function like this:

```csharp
int result = Add(5, 3);
Console.WriteLine(result); // Output: 8
```

## Conclusion

Congratulations! You've now learned the basics of C# programming. You've covered variables, data types, control structures, and functions. With this knowledge, you can start building your own C# applications and exploring more advanced topics in C# development
(If you liked this small tutorial, I can make more in the future).
