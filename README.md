# Example-Starter-Kit-for-Umbraco-v9

This is the git repo for my YouTube videos on how to create a starter kit package for Umbraco v9

I actually published this package onto NuGet for a laugh.

Paste these commands to install it on windows, using local db

```ps
dotnet new -i Umbraco.Templates

# Create solution/project
dotnet new sln --name MySolution
dotnet new umbraco -n MyProject --friendly-name "Admin User" --email "admin@admin.com" --password "1234567890" --connection-string "Data Source=(localdb)\MSSQLLocalDB;AttachDbFilename=|DataDirectory|\Umbraco.mdf;Integrated Security=True"
dotnet sln add MyProject
dotnet add MyProject package MyStarterKit

# Run
dotnet run --project MyProject
#this should all work
```
