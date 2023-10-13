# Chapter 1: C# Basics

**Table of Contents**

- [Chapter 1: C# Basics](#chapter-1-C#-basics)
  - [What is C#?](#what-is-C#)
  - [How does C# works?](#How-does-C#-wroks)
  - [Why we choose C#?](#why-we-choose-C#)
  - [Installing C#](#installing-C#)
    - [Windows](#windows)
    - [Linux and Mac OS](#linux-and-mac-os)
  - [Getting Started](#getting-started)
  - [Hello World with C#](#hello-world-with-C#)
  - [Creating, editing, and running C#.](#creating-editing-and-running-C#)
  - [Comment lines](#comment-lines)

## What is C#?

- A popular, modern, and versatile programming language developed by Microsoft.
- It can be used in:
  - Web
  - Mobile and desktop
  - Cloud
  - Microservices

## How does C# works?

- Microsoft's .NET SDK is used to compile your source code. It translates your human-readable code into an intermediate language called Common Intermediate Language (CIL) code or IL code. This CIL code is stored in an assembly file (typically with a ".dll" or ".exe" extension).
- The CIL code can then be executed by the Common Language Runtime (CLR), which is a component of the .NET framework. The CLR just-in-time (JIT) compiles the CIL code into machine code at runtime, making it executable on the specific platform and architecture where the program is running.

In summary, C# is compiled, and the compiled code is executed by the .NET runtime environment. However, the process of converting CIL code into machine code at runtime makes it possible for C# to support features like platform independence and cross-platform development, as the runtime handles the specifics of the underlying hardware and operating system.

## Why we choose C#?

- Strongly Typed Language
- Cross-Platform Development
- Microsoft Ecosystem
- Active Community and Support

## Installing C#

### Windows

Installing C# in windows is so easy. You can just browse https://dotnet.microsoft.com/en-us/ and download the latest/stable version of your choice and follow the instructions.

### Linux and Mac OS

```bash
# Get Ubuntu version
declare repo_version=$(if command -v lsb_release &> /dev/null; then lsb_release -r -s; else grep -oP '(?<=^VERSION_ID=).+' /etc/os-release | tr -d '"'; fi)

# Download Microsoft signing key and repository
wget https://packages.microsoft.com/config/ubuntu/$repo_version/packages-microsoft-prod.deb -O packages-microsoft-prod.deb

# Install Microsoft signing key and repository
sudo dpkg -i packages-microsoft-prod.deb

# Clean up
rm packages-microsoft-prod.deb

# Update packages
sudo apt update

# install dotnet
sudo apt upgrade dotnet-sdk-7.0
```

> Note: The above process is for Ubuntu for other distro and os please visit https://learn.microsoft.com/en-us/dotnet/core/install/

## Getting Started

To verify the C# is installed in your machine, you can run the following in your command prompt or the terminal

```bash
dotnet --version
```

## Hello World with C#

```csharp
Console.WriteLine("Hello, World!");
```

## Creating, editing, and running C#.

we need to create new dotnet project.

```csharp
dotnet new console --name Basic
```

We can create a new file and save with `.cs` extension to create a new C# file. Since C# file is a normal text file, you should be able to open with any text editor. If you want better syntax highlighting and code completion, you can use IDEs or code editors such as VSCode.

```csharp
int a = 10;
int b = 20;
int c = a + b;
Console.WriteLine(c);
```

To run

```csharp
dotnet run
```

## Comment lines

We can create a comment line to either add the documentation to our code or to
prevent the line to be executed.

The comment line is always started with `//`. The python interpreter
ignores the line once it detects the `//` symbol in the line.

If we want to add a short comment to the statement, we can inline the comment
just after the statement so that only the statement executes.

Example:

```csharp
// the lines below  adds two numbers a and b and assign the value to c.
int a = 10; // inline comment
int b = 20;
int c = a + b;  // this is the result

/*
This is a multi-line comment.
I do not need to add // on every line to this type of comment
and I have a good purpose too, which is documentation.
*/

Console.WriteLine(c);
```
