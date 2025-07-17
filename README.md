# 🧵 String Interpolation Demo in C#

This project demonstrates the use of **string interpolation** in C# to combine literal strings, variables, and verbatim literals. It includes two example programs showcasing different aspects of interpolation, including handling Unicode strings and file paths.

---

## 📚 Table of Contents

- [🧠 Overview](#-overview)
- [🧪 Technical Terms](#-technical-terms)
- [🧩 Code Breakdown](#-code-breakdown)
  - [📄 Program.cs](#-programcs)
  - [📄 StringInterpolationDemo.cs](#-stringinterpolationdemocs)
- [💡 Why It Matters](#-why-it-matters)
- [⚙️ Setup and Usage](#️-setup-and-usage)
- [📁 File Structure](#-file-structure)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🧠 Overview

This repository contains two C# programs that illustrate **string interpolation**, a feature introduced in C# 6.0 that allows embedding expressions directly within string literals using the `$` prefix. The programs demonstrate combining variables, literal strings, verbatim literals, and Unicode text to produce formatted output.

---

## 🧪 Technical Terms

- **String Interpolation**: Embedding expressions inside string literals using `$` and `{}` syntax.  
  Example: `$"Hello, {name}"`

- **Verbatim Literal**: String literal prefixed with `@` that treats backslashes (`\`) as literal characters.  
  Example: `@"c:\folder\file.txt"`

- **Unicode**: Standard for encoding multilingual text (e.g., `\u041f` = "П").

- **Expression**: A snippet inside `{}` in interpolated strings that gets evaluated and inserted.

---

## 🧩 Code Breakdown

### 📄 Program.cs

```csharp
using System;

namespace StringInterpolationDemo
{
    class Program
    {
        static void Main(string[] args)
        {
            string projectName = "ACME";
            string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434";

            Console.WriteLine(@$"View English output:
    c:\Exercise\{projectName}\data.txt

{russianMessage}:
    c:\Exercise\{projectName}\ru-RU\data.txt");
        }
    }
}
````

### 🔍 Key Features

* ✅ Unicode output in Russian
* ✅ `@$` verbatim + interpolated string
* ✅ Clean formatting of file paths

---

### 📄 StringInterpolationDemo.cs

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        string name = "Alice";
        Console.WriteLine($"Hello, {name.ToUpper()}! Welcome to C# programming.");

        int age = 25;
        string city = "New York";
        Console.WriteLine($"My name is {name}, I'm {age} years old, and I live in {city}.");

        Console.WriteLine($"The current date and time is: {DateTime.Now.ToString("MMMM dd, yyyy HH:mm")}");

        string path = "C:\\Users\\Alice\\Documents";
        Console.WriteLine(@$"The file is located at: {path}\MyFile.txt");
    }
}
```

### 🔍 Key Features

* ✅ Uppercase interpolation
* ✅ Multiple variables combined
* ✅ Date formatting inline
* ✅ Verbatim literals in file paths

---

## 💡 Why It Matters

String interpolation makes C# code **easier to read**, **faster to write**, and **less error-prone** than traditional string concatenation or `String.Format`. These examples show how it can be used in real-world scenarios like:

* User messages
* File path generation
* Internationalization
* Logging and UI feedback

---

## ⚙️ Setup and Usage

### 🧰 Prerequisites

* .NET SDK (6.0 or later)
* Visual Studio or Visual Studio Code

### 🚀 Run the Code

```bash
git clone <repository-url>
cd StringInterpolationDemo
dotnet run
```

---

## 📁 File Structure

```
StringInterpolationDemo/
├── Program.cs                  # Russian + file path example
├── StringInterpolationDemo.cs  # General interpolation demo
└── README.md
```

---

## 🤝 Contributing

Contributions welcome!

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit and push your changes
4. Open a pull request 🚀

---

## 📄 License

This project is licensed under the MIT License.
See the [LICENSE](LICENSE) file for details.

---

```

Let me know if you’d like to add:
- 📸 Screenshots or GIFs  
- 🧪 Unit test examples  
- 🔁 Mermaid diagram for learning flow  
Happy to help!
```

