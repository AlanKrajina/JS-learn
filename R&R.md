## What is Rails?

Rails is an open source web application framework written in Ruby. It is a full-stack framework that has been optimised for programmer happiness and sustainable productivity. It emphasises the use of well-known software engineering patterns and paradigms, including convention over configuration (CoC), don't repeat yourself (DRY), the active record pattern, and model–view–controller (MVC).

Extra: David Heinemeier Hansson (DHH) is the creator of Rails, having extracted it from his work on Basecamp. He first released Rails as open source in July 2004.

Useful Links:

http://en.wikipedia.org/wiki/Ruby_on_Rails

## What are the components of Rails MVC?

MVC: Model-View-Controller

Model (ActiveRecord) The model is the central component of MVC and contains the logic of the application. It is independent of the user interface. For example, if one were writing a game, the model would be equivalent of the game engine. That is, it would contain the logic of the game.

View (ActionView) A view is a representation of the information from the model. In a game situation, it would display the game and provide an interface for the user.

Controller (ActionController) Lastly, the controller bridges the model and the view. If a user were playing a game, the instructions entered from the view would be passed to the model. In addition, the controller would use information from the model and control which view is rendered.

Useful Links

http://www.tutorialspoint.com/ruby-on-rails/rails-framework.htm

## What are the Rails naming conventions?

Rails uses both snake_case and camelCase in different situations

Model names are singular and capitalised.

e.g. User or Post

Controller names are generally pluralised and written in camel case.

e.g. UsersController, PostsController

However there are some exceptions (e.g. SessionController, ApplicationController)

View names should match the action names in the controller to which they are associated with.

e.g. ‘posts#show’ would correspond to show.html.erb (in /views/posts)

Migrations are capitalised and written in camel case.

e.g. CreateUsers

Table names are pluralised with underscores if necessary (as opposed to camel case).

e.g. users

Join tables names are made up the pluralised version of both of the relevant tables. These are alphabetised and separated by an underscore.

e.g. libraries_posts

## How would I execute some code for each element in a collection?

In Ruby, it is encouraged that one iterates over a collection using an enumerable. Although traditional loops are available, they are not considered to be idiomatic Ruby. A good Rubyist will be aware of the available enumerables and select the right one for the job.

Below is a list Ruby enumerables in Ruby 2.2.1 http://ruby-doc.org/core-2.2.1/Enumerable.html

## Name a few object-oriented concepts in Ruby

Object-oriented programming" (OOP) is at the core of Ruby (and modern programming). In a nutshell, object-oriented programming sees the world as data, modeled in code by "objects." 

**Classes:**

In Ruby, every value is an object, even the most primitive things: strings, numbers and even true and false. Even a class itself is an object that is an instance of the Class class. A class provides a blueprint for objects, so basically an object is created from a class.

**Inheritance:**

One of the most important concepts in object-oriented programming is that of inheritance. Inheritance allows you to define a class in terms of another class, which makes it easier to create and maintain an application.

**Instance Variables:**

Instance variables are kind of class attributes and they become properties of objects once the objects are created using the class. Every object's attributes are assigned individually and share no value with other objects. They are accessed using the @ operator within the class but to access them outside of the class we use public methods which are called accessor methods.

**Class Variables:**

Class variables are shared between all instances of a class. In other words, there is one instance of the variable and it is accessed by object instances. Class variables are prefixed with two @ characters (@@).

**Useful links:**

- http://ruby.bastardsbook.com/chapters/oops/
- http://www.tutorialspoint.com/ruby/ruby_object_oriented.htm

##When should load be used in Ruby, as opposed to require?

**Require:**

First off, there is the $LOAD_PATH (short version, $:). This is a global variable that holds an Array object of strings, each one describing a path where files can be loaded. This will include various paths in your system where Ruby's standard library lives, as well as some other things If you're using Rubygems, when the Rubygems library itself is loaded it will hijack the require method itself. Rubygems will search through its paths, but Rubygems paths generally don't appear in $LOAD_PATH.

