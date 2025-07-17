String Interpolation Demo

This project demonstrates the use of string interpolation in C# to combine literal strings, variables, and verbatim literals. It includes two example programs showcasing different aspects of string interpolation, including handling Unicode strings and file paths.
Table of Contents

Overview
Technical Terms
Code Breakdown
Program.cs
StringInterpolationDemo.cs


Why It Matters
Setup and Usage
Contributing
License

Overview
This repository contains two C# programs that illustrate string interpolation, a feature introduced in C# 6.0 that allows embedding expressions directly within string literals using the $ prefix. The programs demonstrate combining variables, literal strings, verbatim literals, and Unicode text to produce formatted output.

Program.cs: Displays file paths in English and Russian using string interpolation with verbatim literals.
StringInterpolationDemo.cs: Demonstrates multiple string interpolation techniques, including uppercase conversion, multiple variables, and avoiding intermediate variables.

Technical Terms

String Interpolation: A C# feature that allows embedding expressions inside string literals using $ and {} syntax. Example: $"Hello, {name}".
Verbatim Literal: A string literal prefixed with @ that treats backslashes (\) as literal characters, useful for file paths. Example: @"c:\folder\file.txt".
Unicode: A standard for encoding text characters, used here to represent Russian text via escape sequences (e.g., \u041f for "П").
Expression: A code snippet within {} in an interpolated string that is evaluated and inserted into the output.

Code Breakdown
Program.cs
This program demonstrates string interpolation with verbatim literals and Unicode text to display file paths in English and Russian.
using System;

namespace StringInterpolationDemo
{
    /// <summary>
    /// Demonstrates string interpolation with verbatim literals and Unicode strings.
    /// </summary>
    class Program
    {
        static void Main(string[] args)
        {
            // Define project name and Russian message using Unicode
            string projectName = "ACME";
            string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434"; // "View Russian output"

            // Use verbatim string with interpolation to display file paths
            Console.WriteLine(@$"View English output:
    c:\Exercise\{projectName}\data.txt

{russianMessage}:
    c:\Exercise\{projectName}\ru-RU\data.txt");
        }
    }
}

Key Features:

Unicode Support: Uses Unicode escape sequences to represent Russian text, ensuring multilingual compatibility.
Verbatim Literal with Interpolation: Combines @ for verbatim strings and $ for interpolation to handle file paths with backslashes cleanly.
Why It Matters: This approach simplifies the creation of formatted strings for file paths or multilingual applications without manual string concatenation.

StringInterpolationDemo.cs
This program showcases various string interpolation techniques, including combining variables, avoiding intermediate variables, and using verbatim literals.
using System;

class Program
{
    static void Main(string[] args)
    {
        // 1. Combining a literal string and a variable value, with name in uppercase
        string name = "Alice";
        Console.WriteLine($"Hello, {name.ToUpper()}! Welcome to C# programming.");

        // 2. Using string interpolation with multiple variables and literal strings
        int age = 25;
        string city = "New York";
        Console.WriteLine($"My name is {name}, I'm {age} years old, and I live in {city}.");

        // 3. Avoiding intermediate variables
        Console.WriteLine($"The current date and time is: {DateTime.Now.ToString("MMMM dd, yyyy HH:mm")}");

        // 4. Combining verbatim literals and string interpolation
        string path = "C:\\Users\\Alice\\Documents";
        Console.WriteLine(@$"The file is located at: {path}\MyFile.txt");
    }
}

Key Features:

Uppercase Transformation: Uses ToUpper() within the interpolated string to format the output dynamically.
Multiple Variables: Combines multiple variables (name, age, city) in a single string for concise output.
Direct Expression Evaluation: Avoids intermediate variables by embedding DateTime.Now.ToString() directly in the string.
Verbatim Literals: Uses @$ to handle file paths, making the code more readable and less error-prone.
Why It Matters: These techniques demonstrate how string interpolation can simplify code, improve readability, and handle complex formatting tasks efficiently.

Why It Matters
String interpolation in C# provides a more readable and maintainable alternative to older string formatting methods like String.Format or concatenation. By embedding expressions directly in strings, it reduces errors, simplifies debugging, and supports complex formatting scenarios like multilingual text and file paths. These examples are practical for applications involving user interfaces, file handling, or internationalization.
Setup and Usage

Prerequisites:

.NET SDK (version 6.0 or later)
A code editor like Visual Studio Code


Running the Code:

Clone the repository: git clone <repository-url>
Navigate to the project directory: cd StringInterpolationDemo
Run the program: dotnet run
The output will display formatted strings for both programs.


File Structure:

Program.cs: Contains the Unicode and file path example.
StringInterpolationDemo.cs: Contains the multi-technique interpolation example.



Contributing
Contributions are welcome! Please:

Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
