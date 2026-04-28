# Creating a New .NET Project

This guide covers the steps to bootstrap a new backend service using .NET.

## Prerequisites

- .NET SDK installed
- Access to the internal NuGet feed (if applicable)

## Steps

1. Create a new solution: `dotnet new sln -n MyProject`
2. Add a Web API project: `dotnet new webapi -n MyProject.Api`
3. Add the project to the solution: `dotnet sln add MyProject.Api/MyProject.Api.csproj`
4. Configure `appsettings.json` with required settings.
5. Run locally: `dotnet run --project MyProject.Api`

_Additional configuration and standards to be documented._
