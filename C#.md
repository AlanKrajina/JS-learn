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

_________________________________________ DATATYPES __________________________________________________

```cs

using System;

namespace HelloWorld
{
    class Program
    {
        static int age = 15;
        static string word = "Hello";
        static string word2 = "Hello again";  // must be STATIC to use in MAIN
        static float numb = 2.2f;                // must have F to be FLOAT (double -> doesnt need F)

        static void Main(string[] args)
        {
            int age2 = 20;                     // no need to be STATIC - inside method scope
            Console.WriteLine(age);
            Console.WriteLine(age2);
            Console.WriteLine(Program.word);
            Console.WriteLine(word2);
            Console.WriteLine(numb);

        }
    }
}

// When you define a static method or field, it does not have access to 
//	any instance fields defined for the class; it can use only fields that are marked as static. 

https://www.c-sharpcorner.com/UploadFile/abhikumarvatsa/static-and-non-static-fields-in-C-Sharp/
https://github.com/jwill9999/C-Sharp-Cheatsheet#DataTypes
https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/types-and-variables
```


```cs
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            string name = "Alan";
            int leng = name.Length;        // string methods
            string up = name.ToUpper();

            int num1 = 13;
            int num2 = 5;
            int sum = num1 + num2;

            double d1 = 3.5;
            float d2 = 5.5f;
            double sum2 = d1 + d2;

            double sum3 = num1 + d1;

            double first = d1 / num2; // must be double, if INT -> error
                                      // because the result is double
//          var first = d1 / num2;    -> VAR works too

            Console.WriteLine("The sum is: " + sum); // concatonation (+)
            Console.WriteLine("The sum2 is: " + sum2); // concatonation (+)
            Console.WriteLine("The sum3 is: " + sum3); // concatonation (+)
            Console.WriteLine(first);
            Console.WriteLine(name + leng + up);
        }
    }
}

// The sum is: 18
// The sum2 is: 9
// The sum3 is: 16.5
// 0.7
// Alan4ALAN
```
