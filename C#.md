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

## Datatypes

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

## Data Conversion and Constants

```cs
// constants -> immutable values (cant change after creation)


using System;

namespace HelloWorld
{
    class Program
    {

    	// constants are OUTSIDE ANY METHODS -> as fields
        const string day = "22.01";  // doesnt need to be STATIC to be used inside class


        static void Main(string[] args)
        {
            bool isit = true;
            bool isnot = !isit;

            string some = "15";  // cant be decimal if using int.Parse()
            int numb = int.Parse(some);

            string some2 = "15.34";
            float numb2 = float.Parse(some2);

            Console.WriteLine(isnot);
            Console.WriteLine(numb);
            Console.WriteLine(numb2);

            Console.WriteLine("My birthday is on: " + day);
            Console.WriteLine("My birthday is on: {0}", day);      // {0} means it adding day variable to that position   
        }
    }
}

// False
// 15
// 15.34
// My birthday is on: 22.01
// My birthday is on: 22.01

https://www.tutorialsteacher.com/articles/convert-string-to-int
```


## Methods

https://www.tutlane.com/tutorial/csharp/csharp-methods-functions-with-examples

```cs
Syntax:

<Access Specifier> <Return Type> <Method Name> (Parameter List)
{
	Method Body
}
```


Access_Specifier - It is used to define an access level either public or private, etc. to allow other classes to access the method. If we didn’t mention any access modifier, 
					then by default it is private. 

Return_Type - It is used to specify the type of value the method can return. In case, if the method is not returning any value, then we need to mention void as return type. 

Method_Name - It must be a unique name to identify the method in a class. 

Parameters - The method parameters are useful to send or receive data from a method and these method parameters are enclosed within parentheses and are separated by commas. 
			 In case, if no parameters are required for a method then, we need to define a method with empty parentheses.



```cs
using System;


namespace Tutlane

{

    class Program

    {
        // string name = "alan";   -> error object reference (variable has to be static)
        static string name = "alan"; // this works

        string name2 = "alan"; // this works because we created -> Program p = new Program();

        static void Main(string[] args)   // Return_Type -> void (no value)
                                          // (string[] args) -> array of strings called args

        {

            Program p = new Program();   // instance of Program class p -> so it can use Program methods

            string result = p.GetUserDetails("Suresh Dasari", 31);  // arguments to store "info" into "result"

            Console.WriteLine(result);
      //    Console.WriteLine(name);   -> error object reference (variable has to be static)
            Console.WriteLine(name);   // this works

            Console.WriteLine(p.name2); // this works because we created -> Program p = new Program();

            Console.WriteLine(GetUserDetails2("Alan", 33)); // calling static method 
        
        }

        public string GetUserDetails(string name, int age)    // Return_Type -> string

        {

            string info = string.Format("Name: {0}, Age: {1}", name, age);

            return info;

        }


        public static string GetUserDetails2(string name, int age)    // STATIC so we dont need to create an INSTANCE of the CLASS (new Program)

        {

            string info = string.Format("Name: {0}, Age: {1}", name, age);

            return info;

        }


    }

}




Name: Suresh Dasari, Age: 31
alan
alan
Name: Alan, Age: 33
```

### Inputs + IF ELSE + TRY CATCH FINALLY

```cs
using System;

namespace Tutlane

{

    class Program

    {

        static void Main(string[] args)
        {
            //NumbCalculator(); // works only if numbers are inputs
            inputValidator(); // if input is string CATCHES an Exception
        }

        public static void NumbCalculator ()
        {
            string input = Console.ReadLine();
            string input2 = Console.ReadLine();
            string operat = Console.ReadLine();

            if (operat == "+")
            {
                Console.WriteLine(int.Parse(input) + int.Parse(input2));
            }
            else if (operat == "-")
            {
                Console.WriteLine(int.Parse(input) - int.Parse(input2));
            }
        }


        public static void inputValidator()
        {
            string input = Console.ReadLine();  

            try        // if integer OK, if string CATCH error exception
            {
                int inputInteger = int.Parse(input);
            }
            catch (Exception)
            {
                Console.WriteLine("That was not an integer");
            }
            finally   // called anyways
            {
                Console.WriteLine("Code called at the end whatever happened; finishing code");
            }

        }
    }
}
```

