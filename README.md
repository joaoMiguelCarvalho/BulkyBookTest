BulkyBookWeb
BulkyBookWeb is a modern web application built using ASP.NET Core. The application aims to manage books for a virtual bookstore. It allows users to browse books, manage book inventory, and process orders. The system includes features for both customers and administrators, enabling them to interact with the platform.

Features
User Authentication & Authorization: Users can register and log in to the application.
CRUD Operations for Books: Administrators can create, read, update, and delete books in the inventory.
Shopping Cart: Users can add books to a shopping cart and proceed to checkout.
Order Management: Admin users can view and process orders placed by customers.
Search & Filtering: Users can search and filter books based on categories, authors, and prices.

Technologies Used
ASP.NET Core 5.0/6.0: The framework for building the web application.
Entity Framework Core: ORM for database management.
SQL Server: Database for storing user data, book inventory, and orders.
Bootstrap: Frontend framework for responsive design.
Razor Pages: For dynamic content rendering in the views.

Requirements
.NET SDK 6.0 or higher
SQL Server or an equivalent relational database
Visual Studio or Visual Studio Code for development

Installation

To get started with the BulkyBookWeb project on your local machine:
- Clone the repository:

Restore the dependencies:
- dotnet restore 
  
Configure the Database:
Create a database in SQL Server (or use any compatible database).
Update the appsettings.json file to include the connection string for your database:

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=BulkyBookDb;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}


Apply Migrations:
To create the necessary tables and schema in your database, run the following commands:

dotnet ef migrations add InitialCreate
dotnet ef database update


Run the Application:
After setting up your database, you can run the application:
dotnet run

The application will start on http://localhost:5000.


Folder Structure
Here is an overview of the folder structure in this project:


BulkyBookWeb/
├── Controllers/        # Controllers for handling HTTP requests
├── Data/               # Entity Framework data models and DB context
├── Models/             # Model classes for various entities (Book, User, Order)
├── Views/              # Razor views (UI)
├── wwwroot/            # Static files (CSS, JS, Images)
├── appsettings.json    # Configuration file
├── Program.cs          # Entry point for the application
├── Startup.cs          # Configuration for services and middleware

Usage
User Registration & Login: Users can register an account and log in to access personal features such as the shopping cart and order management.
Add and Manage Books: Admin users can add, edit, and remove books from the inventory through an easy-to-use interface.
Shopping Cart: Users can add books to their cart and proceed to checkout for purchase.
Order History: Users can view past orders and track the status of their current orders.
Contributing
We welcome contributions to improve this project. Please feel free to fork the repository and submit a pull request with your proposed changes. Here are a few ways you can contribute:

Report issues or bugs.
Improve documentation.
Add new features or improve existing ones.

Acknowledgments
Special thanks to the ASP.NET Core team for providing such an excellent framework.
Thanks to Bootstrap for making it easy to build responsive web applications.