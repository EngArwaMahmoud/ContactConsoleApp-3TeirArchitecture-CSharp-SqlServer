# Contacts Management System (3-Tier Architecture)

## Project Overview
This project is a **C# Console Application** for managing Contacts and Countries using **SQL Server**, designed to demonstrate the **3-Tier Architecture** concept.  
The main goal is to separate the application into three layers, each with a specific responsibility, ensuring clean code organization and maintainability.

---

## Architecture

### 1. Presentation Layer
- The **Console interface** acts as the user interface.  
- Users can perform CRUD operations on **Contacts** and **Countries**.  
- Displays contact details such as Name, Email, Phone, Address, Country, and Image.  

### 2. Business Layer
- Contains classes such as `clsContact` and `clsCountry`.  
- Handles the **core business logic**, including adding, updating, deleting, and checking records.  
- Validates data and manages the interaction between the Presentation Layer and Data Access Layer.

### 3. Data Access Layer
- Interacts directly with the **SQL Server database** using `SqlConnection` and `SqlCommand`.  
- Executes database queries for inserting, updating, deleting, and retrieving data.  
- Keeps database operations separated from business logic, following the **Separation of Concerns** principle.

---

## Main Features
- CRUD operations for Contacts (Add, Update, Delete, List)  
- CRUD operations for Countries (Add, Update, Delete, List)  
- Validation to ensure records exist before updating or deleting  
- Management of user information including Name, Email, Phone, Address, Date of Birth, and Image  
- Organized, layered structure for better maintainability and learning purposes

---

## Requirements
- **Visual Studio 2022** 
- **.NET Framework**
- **SQL Server** for database storage  
- Database should include the following tables:  
  - `Contacts`: ContactID, FirstName, LastName, Email, Phone, Address, DateOfBirth, CountryID, ImagePath  
  - `Countries`: CountryID, CountryName, CountryCode, PhoneCode  

---

## How to Run
1. Open the project in Visual Studio.  
2. Configure `clsConnectionString.ConnectionString` with your local database connection.  
3. Run `Program.cs` in **Debug** or **Release** mode.  
4. Use the available test functions to perform CRUD operations on Contacts and Countries, or modify the `Main` method to run specific tests.

---

## Example Usage
```csharp
// Add a new contact
testAddNewContact();

// Update a contact
testUpdateContact(1);

// Delete a contact
testDeleteContact(1);

// List all contacts
ListContacts();

ContactsConsoleApp/
├─ PresentationLayer/   --> Program.cs
├─ BusinessLayer/       --> clsContact.cs, clsCountry.cs
├─ DataAccessLayer/     --> clsContactDataAccess.cs, clsCountryDataAccess.cs
├─ .gitignore
└─ README.md

This project is ideal for learning 3-Tier Architecture, database management, and C# console applications with structured and maintainable code.