Second, it loads more than Ruby files. Native extensions are loaded as .so, .dll or similar. These are files that hold compiled machine code, with symbol tables that Ruby then uses to hook up to Ruby methods. These are important, it's how Ruby touches the outside
world. Any Ruby bindings to any library is bound to use one of these files. And you don't even know it, you just say require 'nokogiri', it doesn't matter to you that Nokogiri was compiled natively. The 'require' method figures out the extension you really want for you.

Lastly, the require method remembers what it has already loaded. If you require the same file twice, nothing at all will happen. The first time you require it, it will load the file as normal. The second time you require it, nothing will happen. The require method itself will even return false to signify this (if something goes really wrong and the file doesn't exist, a LoadError exception will be raised). The list of required modules can be found in the $LOADED_FEATURES global variable (short version is $").

**Load:**

On to the load method. The load method can be thought of as requires less sophisticated cousin. It does the same job, but it doesn't do so in such a professional manner. It doesn't guess which file extension you want, and it doesn't remember or even care what's been loaded or required already.

The load method is almost like the require method except it doesn’t keep track of whether or not that library has been loaded. So it’s possible to load a library multiple times and also when using the load method you must specify the “.rb” extension of the library file name.
Most of the time, you’ll want to use require instead of load but load is there if you want a library to be loaded each time load is called. For example, if your module changes its state frequently, you may want to use load to pick up those changes within classes loaded from.

You will probably never want to use load in practice.


##What are filters in Rails? Give some examples.

Filters are methods that are run before, after or “around” a controller action. These methods can halt the action processing by redirecting or set up common data to every action in the controller. 

Before - common example is authenticating a user and checking whether or not they should be allowed to see the result of a certain action.

After - these run after the action completes and can modify the response, e.g. ActiveRecord::Base.connection.close (works like db.close) in a Sinatra app.

Around - these may have logic that runs before and after the action, and yield to the action in the relevant place, can be used to catch exceptions for actions while the app is running and log bugs.

N.B. Used to be called filters but now you can use action as a keyword as well.

##What are GET and POST methods?

GET and POST methods are part of the REST software architecture style.

GET requests are used to retrieve data from a server. They are typically used for safe actions (or actions without side effects) so that web crawlers cannot edit or delete data on a site. GET requests can be shared and bookmarked, and remain in browser history.

POST requests are used to insert or update data on a server. They submit data to be processed to an identified resource (e.g. submitting an HTML form). A POST request is used when dealing with sensitive data so that any personal info is not shown in the URL or saved in the browser history.

Key things to mention: RESTful, HTTP verbs, GET request shouldn’t update anything on the server, POST changes stuff on the server and you don’t see the data in the URL.

Further reading - http://blog.teamtreehouse.com/the-definitive-guide-to-get-vs-post

##What is YAML?

YAML is an acronym for “YAML Ain't Markup Language” and is a human friendly data serialisation standard for programming languages.

Early on, YAML was said to mean "Yet Another Markup Language", but it was reinterpreted to distinguish its purpose as data-oriented, rather than document markup.

The syntax was designed to be easily mapped to data types common to most high-level languages such as arrays and hashes.

In Ruby on Rails applications, YAML is used to compile the databases.

Useful Links:
- http://en.wikipedia.org/wiki/YAML
- http://yaml.org/
- https://blog.udemy.com/ruby-yaml/

##Give some examples of what you could define in a Rails model.

In a model, you can define the association to other models. For example, you can define if it is a one-to-one, one-to-many, many-to-many etc. In addition, you can define whether the model belongs to another model or if it has other models.

If the rails application were a game, the logic of the game could be defined in the relevant models.

Also very important: validations.

##How does GPS work?

##How do you add a method to jQuery?

##What is browser sniffing? When would you use it?

#B team

##What is meant by convention over configuration?

The idea that you have certain placing or naming conventions so you don't have to explicitly tell the program where stuff is or what it is called.

Seeks to decrease the number of decisions developers need to make, gaining simplicity, but not necessarily losing flexibility. 

A lot of tedious or repetitive code - which is explicit or configuration - is replaced by simple naming and directory structure conventions.

It comes down to being less explicit and more implicit.

Another way you can describe convention over configuration is 'sensible defaults'. Eg in Active Record if you have a class called User, it will by default look for the plural version of the classname, which is Users, even though you could call it Customers.

**Response on convention over configuration by @joshuapaling:**

```
predetermined way of doing common things (convention) alleviates ppl of the need to make explicit choices (configuration)
```

##What is MVC?

MVC is a design pattern for building graphic user interfaces.

It stands for models, views and controllers.

The model is the data and data management of the application.

The view is the visual representation of the data. It renders data from the model into a form that is suitable for the user interface.

And the controller is the interface between both the view and the model. It receives user input and makes calls to model objects and the view to perform appropriate actions.

MVC is designed to separate logic from the user interface.

The point of using an MVC pattern is separation of concerns. 

##Explain RESTful architecture.

The REST in RESTful architecture stands for Representational State Transfer, which is a software architecture style consisting of guidelines and best practices for creating scalable web services.

RESTful systems typically, but not always, communicate over the Hypertext Transfer Protocol with the same HTTP verbs (GET, POST, PUT, DELETE, etc.) used by web browsers to retrieve web pages and send data to remote servers.

The idea behind all of this, the key thing to keep in mind, is that we use the same URL for different purposes.

So if I am dealing with blog posts, the url http://someting.com/posts/7 can refer to a single object, and all the things we might want to do with this object are all at the same URL.

The way we refer to the object is by using different verbs, such as GET, POST, PUT, DELETE.

They are all happeneing to the same URL, but the verbs are different.

The representation is the URL that we are dealing with, and the state is the GET, UPDATE, DELETE, telling it what we want to do with it.

So as long as you know what the URL is, it should respond to all of these verbs. 

RESTful architecture allows us to have one URL for each object, and we use different verbs to interact with it in different ways. It prevents us from having 15 different URLs for one object. 

That is RESTful architecture. 

If they ask you how you would design an API, you would say using a RESTful architecture. 

##Explain the difference between empty? and nil?

Nil is a Ruby method that can be used on any object and returns true if the object is nil and false for anything else.

```
b = nil
b.nil? # => true
```

Empty is a Ruby method that can be used on some objects, such as strings, arrays and hashes, and returns true if their lengths are 0, or if the object contains no elements.

```
a = []
a.empty? # => true
```

Running the empty method on something that is nil will throw a no method error.

```
[1] pry(main)> nil.empty
NoMethodError: undefined method `empty' for nil:NilClass
```

**Response on the difference between empty and nil by @joshuapaling:**

```
Empty: we know you have no Middle Name - your MN is ''
Nil: Your MN has no value in the DB, so don't know if you have one or not
```

##Provide an example showing how an iterator is used

**JS for loop example:** 

```

var things = ['a', 'b', 'c']

for (var i = 0; i < things.length; i++) {
    console.log(things[i]);
  };
    
```

**Ruby each loop example:**

```
(0..5).each do |i|
  puts "Value of local variable is #{i}"
end
```

**Ruby times method:**
```
5.times do |i|
    puts i
end
```

##What is the difference between an argument and a parameter?

Function parameters are the names listed in the function definition.

Function arguments are the real values passed to (and received by) the function.

A parameter is a variable in a method definition. When a method is called, the arguments are the data you pass into the method's parameters.

````
functionName(parameter1, parameter2, parameter3) {
    code to be executed
}

functionName(argument1, argument2, argument4);

```

In reality, the terms can be used interchangebly. 

##Explain how sessions work, specifically in relation to cookies.

A session refers to a limited time of communication between two systems. Some sessions involve a client and a server, while other sessions involve two personal computers.

A common type of client/server session is a Web or HTTP session. An HTTP session is initiated by a Web browser each time you visit a website. While each page visit constitutes an individual session, the term is often used to describe the entire time you spend on the website. For example, when you purchase an item on an ecommerce site, the entire process may be described as a session, even though you navigated through several different pages.

Browser cookies come in two different flavors: "session" and "persistent." Session cookies are temporary and are deleted when the browser is closed. These types of cookies are often used by e-commerce sites to store items placed in your shopping cart, and can serve many other purposes as well. Persistent cookies are designed to store data for an extended period of time. Each persistent cookie is created with an expiration date, which may be anywhere from a few days to several years in the future. Once the expiration date is reached, the cookie is automatically deleted. Persistent cookies are what allow websites to "remember you" for two weeks, one month, or any other amount of time.

Joel says this question might be more in relation to the interaction between how Rails keeps track of which user owns which session via cookies.. this is explained in the Rails Guide: http://guides.rubyonrails.org/security.html

##Andrew: what is The Halting Problem and what are its ramifications?

The halting problem is the problem of determining, whether a computer program will finish running or continue to run forever, such as an infinite loop.  Such as in psudocode: if (true) continue doesn't halt, whereas print "hello world" does halt. In 1936 Alan Turing proved no algorithm can exist which will always correctly decide whether, for a given arbitrary program and its input, the program halts when run with that input; the essence of Turing's proof is that any such algorithm can be made to contradict itself, and therefore cannot be correct. For real-time programming, it's important that programmers attempt to write subroutines that are not only guaranteed to finish (halt), but are guaranteed to finish before the given deadline.

Joel says in essence, it is that we can't check for infinite loops before a program runs, because the check could itself become an infinite loop.

@FluffyJack recommends watching this video: https://www.youtube.com/watch?v=macM_MtS_w4

@BarisBalic, a software engineer in London, says it is: "a fallacy based on the assumption humans posses the skill/capacity necessary to keep a program running indefinitely."

##What is TDD?

TDD or Test-driven development is a software development process. 

It commences with the developer writing a test for the code, before the code is written. 

Initially, to ensure test calibration, just enough code should be written to fail the test. 

Then just enough code should be written to pass the test. Once this is done, then the  second test is developed. 

If the code and tests are written correctly the code should pass the first test but not the second. 

Then refactoring should occur. 

This process of writing the tests, writing the code, then refactoring is repeated. 

By focusing on writing only the code necessary to pass tests, designs can often be cleaner and clearer than is achieved by other methods.

**Joel says it's also worth mentioning the benefits of automated testing and the red green refactor cycle.**

##How can two databases be accessed from the same Rails application?

Connections are usually created through ActiveRecord::Base.establish_connection and retrieved by ActiveRecord::Base.connection.

All classes inheriting from ActiveRecord::Base will use this connection. 

But you can also set a class-specific connection. 

For example, if Course is an ActiveRecord::Base, but resides in a different database, you can just say Course.establish_connection and Course and all of its subclasses will use this connection instead.

**The steps:**

Additional databases can be created in the config/database.yml file. 

Let’s say we want to integrate the foo database, the additional connection might be:

```
foo:
  adapter: mysql2
  database: foo
  encoding: utf8
  username: root
  password: secret
```

The connection to this database then needs to be established in the associated models.

To access the foo database, we conventionally use models in the Foo namespace and use a proper connection.

```
class Foo::Bar < ActiveRecord::Base
  establish_connection 'foo'
end
```


##What is an IP address?

An IP address is an Internet Protocol address. 

It is used to identify all the websites on the internet. 

Each IP address is unique and it is separated by periods. 

For example :124.2.3.5 . It ranges from 0 to 255. 

Each and every website have an IP address. 

For example, an IP address for Google.com is 216.239.59.147 and that is how the internet identifies it.

Generally, ip address is very difficult to remember by the visitors. 

So, they type domain name (google.com/yahoo.com etc ) in the browser and it is converted to the destination address.

This conversion process is done by DNS ( Domain name system / Domain Name Server ). 

There are two types of ip addresses:

1. Private Ip address
2. Public Ip address

Private ip address is also known as internal ip of your computer. 

To get the ip address of a computer use the following steps: 

start->run->cmd-> ipconfig 

or

start->run->cmd->ipconfig/all It shows your internal ip address. 

Public or external ip address is used to access the internet.

##How might your prevent name conflicts in Javascript?

1. you can use objects and put everything inside that object, eg an app object like we do with Backbone, and then that is the only place you could have a possible conflict
2. inside the document.ready any variables you define will only exist inside the document.ready function, so you can prevent conflicts just by wrapping them in a document.ready 

##How would you model a coffee shop in Rails?

Coffee, Customer, Order, Employee, Owner

a coffee belongs_to :order

an order has_many :coffees

an order belongs_to :customer

a customer has_many :orders

an employee has_many :orders

an order belongs_to :employee

an employee belongs_to :owner

an owner has_many :employees

##Why is it better to serve site assets from multiple domains?

Serving assets from multiple domains can increase the number of assets a browser can download in parallel. This then would improve a website's response time.

even better when coupled with actual CDN technology that can help decrease latency by serving assets from a more suitable physical location.

To avoid overloading on one server, the browser has the limit on the number of resources loaded from a domain simultaneously. The number varies between browsers. So it's better to serve resources from multiple domains.

But there can be a downside to this - depending on bandwidth and CPU speed, too many parallel downloads can degrade performance.

#C team

##What is a framework?

Frameworks, such as Rails, Sinatra, Backbone, provide structure to the complex computer systems/computer languages. The user can add to the frameworks with their own code and customizations. Frameworks may include APIs, libraries, toolsets, compilers, support programs that enable development.

##How does MVC work?

Model-Views-Controller is the basic architectural pattern for software applications for implementing user interfaces. (talk about the router if you are going for a Rails job)
Model- directly manages the data, logic, and rules of the application
Views - requests info from the model and uses info to generate and output representation to the user
Controller - accepts the input and converts it to commands for the model or view; can send commands to the model to update the model’s state

##Why would you use Rails rather than another framework?

Rails allows the user to easily develop software because it is optimized for programmer happiness and sustainable productivity (aka ideal for building web applications). Rails is completely free and open-source and it even runs on Linux. Rails has a big community so it is easy to search websites like Stackoverflow for questions. It is scalable as many big companies have used it to develop their own software such as Twitter (which also means it allows for complexity).

The large rails community has also meant the continuous development of useful gems.

##What operators are available in Ruby?

Ruby operators:

arithmetic (+, -, , /, %, *)

comparison(==, >=, <=, >, <, etc.)

assignment (=, +=, -=, *=, etc.)

logical (&&, ||, and, or, etc. )

bitwise (a&b, etc. )

range (.., ...)

ternary (?:)

##What are the looping structures in Ruby?

Loops in Ruby are used to execute the same block of code a specified number of times, or each element in a collection.

for - while - until - begin  - each - select - any? - times - map - unless - loop do

##Compare validations, callbacks and observers in ActiveRecord

Validations are used to ensure that only valid data is saved into your database

Callbacks, which are sometimes referred to as ‘hooks’, are methods that are called at specific times in an object’s life cycle. For example, you can specify that certain code will run when an object is either created, saved, updated, deleted, loaded or validated from the database.

Whereas callbacks can pollute a model with code that isn’t directly related to its purpose, observers allow you to add the same functionality without changing the code of the model.

##What are helpers in Rails?

(this is more of a view helper) helpers in rails assist with assets, dates, forms, numbers and model objects. They are more like methods in that you call them on an object, which might help you to format time or to capitalize a person’s first name. You can either use the standard template helpers or you can create your own customized helpers 

##What are the associations available in ActiveRecord models?

belongs_to - one-to-one connection with another model

has_one - one-to-one connection with another model, but each instance of a model contains or possesses one instance of another model

has_many - one-to-many connection with another model. You'll often find this association on the "other side" of a belongs_to association
has_many :through - This association indicates that the declaring model can be matched with zero or more instances of another model by proceeding through a third model

has_one :through - This association indicates that the declaring model can be matched with one instance of another model by proceeding through a third model

has_and_belongs_to_many - creates a direct many-to-many connection with another model, with no intervening model

##What is the log to check for errors in Rails?

Rails maintains error logs for the application. There are separate logs for development, production and testing environments. The development and testing logs can be found in the log folder in the app root directory. The production log can only be accessed on the host once the application is deployed to production.

##What is ORM in Rails?

Using ORM, the properties and relationships of the objects in an application can be easily stored and retrieved from a database without writing SQL statements directly and with less overall database access code.
ORM is Object Relational Mapper. It means you don't have to manually call the database yourself; the ORM handles it for you. Ruby on Rails uses one called ActiveRecord
Active Record gives us several mechanisms, the most important being the ability to:

- Represent models and their data.
- Represent associations between these models.
- Represent inheritance hierarchies through related models.
- Validate models before they get persisted to the database.
- Perform database operations in an object-oriented fashion


##How does a URL work?

##What happens when you enter a URL into your browser?

##Name 3 ways to decrease page load.

#D Team

##Compare Ruby on Rails and PHP

Like comparing apples to oranges. PHP is a scripting language, Ruby on Rails is a web development framework based on the scripting language Ruby.

Why Rails over PHP? PHP projects do not have a mature, proven framework (there are lots to choose from), whereas Rail's framework utilises convention over configuration using automation (generators/scaffolding, gems/plugins, Active Record ORM, tests)

##What is a destructive method?

A destructive method is one which alters the state of an object. String, Array, and Hash, and others have such methods. Often there are two versions of a method, one with a plain name, the other with the same, but followed by !. The plain version takes a copy of the receiver, makes its change to it, and returns the copy. The version with the ! modifies the receiver in place.

Beware, however, that there are a fair number of destructive methods that don't have an !, including assignment operators (name=), array assignment ([]=), and methods such as Array.delete.

Destructive methods are dangerous as assignment in most cases just copies object references, and that parameter passing is equivalent to assignment. This means you can end up with multiple variables referencing the same object. If one of those variables is used to invoke a destructive method, the object referenced by all of them will be changed.

Can be faster and more efficient if you can afford to manipulate the original dataset, particularly if they are large data sets.

(reference: http://www.rootr.net/rubyfaq-7.html)

##Explain the different variable scopes in Ruby

Scope defines where in a program a variable is accessible. Ruby has four types of variable scope, local, global, instance and class. In addition, Ruby has one constant type. Each variable type is declared by using a special character at the start of the variable name as outlined in the following table.

Name Begins With Variable Scope

$ A global variable

@ An instance variable

[a-z] or _ A local variable

[A-Z] A constant

@@ A class variable

In addition, Ruby has two pseudo-variables which cannot be assigned values. These are nil which is assigned to uninitialized variables and self which refers to the currently executing object. In the remainder of this chapter we will look at each of these variable scopes in turn.

reference(http://www.techotopia.com/index.php/Ruby_Variable_Scope)

##What is the Ruby convention for naming methods?

Use snake_case for symbols, methods and variables.

Use CamelCase for classes and modules

Use SCREAMING_SNAKE_CASE for other constants.

Methods also have the convention of being suffixed with ? (which will return true or false) or ! (which will return a destructive method)

(reference: https://github.com/bbatsov/ruby-style-guide#naming)

##Compare instance and class variables

##Describe the concept of visibility in Rails

##What is meant by DRY?

##What is a garbage collector and how does it work?

automation of memory deallocation

How? Ruby uses bitmap marking

The GC module provides an interface to Ruby’s mark and sweep garbage collection mechanism

GC module in Ruby that you can set GC.disable => true || false

Why? dramatically reduce overall memory consumption by all Ruby processes running on a web server!

http://patshaughnessy.net/2012/3/23/why-you-should-be-excited-about-garbage-collection-in-ruby-2-0


##What is the role of a router in Rails?

Recognizes URLs and dispatches them to a controller's action.

It can also generate paths and URLs, avoiding the need to hardcode strings in your views.

Resource routing allows you to quickly declare all of the common routes for a given resourceful controller

Browsers request pages from Rails by making a request for a URL using a specific HTTP method, such as GET, POST, PATCH, PUT and DELETE. Each method is a request to perform an operation on the resource. A resource route maps a number of related requests to actions in a single controller.

##What is your favourite browser and why?

Chrome

Why? Dev tools, HTML5, Web Components, Automated Updating, UX

##How would you make a web page load faster?

##What is the difference between a SPAN and a DIV?

##If you could master one technology this year, what would it be?









