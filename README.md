📘 **Online Book Library System**

A simple web application to manage a library of books, built using ASP.NET Core MVC and Entity Framework Core. 
The app supports full CRUD functionality and is deployed on Azure App Service with an Azure SQL Database backend.

🚀 **Features**

- Add a new book

- View list of all books

- Edit book details

- View book details

- Delete a book

- Available online via Azure deployment

🛠️ **Technologies Used**

- ASP.NET Core MVC

- Entity Framework Core

- SQL Server / Azure SQL

- Razor Views + Bootstrap

- Visual Studio

- Azure App Service

- Git for version control

🛠️ **Technologies Used
ASP.NET Core MVC**

Entity Framework Core

SQL Server / Azure SQL

Razor Views + Bootstrap

Visual Studio

Azure App Service

Git for version control

🗃️ **Database Schema**

Book Table

| Field Name    | Type     |
| ------------- | -------- |
| Id            | int (PK) |
| Title         | string   |
| Author        | string   |
| Genre         | string   |
| PublishedYear | int      |
| IsAvailable   | bool     |

🏗️ **Project Structure**

```
OnlineBookLibrary/
├── Controllers/
│   └── BooksController.cs
├── Models/
│   └── Book.cs
├── Views/
│   └── Books/
│       ├── Index.cshtml
│       ├── Create.cshtml
│       ├── Edit.cshtml
│       ├── Details.cshtml
│       └── Delete.cshtml
├── Data/
│   └── ApplicationDbContext.cs
├── appsettings.json
└── Startup.cs / Program.cs
```

## ⚙️ How to Run the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/your-username/OnlineBookLibrary.git
```

### 2. Open the solution

Open the solution in **Visual Studio**.

### 3. Configure the database

Update the `appsettings.json` file with your **local SQL Server** connection string.

### 4. Apply database migrations

```powershell
Update-Database
```

### 5. Run the application

Press `Ctrl + F5` or click **Start Without Debugging** in Visual Studio.


## ☁️ Azure Deployment Instructions

### 1. Create Azure Resources
- Create an **Azure SQL Database** and an **App Service** in the Azure portal.

### 2. Update `appsettings.json` with your connection string

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=tcp:<your-server>.database.windows.net,1433;Initial Catalog=OnlineBookLibraryDB;Persist Security Info=False;User ID=<your-username>;Password=<your-password>;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;"
}
```

### 3. Publish from Visual Studio
- Right-click the project in **Solution Explorer**  
- Select: **Publish → Azure → App Service**  
- Choose an existing App Service or create a new one  
- Click **Publish**

### 4. Apply database migrations

Open **Package Manager Console** and run:

```powershell
Update-Database
```

### 5. Test the application

Visit your live App Service URL in the browser to confirm the deployment was successful.