```cs
// user first signs in and creates account with his details get saved to variables
// then program asks to log in with ne inputs and if loged in inputs are the same as ones he used to sign in
// -> login() is successfull

using System;

namespace Tutlane
{

    class Program

    {
        static string name;
        static string password;

        static void Main(string[] args)
        {
            Console.WriteLine("Please enter your name and password to create account:");

            Signin();

            Login();

    }

        static void Login()
        {
            string loginName = Console.ReadLine();
            string loginPassword = Console.ReadLine();

            if (name == loginName && password == loginPassword)
            {
                Console.WriteLine("Loged in!");

            }
            else
            {
                Console.WriteLine("Invalid credentials, try again.");
                Login();
            };
        }

        static void Signin()
        {
            name = Console.ReadLine();
            password = Console.ReadLine();

            if (name != "" && password != "")
            {
                Console.WriteLine("Account created!");

            }
            else
            {
                Console.WriteLine("Invalid credentials, try again.");
                Signin();
            };
        }
    }
}

```

## OOP Classes


Class is a blueprint of an Object.

-> has methods
-> has properties
-> inheritance


##### Class 1

```cs
using System;

namespace HelloWorld
{

    class Program

    {
        static void Main(string[] args)
        {
            Human alan = new Human();
            alan.Hello();
            Console.WriteLine(alan.firstName);

            Human mick = new Human();
            mick.firstName = "Mick";
            mick.Hello();
            Console.WriteLine(mick.firstName);

        }
    }
}

// Hi Alan
// Alan
// Hi Mick
// Mick
```

##### Class 2 Blueprint

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    class Human
    {
        public string firstName = "Alan"; // must be public to use on instance

        public void Hello() // must be public to use on instance
        {
            Console.WriteLine("Hi " + firstName);
        }
    }
}

```

### Constructors

##### Class 1

```cs
using System;

namespace HelloWorld
{

    class Program

    {
        static void Main(string[] args)
        {
            Human alan = new Human("alan","krajina"); // instance of class
            // class     // calling constructor with arguments
            alan.Hello();

        }
    }
}
    

// Hi alan krajina

```

##### Class 2 Blueprint

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    class Human
    {
        // member variable needed to use in constructor
        private string firstName; // private 
        private string lastName;

        // constructor
        public Human(string firstName, string lastName) // same name as CLASS
        {
            this.firstName = firstName;
            this.lastName = lastName;
        // no methods inside constructor?
        }
        
        public void Hello() // must be public to use on instance
        {
            Console.WriteLine("Hi " + firstName + " " + lastName);
        }
    }
}

```

### Multiple Constructors

##### Class 1

```cs
using System;

namespace HelloWorld
{

    class Program

    {
        static void Main(string[] args)
        {
            Human alan = new Human("alan","krajina"); // instance of class
            // class     // calling constructor with arguments
            Human mick = new Human("mick");
            alan.Hello();
            mick.Hello();


            Console.WriteLine(alan.firstName); // inaccesible since firstName is PRIVATE in Human class
            Console.WriteLine(alan.lastName);  // accessible since lastName is PUBLIC in Human class
 
            // https://code-maze.com/csharp-basics-access-modifiers/
        }
    }
}
    
// Hi alan krajina
// Hi mick
// no value

```
Objects that implement PUBLIC access modifiers are accessible from everywhere in our project. Therefore, there are no accessibility restrictions.

Objects that implement PRIVATE access modifier are accessible only inside a class or a structure. As a result, we can’t access them outside the class they are created.

