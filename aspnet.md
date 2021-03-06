https://medium.com/net-core/asp-net-core-mvc-web-application-project-structure-3ccaa244fa66
https://medium.com/net-core/building-a-web-application-using-asp-net-core-mvc-and-entity-framework-core-15ee6192b3f3
https://www.udemy.com/course/introduction-to-aspnet-core-x/
https://www.udemy.com/course/complete-aspnet-core-21-course/
https://www.udemy.com/course/introduction-to-aspnet-core-x/

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

- Pages -> create BookList folder -> inside create Razor Page - Index

inside BookList -> Index.cshtml.cs:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using BookListRazor.Model;
using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.RazorPages;
using Microsoft.EntityFrameworkCore;

namespace BookListRazor
{
    public class IndexModel : PageModel
    {
        private readonly ApplicationDbContext _db;

        public IndexModel(ApplicationDbContext db)
        {
            _db = db; // extracting application from db context to this page using Dependancy Injection
        }

        public IEnumerable<Book> Books{ get; set; }

        public async Task OnGet()
        {
            Books = await _db.Book.ToListAsync(); // going to database and retrieving all books using Entity
        }                                         // storing that in Books IEnumerable
    }                                             // -> now inside Pages -> Index.cshtml we have all books to display
}
```

### 7. Design Book Index Page

##### Inside _Layout kreiram route:

```html
   <a class="nav-link text-dark" asp-area="" asp-page="/BookList/Index">Book</a>
```
- sada kad pokrenem applikaciju i kliknem "Book" TAB, otvori novi URL:

https://localhost:44300/BookList


I onda pokaze:

- BookList -> Index.cshtml:

```html
@page
@model BookListRazor.IndexModel
@{
    ViewData["Title"] = "Index";
}

    <h1>Index Book</h1>
```

### 8. Design Book Index Page 2

##### Use Razor Syntax to display Books:

- BookList -> Index.cshtml:

```cs
@page
@model BookListRazor.IndexModel
@{
    ViewData["Title"] = "Index";
}

<h1>Index Book</h1>

<div>
    @if (Model.Books.Count() > 0)
    {
        @foreach (var item in Model.Books)
        {
            <p>Book name: @Html.DisplayFor(m=>item.Name)</p>
            <p>Book author: @Html.DisplayFor(m => item.Author)</p>
        }

    }
    else
    {
        <p>No Books Available</p>
    }
</div>
```

#### ADD BOOKS TO DATABASE TO DISPLAY:

SQL Server Management Studio

- right click on dbo.Book -> edit
- refresh page ---> BOOKS SHOW NOW

https://www.udemy.com/course/introduction-to-aspnet-core-x/learn/lecture/18078037#overview
