* [Datatypes](#Datatypes)
* [Methods](#Methods)
* [OOP](#OOP)
* [OOP Inheritance](#OOP-Inheritance)
* [Constructors](#Constructors)
* [OOP Polymorphic](#OOP-Polymorphic)
* [Arrays](#Arrays)
* [Single Dimensional Arrays](#Single-Dimensional-Arrays)
* [Multidimensional Arrays](#Multidimensional-Arrays)
* [Jagged Arrays](#Jagged-Arrays)
* [Tic Tac Toe game](#Tic-Tac-Toe-game)
* [Lists](#Lists)
##### Advanced C#
* [Access Modifiers](#Access-Modifiers)
- public, private, protected, internal
* [Properties](#Properties)
- fields, properties, get-set
* [Enums](#Enums)
* [Math class](#Math-class)
* [Regular Expressions](#Regular-Expressions)
* [DateTime class](#DateTime-class)

___________________________________________________________________________________________________________________________________
#### .NET Core vs .NET Framework

https://stackify.com/net-core-vs-net-framework/

o	C# (ASP.NET, dotnet core 2.0+) 
https://docs.microsoft.com/en-us/aspnet/core/?view=aspnetcore-3.1

- Developers use the .NET framework to create Windows desktop applications and server based applications. This includes ASP.NET web applications. 
- .NET Core is used to create server applications that run on Windows, Linux and Mac. 

https://www.tutlane.com/tutorial/csharp/csharp-tutorial


C# (C-Sharp) is a programming language developed by Microsoft that runs on the .NET Framework.

C# is used to develop web apps, desktop apps, mobile apps, games and much more.

.NET Framework is a software framework

.NET consists of:

1. CLR (Common Language Runtime)
2. Class Library (for building applications)


________________CLR_________________

- translates Code in to the Mashine code (Linux for example)
- this work is called JIT (Just In Time compilation)


---- Namespace ----

- container for RELATED CLASSES
- unutar Namespace su Classe



---- Assembly (DLL or EXE)----

- container for RELATED NAMESPACES



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

# OOP 


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


## Class Members

Fields and methods inside classes are often referred to as "Class Members":

https://www.w3schools.com/cs/cs_class_members.asp

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace MembersC
{
    class Program
    {
       
        static void Main(string[] args)
        {
            Members member1 = new Members();
            member1.Introducing(true);
        }
    }
}
```

```cs
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace MembersC
{
    class Members
    {
        // member - private field
        private string memberName;
        private string jobTitle;
        private int salary;

        // member - public field
        public int age;


        // member - property - exposes jobTitle safely - properties start with a capital letter
        public string JobTitle {
            get
            {
                return jobTitle;
            }
            set
            {
                jobTitle = value;
            }
        }


        // public member Method - can be called from other classes
        public void Introducing(bool isFriend)
        {
            if (isFriend)
            {
                SharingPrivateInfo();
            }
            else
            {
                Console.WriteLine("Hi, my name is {0}, and my job title is {1}. I'm {2} years old", memberName, jobTitle, age);
            }

        }


        private void SharingPrivateInfo()   // can be called even Private since its INSIDE PUBLIC METHOD
        {
            Console.WriteLine("My salary is {0}", salary);
        }


        // member constructor with DEFAULT data
        public Members()
        {
            age = 30;
            memberName = "Lucy";
            salary = 60000;
            jobTitle = "Developer";
            Console.WriteLine("Object created");
        }


        // member - finalizer - destructor OPTIONAL
        ~Members()
        {
            // cleanup statements
            Console.WriteLine("Deconstruction of Members object");
            Debug.Write("Destruction of Members object");  // this shows in console
        }

    }
}
```

# OOP Inheritance

## Class Inheritance + overriding methods

##### Main Class

```cs
using System;
using System.Collections;
using System.Collections.Generic;

namespace HelloWorld
{
    class GFG
{
    public static void Main()
    {
        // default constructor with default data (hardcoded)
        Post post1 = new Post();

        // instance with 3 paramaters
        Post post2 = new Post("hello there", true, "John");

            Console.WriteLine(post1);
            Console.WriteLine(post2);

        // calling method with arguments
            post2.Update("what is this ", true);
            Console.WriteLine(post2);

        // created inherited instance of Post class
        InheritFromPostClass imagePost1 = new InheritFromPostClass("Nike", true, "https://...", "Mick");
            Console.WriteLine(imagePost1.ToString());
	    
	
        VideoClass video1 = new VideoClass("https://...", 0.5);
            video1.Play();
        }
    }
}

/*
ID: 0 My first post by alan
ID: 1 hello there by John
ID: 1 what is this  by John
ID: 2 Nike by Mick via link https://...

Song length: 0.5
The Elapsed song time: 0.1
The Elapsed song time: 0.2
The Elapsed song time: 0.30000000000000004
The Elapsed song time: 0.4
The Elapsed song time: 0.5
Song ended
*/
```

##### Class Constructor II (parent)

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    class Post
    {
        private static int currentPostId;

        // properties
        // protected -> can only be used by this class and inherits
        protected int ID { get; set; }
        protected string Title { get; set; }
        protected string SendByUsername { get; set; }
        protected bool IsPublic { get; set; }

        // create CONSTRUCTOR
        public Post()
        {
            ID = 0;
            Title = "My first post";
            IsPublic = true;
            SendByUsername = "alan";
        }

        // instance CONSTRUCTOR with 3 parameters
        public Post(string title, bool isPublic, string sendByUsername)
        {
            this.ID = GetNextID();
            this.Title = title;
            this.IsPublic = isPublic;
            this.SendByUsername = sendByUsername;
        }

        // method to create next ID

        protected int GetNextID()
        {
            return ++currentPostId;
        }

        // method to update title and isPublic values on calling
        // class properties
        public void Update(string title, bool isPublic)
        {
            this.Title = title;
            this.IsPublic = isPublic;
        }

        // class that comes from System
        public override string ToString()
        {
            return String.Format("ID: " + this.ID + " " + this.Title + " by " + this.SendByUsername);
        }
    }
}
```

##### Class that inherits

```cs
using System;
using System.Collections.Generic;
using System.Text;

namespace HelloWorld
{
    // inheritance:
    class InheritFromPostClass:Post
    {
        public string ImageURL { get; set; }

        // constructor I
        public InheritFromPostClass() { }
        // constructor II
        public InheritFromPostClass(string title, bool isPublic, string imageURL, string sendByUsername) 
        {
            // inherited method from Post
            this.ID = GetNextID();

            this.Title = title;
            this.IsPublic = isPublic;
            this.SendByUsername = sendByUsername;

            this.ImageURL = imageURL;
        }

        // overriding Post method to include link
        public override string ToString()
        {
            return String.Format("ID: " + this.ID + " " + this.Title + " by " + this.SendByUsername + " via link " + this.ImageURL);
        }
    }
}

```

#### Timer Class

```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Timers;

namespace HelloWorld
{
    class VideoClass:Post
    {
        public string VideoURL { get; set; }
        public double Length { get; set; }

        private static System.Timers.Timer aTimer;

        public static double Counter;


        // constructor I
        public VideoClass() { }
        // constructor II
        public VideoClass(string videoURL, double length)
        {
            this.Length = length;
            this.VideoURL = videoURL;
        }

        // public member Method - can be called from other classes
        public void Play()
        {
            SetTimer();

            Console.WriteLine("Song length: " + this.Length);
            Console.ReadLine();
        }


        public void SetTimer()
        {

            // Create a timer with a 1 second interval.
            aTimer = Timer(1000);
	    
            // Hook up the Elapsed event for the timer. 
            aTimer.Elapsed += OnTimedEvent;
            aTimer.AutoReset = true;
            aTimer.Enabled = true;
        }

        public void OnTimedEvent(Object source, ElapsedEventArgs e)
        {
            if (Counter != this.Length)
            {
            Counter += 0.1;
            Console.WriteLine("The Elapsed song time: {0}", Counter);
            }
            else
            {
                aTimer.Stop();
                Console.WriteLine("Song ended");
            }
        }


        public override string ToString()
        {
            return String.Format("ID: " + this.ID + " " + this.Length + " length and" + " via link " + this.VideoURL);
        }
    }
}

```

### Interface

- An interface is a completely "abstract class", which can only contain abstract methods and properties (with empty bodies)
- To access the interface methods, the interface must be "implemented" (kinda like inherited) by another class. To implement an interface, use the : symbol (just like with inheritance).

```cs
// Interface
interface IAnimal 
{
  void animalSound(); // interface method (does not have a body)
}

// Pig "implements" the IAnimal interface
class Pig : IAnimal 
{
  public void animalSound() 
  {
    // The body of animalSound() is provided here
    Console.WriteLine("The pig says: wee wee");
  }
}

class Program 
{
  static void Main(string[] args) 
  {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
  }
}
```

# OOP Polymorphic

- Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.


- Inheritance lets us inherit fields and methods from another class. 
- Polymorphism uses those methods to perform different tasks. This allows us to perform a single action in different ways.

- C# provides an option to "override" the base class method, by adding the virtual keyword to the method inside the base class, and by using the override keyword for each derived class methods

##### Why And When To Use "Inheritance" and "Polymorphism"?

- It is useful for code reusability: reuse fields and methods of an existing class when you create a new class.

https://www.w3schools.com/cs/cs_polymorphism.asp

In c#, Run Time Polymorphism means overriding a base class method in the derived class by creating a similar function and this can be achieved by using "override" & "virtual" keywords along with inheritance principle.

https://www.tutlane.com/tutorial/csharp/csharp-polymorphism


##### animalSound() method with a VIRTUAL keyword in the base class to allow derived class to OVERRIDE that method using the OVERRIDE keyword

##### Example 1
```cs
class Animal  // Base class (parent) 
{
  public virtual void animalSound()                     // default VIRTUAL method that gets shared upon inheritance
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public override void animalSound()                  // OVERRIDE default method and give NEW return value
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public override void animalSound()                  // OVERRIDE default method and give NEW return value
  {
    Console.WriteLine("The dog says: bow wow");
  }
}

class Program 
{
  static void Main(string[] args) 
  {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object

    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}

/*
The animal makes a sound
The pig says: wee wee
The dog says: bow wow
*/
```

##### Example 2

```cs
using System;

namespace Tutlane
{
    // Base Class

    public class BClass
    {
        public virtual void GetInfo()
        {
            Console.WriteLine("Learn C# Tutorial");
        }
    }

    // Derived Class

    public class DClass : BClass
    {
        public override void GetInfo()
        {
            Console.WriteLine("Welcome to Tutlane");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            DClass d = new DClass();

            d.GetInfo();

            BClass b = new BClass();

            b.GetInfo();

            Console.WriteLine("\nPress Enter Key to Exit..");

            Console.ReadLine();
        }
    }
}

// 
```

### Sealed

In c#, sealed is a keyword that is used to stop inheriting the particular class from other classes and we can also prevent overriding the particular properties or methods based on our requirements.

- sealed Class
- sealed Methods  (can only seal OVERWRITEN methods!!)
- Sealed Properties

https://www.tutlane.com/tutorial/csharp/csharp-sealed-keyword


### HAS A Relationship

```cs
public class Engine
{
  public int cylinders;
  public int horsepower;

  public void Start()
  {
    System.Console.WriteLine("Engine started");
  }

}

public class Car
{
  public string make;
  public Engine engine;         // Car has an Engine  -> how we "inherit" Engine as engine in Car
  				// now we have an option to access Engine class properties FROM CAR
				// myCar.Start()    -> calls Engine instance method Start()
				// myCar.engine.cylinders

  public void Start()
  {
    engine.Start();
  }

}

class MainClass
{

  public static void Main()
  {
    // CREATING A CAR instance and giving data
    System.Console.WriteLine("Creating a Car object");
    Car myCar = new Car();
    myCar.make = "Toyota";

    // CREATING A ENGINE instance INSIDE myCar.engine          -> and inheriting al engine properties	!!!
    System.Console.WriteLine("Creating an Engine object");
    myCar.engine = new Engine();
    myCar.engine.cylinders = 4;
    myCar.engine.horsepower = 180;

    System.Console.WriteLine("myCar.make = " + myCar.make);
    System.Console.WriteLine("myCar.engine.cylinders = " + myCar.engine.cylinders);    
    System.Console.WriteLine("myCar.engine.horsepower = " + myCar.engine.horsepower);

    myCar.Start();
  }
}

/*
Creating a Car object
Creating an Engine object
myCar.make = Toyota
myCar.engine.cylinders = 4
myCar.engine.horsepower = 180
Engine started
*/
```
### Textfile - read + write

https://www.udemy.com/course/complete-csharp-masterclass/learn/lecture/9567046#overview


# Arrays

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/

- In an array, every element has the same DataType

```cs
class TestArraysClass
{
    static void Main()
    {
        // Declare a single-dimensional array. 
        int[] array1 = new int[5];

        // Declare and set array element values.
        int[] array2 = new int[] { 1, 3, 5, 7, 9 };

        // Alternative syntax.
        int[] array3 = { 1, 2, 3, 4, 5, 6 };

        // Declare a two dimensional array.
        int[,] multiDimensionalArray1 = new int[2, 3];

        // Declare and set array element values.
        int[,] multiDimensionalArray2 = { { 1, 2, 3 }, { 4, 5, 6 } };

        // Declare a jagged array.
        int[][] jaggedArray = new int[6][];

        // Set the values of the first array in the jagged array structure.
        jaggedArray[0] = new int[4] { 1, 2, 3, 4 };
    }
}
```

### Single Dimensional Arrays

```cs
int[] array = new int[5];         

string[] stringArray = new string[6];
int[] array1 = new int[] { 1, 3, 5, 7, 9 };


---> OR:

string[] weekDays2 = { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" };

int[] numbers = { 4, 5, 6, 1, 2, 3, -2, -1, 0 };


	foreach (int i in numbers)
	{
                Console.WriteLine(i);	
	}
	
// Output: 4 5 6 1 2 3 -2 -1 0
```

### Multidimensional Arrays

Multi-dimensional arrays are also known as Rectangular Arrays, due to the fact that the size of every row will always be same.

- 2D [,]
- 3D [,,]

```cs
// two-dimensional array of four rows and two columns:

int[,] array = new int[4, 2];
int[,] array2D = new int[,] 
    {
	{ 1, 2 },   // row 0
	{ 3, 4 },   // row 1
	{ 5, 6 },   // row 2
	{ 7, 8 }    // row 3
     };

Console.WriteLine(array2D[0, 1]);
// 2


// three-dimensional array of four rows and two columns:

int[,,] array3D = new int[,,] 
    {
        {             // [0]                        
	   { 1, 2 },  // array3D[0,0,1]   -> 2 
	   { 3, 4 },  
	}, 
        {
	   { 5, 6 },  
	   { 7, 8 }  
	}
    };



---> OR:

int[,] array4 = { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };

// Console.WriteLine(array2D[1, 1]);
// 4

	foreach (int i in array4)
	{
                Console.WriteLine(i);
	}

// Output: 1 2 3 4 5 6 7 8

```

##### .Length + .Rank
```cs
       Console.WriteLine(array3D.Length);   // returns total number of numbers, like one normal array in JS
       Console.WriteLine(array3D.Rank);     // returns number of dimensions ( {{{ )
	    
// 8
// 3
```
_______________________________________________________________________________________________________________________________________
### Tic Tac Toe game

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace CSharpPractice
{
    class Section7TicTacToe
    {

        static string[,] gameBoard = new string[,]
        {
            {"1", "2", "3"},
            {"4", "5", "6"},
            {"7", "8", "9"}
        };

        static string[] gameBoardOneDimension = new string[10];
        static bool isPlayerXTurn = false;
        static bool gameOver = false;
        static string winner;
        static int movesLeft = 8;

        public static void Main()
        {
            UpdateGameBoard(gameBoard, null);
            Console.WriteLine("Begin game");

            // Main game loop
            while (gameOver == false)
            {
                // Ask for input
                if (isPlayerXTurn)
                    Console.WriteLine("Player X, what is your move? (Enter 1-9)");
                else
                    Console.WriteLine("Player O, what is your move? (Enter 1-9)");
                string input = Console.ReadLine();

                // Validate and check input
                if (!ValidateUserInput(input))
                {
                    Console.WriteLine("You must choose a number from 1-9. Pick again.");
                    continue;
                }
                else if (CheckIfMoveWasAlreadyMade(input))
                {
                    Console.WriteLine("Move already taken. Choose another.");
                    continue;
                }
                else
                {
                    UpdateGameBoard(gameBoard, input);
                    movesLeft--;
                }
            }

            Console.WriteLine("Game over.");
            if (winner != null)
                Console.WriteLine("Player {0} wins!", winner);
            else
            {
                Console.WriteLine("Stalemate.");
            }
        }

        public static bool ValidateUserInput(string input)
        {
            bool success = int.TryParse(input, out int parsedValue);
            if (success && parsedValue > 0 && parsedValue < 10)
                return true;
            else
                return false;
        }

        public static bool CheckIfMoveWasAlreadyMade(string playerMove)
        {
            if (gameBoardOneDimension[Int32.Parse(playerMove) - 1] == "X" || gameBoardOneDimension[Int32.Parse(playerMove) - 1] == "O")
                return true;
            else
                return false;
        }

        public static void SwitchPlayers()
        {
            isPlayerXTurn = !isPlayerXTurn;
        }
        public static void RedrawGameBoard(string[] gameBoardOneDimension)
        {
            Console.Clear();
            string[] a = gameBoardOneDimension;
            // Designed to match the number pad
            Console.WriteLine("------------------");
            Console.WriteLine("     |     |       ");
            Console.WriteLine("  " + a[6] + "  |  " + a[7] + "  |  " + a[8]);
            Console.WriteLine("     |     |       ");
            Console.WriteLine("------------------");
            Console.WriteLine("     |     |       ");
            Console.WriteLine("  " + a[3] + "  |  " + a[4] + "  |  " + a[5]);
            Console.WriteLine("     |     |       ");
            Console.WriteLine("------------------");
            Console.WriteLine("     |     |       ");
            Console.WriteLine("  " + a[0] + "  |  " + a[1] + "  |  " + a[2]);
            Console.WriteLine("     |     |       ");
            Console.WriteLine("------------------");
        }
        public static void UpdateGameBoard(string[,] gameBoard, string playerMove)
        {
            // Convert 2d array to 1d array, then pass to PrintGameBoard
            // Create counter variable to get the proper index of gameBoardOneDimension inside the nested loop
            int counter = -1;
            // Then iterate over a 2d array, by columns first, then by row, using the built in GetLength property of the 2D array
            for (int col = 0; col < gameBoard.GetLength(0); col++)
            {
                for (int row = 0; row < gameBoard.GetLength(1); row++)
                {
                    counter++;

                    // Check if the player's move matches the element and if so, replace with that move in both arrays
                    if (playerMove == gameBoard[col, row])
                    {

                        if (isPlayerXTurn)
                        {
                            gameBoardOneDimension[counter] = "X";
                            gameBoard[col, row] = "X";
                        }
                        else
                        {
                            gameBoardOneDimension[counter] = "O";
                            gameBoard[col, row] = "O";
                        }
                    }
                    else
                    {
                        gameBoardOneDimension[counter] = gameBoard[col, row]; // Assigning each element in order to a 1D array
                    }
                }
            }
            SwitchPlayers();
            RedrawGameBoard(gameBoardOneDimension);
            CheckIfGameOver();
        }

        public static bool CheckIfGameOver()
        {
            // Check for winner
            for (int i = 0; i < 3; i++)
            {
                // Check all rows for a win
                if (gameBoard[i, 0] == gameBoard[i, 1] && gameBoard[i, 1] == gameBoard[i, 2])
                {
                    winner = gameBoard[i, 0];
                    return gameOver = true;

                }
                // Check all columns for a win
                if (gameBoard[0, i] == gameBoard[1, i] && gameBoard[1, i] == gameBoard[2, i])
                {
                    winner = gameBoard[0, i];
                    return gameOver = true;
                }
            }

            // Then check crosses for a win
            if (gameBoard[0, 0] == gameBoard[1, 1] && gameBoard[1, 1] == gameBoard[2, 2])
            {
                winner = gameBoard[0, 0];
                return gameOver = true;

            }
            if (gameBoard[0, 2] == gameBoard[1, 1] && gameBoard[1, 1] == gameBoard[2, 0])
            {
                winner = gameBoard[0, 2];
                return gameOver = true;
            }

            // Finally, check for stalemate (so a player can win on the last move)
            if (movesLeft == 0)
            {
                return gameOver = true;
            }

            return gameOver = false;
        }
    }
}
```
___________________________________________________________________________________________________________________________________

### Jagged Arrays 

- (nested from js)

A jagged array is an array whose elements are arrays. The elements of a jagged array can be of different dimensions and sizes. A jagged array is sometimes called an "array of arrays." 


Printing everything in 1 row:

```cs
            int[][] jaggedArray3 =
            {
                new int[] { 1, 3, 5, 7, 9 },             // jedan nacin
                new int[] { 0, 2, 4, 6 },
                new int[] { 11, 22 }
            };

            foreach (int[] array in jaggedArray3)
            {
                Console.WriteLine("Rows");

                foreach (int i in array)
                {
                    Console.WriteLine(i);          // brojke idu prema dolje jer C.WriteLine stvara novi red za svaki broj
                }
            }
/*	    
Rows
1
3
5
7
9
Rows
0
2
4
6
Rows
11
22
*/

```
##### Printing everything in 2 rows:

```cs
// Declare the array of two elements.
        int[][] arr = new int[2][];

// Initialize the elements.
        arr[0] = new int[5] { 1, 3, 5, 7, 9 };        // FIRST NESTED array
        arr[1] = new int[4] { 2, 4, 6, 8 };           // SECOND NESTED array


// Display certain element
        Console.Write("{0}", arr[0][1]);
// 3


// Display the array elements.                           
            for (int i = 0; i < arr.Length; i++)          // iteration through outer array (empty)
            {

                for (int j = 0; j < arr[i].Length; j++)   // iteration through inner 2 arrays (done twice)
                {
                    Console.Write(arr[i][j]);   
                }
                Console.WriteLine();                      // zbog ovoga je u dva reda a ne (135792468)
            }


/* 
13579
2468
*/

EXAMPLE 2:

            int[][] a = new int[][] { 
                new int[] { 0, 0 }, 
                new int[] { 1, 2 }, 
                new int[] { 2, 4 }, 
                new int[] { 3, 6 }, 
                new int[] { 4, 8 } };
            int i, j;

            for (i = 0; i < 5; i++)
            {
                for (j = 0; j < 2; j++)
                {
                    Console.WriteLine("a[{0}][{1}] = {2}", i, j, a[i][j]);
                }
            }

            // accessing element from a jagged array
            Console.WriteLine(a[2][1]);


        }
	    
/*	    
a[0][0] = 0            a[outer index][inner index] = number
a[0][1] = 0
a[1][0] = 1
a[1][1] = 2
a[2][0] = 2
a[2][1] = 4
a[3][0] = 3
a[3][1] = 6
a[4][0] = 4
a[4][1] = 8
4
*/	    

## logging out first nested array:

            int counter = 0;

            for (int i = 0; i < arr.Length; i++)                  // iteration through OUTER nested array 
            {

                if (counter == 0)                                 // if TRUE continues to iterate
                {
                    for (int j = 0; j < arr[i].Length; j++)       // iteration through FIRST nested array (arr[0])
                {
                    Console.Write(arr[i][j]);
                }
                }                        
                counter++;                                      // then it updates counter after ONE ITERATION

                if (counter == 0)                               // not TRUE -> STOPS all iteration
                {
                    Console.Write("Second row: ");
                    for (int j = 0; j < arr[i].Length; j++)     // iteration through SECOND nested array (arr[1])
                    {
                        Console.Write(arr[i][j]);
                    }
                }
            }
	    
// 13579
```

### Array as property (argument)

```cs
        static void Main(string[] args)
        {
            int[] gradesArray = { 1, 2, 3, 4, 10 };
            GetAverage(gradesArray);
        }

        static void GetAverage(int[] gradesArray)
        {
            int total = gradesArray.Length;
            int numbers = 0;

            foreach (int i in gradesArray)
            {
                numbers += i;
            }

            Console.WriteLine(numbers/total);
        }

// 4
```

## ArrayList - 	not used anymore

- It can contain elements of any data types. 
- It is similar to an array, except that it grows automatically as you add items in it. 

Properties of ArrayList Class:

- Elements can be added or removed from the Array List collection at any point in time.
- The ArrayList is not guaranteed to be sorted.
- The capacity of an ArrayList is the number of elements the ArrayList can hold.
- Elements in this collection can be accessed using an integer index. Indexes in this collection are zero-based.
- It also allows duplicate elements.
- Using multidimensional arrays as elements in an ArrayList collection is not supported.

https://www.geeksforgeeks.org/c-sharp-arraylist-class/

```cs
using System;
using System.Collections;            // important for ArrayList
using System.Collections.Generic;

class GFG
{

    // Driver code  
    public static void Main()
    {

        // Creating an ArrayList 
        ArrayList myList = new ArrayList(10);

        // Adding elements to ArrayList 
        myList.Add(2);                     // array method
        myList.Add("hello");
        myList.Add(6);
        myList.Add(8);
        myList.Add(10);
        myList.Add(12);
        myList.Add(14);
        myList.Add(16);
        myList.Add(18);
        myList.Add(20);

        // Displaying the elements in ArrayList 
        Console.WriteLine("The initial ArrayList: ");

        foreach (object i in myList)                           // object umjesto int tako da moze i "hello" logirat
        {
            Console.WriteLine(i);
        }

        // removing 4 elements starting from index 0 
        myList.RemoveRange(0, 4);                                // array method (slice)

        // Displaying the modified ArrayList 
        Console.WriteLine("The ArrayList after Removing elements: ");

        // Displaying the elements in ArrayList 
        foreach (int i in myList)
        {
            Console.WriteLine(i);
        }
    }
}

/*
The initial ArrayList: 
2
"hello"
6
8
10
12
14
16
18
20
The ArrayList after Removing elements: 
10
12
14
16
18
20
*/
```

## Lists

- Represents the list of objects which can be accessed by index. 
- It comes under the System.Collection.Generic namespace. 
- List class can be used to create a collection of different types like integers, strings etc. List<T> class also provides the methods to search, sort, and manipulate lists

Characteristics:

- It is different from the arrays. A List<T> can be resized dynamically but arrays cannot.
- List<T> class can accept null as a valid value for reference types and it also allows duplicate elements.
- If the Count becomes equals to Capacity, then the capacity of the List increased automatically by reallocating the internal array. - - The existing elements will be copied to the new array before the addition of the new element.
- List<T> class is the generic equivalent of ArrayList class by implementing the IList<T> generic interface.
- This class can use both equality and ordering comparer.
- List<T> class is not sorted by default and elements are accessed by zero-based index.
- For very large List<T> objects, you can increase the maximum capacity to 2 billion elements on a 64-bit system by setting the enabled attribute of the configuration element to true in the run-time environment.
	
https://www.geeksforgeeks.org/c-sharp-list-class/

https://www.bitdegree.org/learn/c-sharp-list
	

Jedan nacin kreiranja Liste:
```cs
        List<string> names = new List<string>()            // sa default elementima prvo
        {"Marge", "Homer"};
        names.Add("Lisa");
        names.Add("Bart");
        names.Remove("Homer");
        foreach (var name in names)
        {
            Console.WriteLine(name);
        }
```
	
	
```cs
        // Creating an List<T> of Integers 
        List<int> firstlist = new List<int>();    // ovo onda -> List<object> firstlist = new List<object>();
  
        // Adding elements to List 
        firstlist.Add(17); 
        firstlist.Add(19);                     // ovo moze biti -> firstlist.Add("hello");
        firstlist.Add(21); 
        firstlist.Add(9); 
        firstlist.Add(75); 
        firstlist.Add(19); 
        firstlist.Add(73); 
  
        Console.WriteLine("Elements Present in List:\n"); 
  
        int p = 0; 
  
        // Displaying the elements of List 
        foreach(int k in firstlist)                             // ovdje -> object
        { 
            Console.Write("At Position {0}: ", p); 
            Console.WriteLine(k); 
            p++; 
        } 
  
        Console.WriteLine(" "); 
  
        // removing the element at index 3 
        Console.WriteLine("Removing the element at index 3\n"); 
  
        // 9 will remove from the List 
        // and 75 will come at index 3 
        firstlist.RemoveAt(3); 
  
        int p1 = 0; 
  
        // Displaying the elements of List 
        foreach(int n in firstlist)                             // ovdje -> object
        { 
            Console.Write("At Position {0}: ", p1); 
            Console.WriteLine(n); 
            p1++; 
        } 
	
		// accessing element	
	        Console.WriteLine(firstlist[0]);
		// 17
		
		// clearing whole list	
	        firstlist.Clear();


```cs
Elements Present in List:

At Position 0: 17
At Position 1: 19                           // hello
At Position 2: 21
At Position 3: 9
At Position 4: 75
At Position 5: 19
At Position 6: 73
 
Removing the element at index 3

At Position 0: 17
At Position 1: 19                          // hello
At Position 2: 21
At Position 3: 75
At Position 4: 19
At Position 5: 73
```

### Difference between List and ArrayList and Arrays

List<T> is a generic class. It supports storing values of a specific type without casting to or from object (which would have incurred boxing/unboxing overhead when T is a value type in the ArrayList case). ArrayList simply stores object references. As a generic collection, List<T> implements the generic IEnumerable<T> interface and can be used easily in LINQ (without requiring any Cast or OfType call).

ArrayList belongs to the days that C# didn't have generics. It's deprecated in favor of List<T>. You shouldn't use ArrayList in new code that targets .NET >= 2.0 unless you have to interface with an old API that uses it.

Arrays are limited to one type (int, string..)

```cs
        // immutable Array - limited to one type

        int[] scores = { 1, 2, 3, 4, 5 };

        // List 
        List<int> list = new List<int>();

        // adding elements  
        list.Add(2);                               // add method
        list.Add(1);
        list.Add(3);
        list.Add(5);
        list.Add(4);

        // Printing elements of List 
        foreach (object i in list)
        {
        Console.WriteLine(i);
        }

        list.Sort();                              // sort method

        // Printing SORTED elements of List 
        foreach (object i in list)
        {
            Console.WriteLine(i);
        }
    }
}

/*
2
1
3
5
4
1
2
3
4
5
*/
```

### Lambda expessions

```cs
        // Creating an List<T> of Integers 
        List<int> firstlist = new List<int>();

        // Adding elements to List 
        firstlist.Add(17);
        firstlist.Add(21);
        firstlist.Add(9);
        firstlist.Add(75);
        firstlist.Add(19);
        firstlist.Add(73);

	// .FindIndex
        int index = firstlist.FindIndex(el => el == 9);    // can only FindIndex if integer List
        Console.WriteLine(index);
	
	// 2
	
	
	// .ForEach
	firstlist.ForEach(el => Console.WriteLine(el));
	
	/*
	17
	21	
	9
	75
	19
	73
	*/
	
	
	int[] numbers = { 4, 5, 6, 1, 2, 3, -2, -1, 0 };

        numbers.ForEach(el => Console.WriteLine(el));            // ERROR -> cannot be used on array, only LIST
	
	
    }
    
```

### Access Modifiers

- The public keyword is an access modifier, which is used to set the access level/visibility for classes, fields, methods and properties.

To achieve "Encapsulation" - which is the process of making sure that "sensitive" data is hidden from users. This is done by declaring fields as PRIVATE. 

- we can use SETTERS and GETTERS 


Modifier---------Description
____________________________________________________________________________________________________________________________________
PUBLIC---------The code is accessible for all classes

PRIVATE---------The code is only accessible within the same class ( 2 files with 2 classes -> I class creates private, II class Main CAN'T use it)

```cs
class Car
{
  private string model = "Mustang";
}

class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);        // cant use 
  }
}

// 'Car.model' is inaccessible due to its protection level                  -> ERROR
```

PROTECTED---------The code is accessible within the same class, or in a class that is inherited from that class

INTERNAL---------The code is only accessible within its own assembly, but not from another assembly. 

### Properties

The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must:

- declare fields/variables as private
- provide public get and set methods, through properties, to access and update the value of a private field

https://www.w3schools.com/cs/cs_properties.asp

- uppercase Name -> property
- lovercase name -> field

##### Main:
```cs
namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Person myObj = new Person();
            myObj.Name = "Liam";                 // SET property
            myObj.Prezime = "Krajina";           // SET property
	    
            Console.WriteLine(myObj.Name);       // GET property
            Console.WriteLine(myObj.Prezime);    // GET property

            Console.WriteLine(myObj.name2);      // public
            // Console.WriteLine(myObj.name3);   // error protected

            myObj.name2 = "Alan2";               // reassigned FIELD value
            Console.WriteLine(myObj.name2);
        }
    }
}

/*
Liam
Krajina
alan
Alan2
*/
```

##### Class II:
```cs
namespace ConsoleApp1
{
    class Person
    {
        public string name2 = "alan";
        private string name3 = "John";

	// OVO NE KORISTIT
        private string name;           // field lowercase koji moram imat sa long syntax PRIVATE -> zbog toga GET i SET
        public string Name             // uppercase property - long syntax
        {
            get { return name; }
            set { name = value; }
        }

	// OVO KORISTIT
        public string Prezime          // uppercase property - short syntax (ovdje mi ne treba lowercase prezime prije ovog)
        { get; set; }
    }
}
```

### Enums

- An enum is a special "class" that represents a group of constants (unchangeable/read-only variables).

https://www.w3schools.com/cs/cs_enums.asp

```cs
class Program
{
  enum Level
  {
    Low,          // 0
    Medium,       // 1
    High          // 2
  }
  static void Main(string[] args)
  {
    Level myVar = Level.Medium;       // accessing value
    Console.WriteLine(myVar);
    
   int myNum = (int) Level.Medium;    // accessing index
   Console.WriteLine(myNum);

  }
}

// Medium
// 1
```

### Math class

https://www.w3schools.com/cs/cs_math.asp

Math.Max(x,y)
```cs
Math.Max(5, 10);

// 10
```

Math.Sqrt(x);
```cs
Math.Sqrt(64);

// 8
```

Math.Round()
```cs
Math.Round(9.99);

// 10
```


### Regular Expressions

https://regexr.com/   -> CONSOLE

https://www.dotnetperls.com/regex   -> C# examples

https://www.mikesdotnetting.com/article/46/c-regular-expressions-cheat-sheet


### DateTime class

https://www.c-sharpcorner.com/article/datetime-in-c-sharp/

```cs
var date1 = new DateTime(2008, 5, 1, 8, 30, 52);
Console.WriteLine(date1);

var dat1 = new DateTime();
Console.WriteLine(dat1);

DateTime date2 = DateTime.Now;
DateTime date3 = DateTime.UtcNow;
DateTime date4 = DateTime.Today;
Console.WriteLine(date2);
Console.WriteLine(date3);
Console.WriteLine(date4);

/*
5/1/2008 8:30:52 AM
1/1/0001 12:00:00 AM
3/13/2020 12:53:30 PM
3/13/2020 12:53:30 PM
3/13/2020 12:00:00 AM
*/


            DateTime myDate = new DateTime(2015, 12, 25, 10, 30, 45);
            int year = myDate.Year;              // 2015  
            int month = myDate.Month;            // 12  
            int day = myDate.Day;                // 25  
            int hour = myDate.Hour;              // 10  
            int minute = myDate.Minute;          // 30  
            int second = myDate.Second;          // 45  
            int weekDay = (int)myDate.DayOfWeek; // 5 due to Friday 
	    
```
