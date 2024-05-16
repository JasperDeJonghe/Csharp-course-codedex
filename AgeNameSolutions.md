Excercise:
```
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
```
Solution:
```csharp
Console.WriteLine("Please enter your age:");
string? ageInput = Console.ReadLine();

int? age = int.Parse(ageInput);
Console.WriteLine("Please enter your name:");
string? name = Console.ReadLine();

if (age < 18) {
    Console.WriteLine($"Hello {name}, you are underage.");
} else if (age >= 18 && age <= 65) {
    Console.WriteLine($"Hello {name}, welcome!");
} else {
    Console.WriteLine($"Hello {name}, enjoy your retirement!");
}

```