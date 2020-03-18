MVC invokes controller classes (and the action methods within them) depending on the incoming URL. The default URL routing logic used by MVC uses a format like this to determine what code to invoke:

[Controller]/[ActionName]/[Parameters]

___________________RAZOR App_________________________

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

