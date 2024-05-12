# Dating App Project Setup

## Introduction

In this training course, we will be using the .NET command-line interface (CLI) to create our project. While you can use Visual Studio or Ryder, I recommend using the command line for consistency and to familiarize yourself with the available options.

## Step 1: Set Up Project Folder

1. Open a terminal.
2. Navigate to the directory where you want to create your project.
3. Use the following command to create a new directory:
   ```
   mkdir DatingApp
   ```
4. Change into the `dating-app` directory:
   ```
   cd DatingApp
   ```

## Step 2: Check .NET SDK Version

1. Check the installed .NET SDK version by running:
   ```
   dotnet --info
   ```
   Note: In this case, the version is `7.0.100 RC 2`.

## Step 3: Create Solution and Project

1. Create a solution file:
   ```
   dotnet new sln
   ```
2. Create a Web API project:
   ```
   dotnet new webapi -n API
   ```
   if you using .Net 8.0 then use following command
   ```
   dotnet new webapi -n API --use-controllers
   ```

## Step 4: Add Project to Solution

1. Add the API project to the solution:
   ```
   dotnet sln add API
   ```

## Step 5: Open Project in Visual Studio Code

1. Open Visual Studio Code:
   ```
   code .
   ```
2. If you encounter an issue, follow these steps:
   - Open the command palette (Shift + Command + P on Mac).
   - Search for "path".
   - Choose "Shell Command: Install 'code' command in PATH".
   - If access is denied, uninstall and reinstall the command in PATH.
   - Once installed successfully, close and reopen Visual Studio Code.
3. Confirm trust for the project files when prompted.

## Conclusion

Now that your project is set up, you can begin developing your .NET Web API application.


# Project Overview

In this section, we'll take a closer look at the structure of our project and ensure that our application is running correctly. We'll also make some adjustments to the project settings.

## Viewing Project Structure

### Solution Explorer
1. Open Visual Studio Code.
2. Use the Solution Explorer view to navigate through the project.

### Terminal
3. Open the terminal (Ctrl + `).
4. Navigate to the API project:
    ```
    cd API
    ```

### Running the Application
5. Run the application:
    ```
    dotnet run
    ```

### Testing the Application
6. Open your browser and navigate to the URL provided in the terminal.

### Exploring Project Files
- **Properties**
    - `launchSettings.json`: Contains configuration settings for running the application.

- **App Settings**
    - `appsettings.json`: General configuration settings.
    - `appsettings.Development.json`: Development-specific configuration settings.

- **Program.cs**
    - Main entry point into the application.
    - Contains configuration for services and the HTTP request pipeline.

## Adjusting Project Settings

### `launchSettings.json`
- Remove unnecessary profiles.
- Set the application URL to `https://localhost:5001`.

### `Program.cs`
- Remove Swagger-related middleware.

## Conclusion
Now that we have explored our project structure and adjusted the necessary settings, our application is ready for further development. In the next section, we will create our first class and begin building our application.