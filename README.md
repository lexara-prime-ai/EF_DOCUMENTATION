# Creating a Full Stack Application with .NET and Angular

```powershell
PS C:\API> dontnet new webapi
```
```powershell
PS C:\API> dotnet run
```
*Screenshot*

### Install dependencies :
**Install dotnet-ef**(*Command-Line Tool  for **Entity Framework***)
```powershell
PS C:\API> dotnet tool install --global dotnet-ef
```
```powershell
PS C:\API> dotnet add package Microsoft.EntityFrameworkCore
PS C:\API> dotnet add package Microsoft.EntityFrameworkCore.SqlServer
PS C:\API> dotnet add package Microsoft.EntityFrameworkCore.Tools
```
### STEPS
* Create a direcory, **Models** and a sub-directory, **Entities** as well as a new **Class**, **Post.cs(/Models/Entites/Post.cs)**

### Update the Post Class with the following content
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;

namespace API.Models.Entities
{
	public class Post
	{
		public Guid Id { get; set; }
		public string Title { get; set; }
		public string Content { get; set; }
		public string Summary { get; set; }
		public string UrlHandle { get; set; }
		public string FeaturedImageUrl { get; set; }
		public string Visible { get; set; }
		public string Author { get; set; }
		public DateTime PublishDate { get; set; }
		public DateTime ModifiedDate { get; set; }
	}
}
```
#### Create Migrations
