MVC invokes controller classes (and the action methods within them) depending on the incoming URL. The default URL routing logic used by MVC uses a format like this to determine what code to invoke:

[Controller]/[ActionName]/[Parameters]

# Razor Book App

### 1. Add Package to update page content on page refresh

- Tools -> NuGet -> compilationRunetime Razor
- inside startup.cs -> add AddRazorRuntimeCompilation()

```cs
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddRazorPages().AddRazorRuntimeCompilation();
        }
```

https://www.udemy.com/course/introduction-to-aspnet-core-x/learn/lecture/18078021#overview


### 2. Created model Book.cs

```cs
namespace BookListRazor.Model
{
    public class Book
    {
        [Key]
        public int Id { get; set; }

        [Required] // name cannot be null
        public string Name { get; set; }

        public string Author { get; set; }
    }
}
```
https://www.udemy.com/course/introduction-to-aspnet-core-x/learn/lecture/18078023#overview

### 3. Set up Database

- Tools -> NuGet -> Microsoft.EntityFrameworkCore

-> Entity framework to access database

- Tools -> NuGet -> Microsoft.EntityFrameworkCore.SqlServer

- Tools -> NuGet -> Microsoft.EntityFrameworkCore.Tools    

-> Tools for migrations

### 4. Open SQL Server Management Studio

- connect

- appsettings.json ( Visual Studio solution explorer)

```cs
// ADD:

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=USER;Database=BookListRazor;Trusted_Connection=True;MultipleActiveResultSets=True"
    },

    "Logging": {
      "LogLevel": {
        "Default": "Information",
        "Microsoft": "Warning",
        "Microsoft.Hosting.Lifetime": "Information"
      }
    },
    "AllowedHosts": "*"
  }
```

### 5. Add Book Table to Database

- add -> Model -> class -> ApplicationDbContext.cs

```cs
using Microsoft.EntityFrameworkCore;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;

namespace BookListRazor.Model
{
    public class ApplicationDbContext : DbContext
    {
        public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options) : base(options)
        {

        }

        public DbSet<Book> Book { get; set; }
    }
}
```

- Startup.cs:

```cs
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddDbContext<ApplicationDbContext>(option => option.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
        //    services.AddRazorPages().AddRazorRuntimeCompilation();
        }
        
// ctrl + .
// had to do to include ENTITY framework inside Configuration pipeline
// next we need to push to database
```

##### Pushing to Database:

- Tools -> NuGet -> Package Manager Console


##### Adding script:
```cs
// inside console:

PM> add-migration AddBookToDb


            migrationBuilder.CreateTable(
                name: "Book",
                columns: table => new
                {
                    Id = table.Column<int>(nullable: false)
                        .Annotation("SqlServer:Identity", "1, 1"),
                    Name = table.Column<string>(nullable: false),
                    Author = table.Column<string>(nullable: true)
                },
                constraints: table =>
                {
                    table.PrimaryKey("PK_Book", x => x.Id);
                });
```

##### Creating database and push migrations:
```cs
// inside console:

PM> update-database

```

##### In SQL Management Studio

- new Database has been created

```cs
SELECT TOP (1000) [Id]
      ,[Name]
      ,[Author]
  FROM [BookListRazor].[dbo].[Book]
```

### 6. Book Index get Handler