The PROTECTED keyword implies that the object is accessible inside the class and in all classes that derive from that class.

The INTERNAL keyword specifies that the object is accessible only inside its own assembly but not in other assemblies:



##### Class 2 Blueprint

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    class Human
    {
        // member variable needed to use in constructor
        private string firstName; 
        public string lastName;

        // constructor 1
        public Human(string firstName, string lastName) // same name as CLASS
        {
            this.firstName = firstName;
            this.lastName = lastName;
        }


        // constructor 2 (one less argument)
        public Human(string firstName) 
        {
            this.firstName = firstName;
        }

        public void Hello() // must be public to use on instance
        {
            if (firstName != null && lastName != null)
            {
                Console.WriteLine("Hi " + firstName + " " + lastName);
            }
            else
            {
                Console.WriteLine("Hi " + firstName);
                Console.WriteLine(lastName + "no value");

            }
        }
    }
}


```

### More private + public + Setter + Getter

- changing properties using Setter and getting changed ones using Getter
- accessing data depending if PUBLIC or PRIVATE

##### Class 1

```cs
using System;

namespace HelloWorld
{

    class Program

    {
        static void Main(string[] args)
        {
            Box calc = new Box(2,4,5);
            calc.DisplayInfo();

            calc.SetLength(13); // setter method to change this.length DESTRUCTIVE -> works because SetLength is PUBLIC
            calc.DisplayInfo();

            // Length is 2,height is 4, width is 5 so the volume is 40
            // Length is 13,height is 4, width is 5 so the volume is 260

            // Console.WriteLine(calc.length); // Box.length is inacessible due protection level

            Console.WriteLine(calc.GetLength()); // getter method returns 13 (new length we set in SETTER) -> works because GetLength is PUBLIC
        }
    }
}
```

##### Class 2 Blueprint

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    class Box
    {
        // member variables
        protected int length;  // all inacessible in Main as calc.length  -> (only able to use getter that is PUBLIC)
        private int height; 
        private int width;
        private int volume;

        public Box(int length, int height, int width)
        {
            this.height = height;
            this.length = length;
            this.width = width;
        }

        // setter method 
        public void SetLength(int length)     // acccesable in Main because its public
        {
            this.length = length;
        }

        // getter method
        public int GetLength()                // acccesable in Main because its public
        {
            return this.length;
        }

        public void DisplayInfo()             // acccesable in Main because its public
        {
            Console.WriteLine("Length is {0},height is {1}, width is {2} so the volume is {3}", length, height, width, volume = length*height*width);
        }



    }
}
```

### PROPERTIES (continues on setter and getters)

The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. 
To achieve this, you must:

- declare fields/variables as private
- provide public get and set methods, through properties, to access and update the value of a private field

https://www.w3schools.com/cs/cs_properties.asp

```cs
using System;

namespace HelloWorld
{
    class Person
    {
        private string name; // field
        private string prezime; // field


        private string ime = "Ime1";
        public string ime2 = "Ime2";

        // created to be able to SET and GET -> PRIVATE string name (myObj.Name)
        public string Name   // property (uppercase Name), not a variable
        {
            get { return name; }   // get method
            set { name = value; }  // set method
        }

        // Automatic Properties (Short Hand) -> sets preyime variable as value 
        public string Prezime  // property
        { get; set; }
    }
}

```

```cs
namespace HelloWorld
{

    class Program

    {
        static void Main(string[] args)
        {
            Person myObj = new Person();
            myObj.Name = "Alan";   // SETTING value to lowercase name property from class
            Console.WriteLine(myObj.Name);   // GETTING value of lowercase name property from class

       //   Console.WriteLine(myObj.ime);   // error -> private
            Console.WriteLine(myObj.ime2);  // OK -> public
            
            myObj.Prezime = "Krajina";
            Console.WriteLine(myObj.Prezime);
        }
    }
}


// Alan
// Ime2
// Krajina
```
