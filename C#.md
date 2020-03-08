C# (C-Sharp) is a programming language developed by Microsoft that runs on the .NET Framework.

C# is used to develop web apps, desktop apps, mobile apps, games and much more.

.NET Framework is a software framework


.NET consists of:

1. CLR (Common Language Runtime)
2. Class Library (for building applications)



________________CLR_________________

- translates Code in to the Mashine code (Linux for example)
- this work is called JIT (Just In Time compilation)



.NET architecture:



---- Class ----

Data    (state of app)
-> make
-> model
-> color

Methods (functions)
-> Start()
-> Move()




---- Namespace ----

- container for RELATED CLASSES
- unutar Namespace su Classe



---- Assembly (DLL or EXE)----

- container for RELATED NAMESPACES




___________METHODS____________

- have input and output


static void Main(string[] args)            // here args (parameters) are type of STRING array
{                                          // VOID means nothing -> method does not return a Value
	
}



/////////////////////////////////////////////////////////////////////////////////////////////////////////

F5 runs program

```cs
using System;  // namespace as well

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)            // method Main
        {
        	Console.ForegroundColor = ConsoleColor.Blue;   // property
            Console.WriteLine("Hello World!");             // method
        }
    }
}
```
