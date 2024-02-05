# Restaurant
_by Gabriel Tucker_

## Description
create an MVC web application to help her manage her employees (stylists) and their clients. Claire should be able to add a list of stylists working at the salon, and for each stylist, add clients who see that stylist. The stylists have specific specialties, so each client can only see (belong to) a single stylist.

### Technologies Used

* C#
* MSTest
* .Net
* Git
* NuGet package with dotnet CLI
* Sql

## Setup

1. Navigate to [github repository](https://github.com/Gabe9T/HairSalon.Solution) for this project 

2. Click the `Fork` button and  you will be taken to a new page where you can give your repository a new name and description. Choose "create fork".

3. Click the `Code` button and copy the url for HTTPS.

4. On your local computer, create a working directory for my files and name appropriately.

5. On your terminal, type `$ git clone https://github.com/Gabe9T/HairSalon.Solution.git`

6. In the terminal, type `$ dotnet run` (to compile and execute the console application ).

7. Enjoy!  You can close the development server at anytime by entering `ctrl` + `c` in the terminal.

# Setting up the SQL Database

This project uses a SQL database to store and manage data. Follow the instructions below to set up the database environment.

## Prerequisites

Install SQL Workbench if you haven't already. You can download it from the [official website](https://www.mysql.com/products/workbench/).

## Steps to Set Up the Database

### 1. Connect to MySQL Server

- Open SQL Workbench.
- Click on the "+" icon in the "MySQL Connections" tab to create a new connection.
- Enter the connection details such as hostname, port, username, and password to connect to your MySQL Server instance.

### 2. Create a New Database

- Once connected, click on the "SQL Editor" tab.
- Execute the following SQL command to create a new database:

    ```sql
    CREATE DATABASE YourDatabaseName;
    ```

### 3. Create Tables
- Use [SQL file](#gabriel_tucker)
- Navigate to the project directory and locate the SQL script for creating tables (`gabriel_tucker.sql`).
- Open the script in SQL Workbench.
- Execute the script to create necessary tables in your database.

### 4. Configure Connection String

- In the root of the HairSalon directory, create the `appsettings.json` file.
- Update the connection string with the appropriate details:

    ```json
    {
      "ConnectionStrings": {
        "DefaultConnection": "Server=YourServerName;Database=gabriel_tucker;User Id=YourUsername;Password=YourPassword;"
      }
    }
    ```

    Replace YourServerName, YourDatabaseName, YourUsername, and YourPassword with your actual MySQL Server instance details.

### 5. Testing Connection

- Build and run the project.
- Ensure that your application can connect to the database without any errors.
