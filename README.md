# CRUD
CRUD Application with ASP.NET Core and Entity Framework

This guide shows how to build a simple CRUD (Create, Read, Update, Delete) application using ASP.NET Core Web App and Entity Framework.

Step 1. Create the Project

Open Visual Studio 2022.

Click Create a new project.

Search for ASP.NET Core Web App.

Name your project and click Create.

<img width="1544" height="550" alt="image" src="https://github.com/user-attachments/assets/21e9a7b9-4e64-4c7e-8a08-4f43f942d3ab" />
Step 2. Create the Model

In Solution Explorer, right-click the project.

Add a new Folder and name it Models.

Right-click Models, select Add > Class, and name it Users.cs.

Add the following code:
```
public class Users
{
    public int ID { get; set; }
    public string Name { get; set; }
    public string Email { get; set; }
}
```

<img width="1497" height="644" alt="image" src="https://github.com/user-attachments/assets/084b329a-626a-4f34-ac2c-76958edf5956" />
Step 3. Create Razor Pages for CRUD

Right-click the Pages folder.

Add a New Folder and name it Users.

Right-click Users, select Add > New Scaffolded Item.

Choose Razor Pages using Entity Framework (CRUD) and click Add.

<img width="952" height="656" alt="image" src="https://github.com/user-attachments/assets/62a1335e-2974-4c0e-93e8-5081506fe198" />

Select Model Class as Users (CRUDApp.Models).

Under Data Context Class, click the + icon to create a new context.

Click Add and wait for NuGet packages to install.

Step 4. Run Database Migration

Go to Tools > NuGet Package Manager > Package Manager Console.

Run the following commands one by one:

Type first

```
add-migration Initial
```
Then type this
```
update-database
```


Wait until both complete successfully.

<img width="949" height="119" alt="image" src="https://github.com/user-attachments/assets/edae2837-43ae-4c96-9c3f-90e4a35abade" />
Step 5. Run the Application

Press F5 to build and run the project.

When the app starts, go to:

https://localhost:7017/users


You will see the Users page.

<img width="758" height="217" alt="image" src="https://github.com/user-attachments/assets/d10798ef-6a1d-492c-88eb-c6a6801e55f8" />
Step 6. Test the CRUD Features
Index / Dashboard

Displays all users.

<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/9d446f68-3a6b-498f-8465-2c146a51caf3" />
Create

Add a new user.

Edit

Modify an existing user.

<img width="1918" height="1031" alt="image" src="https://github.com/user-attachments/assets/80e9ed9a-b8d2-4cea-8f12-1ae0dfbde6c5" />
Details

View detailed information.

<img width="1919" height="1030" alt="image" src="https://github.com/user-attachments/assets/f4a0f50a-1aad-43a0-9133-b9c232dfa9e3" />
Delete

Remove a user record.

<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/4c224776-ca3f-4723-be02-e82689dedfed" />
Step 7. View the Database in Visual Studio

In the top search bar, type SQL.

Open SQL Server Object Explorer.

Navigate to:

(localdb)\MSSQLLocalDB
Databases
CRUDContext
Tables
dbo.Users


Right-click dbo.Users and select View Designer.

<img width="1919" height="667" alt="image" src="https://github.com/user-attachments/assets/0f796f05-7a00-489f-a60d-ba3151ef9b88" />
Done

You now have a working CRUD application that connects to a local SQL database and manages user data.
