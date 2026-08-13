# StockForge — Hardware Inventory Management System

StockForge is a **Hardware Inventory Management System** designed to help hardware businesses manage products, categories, suppliers, customers, purchases, sales/orders, inventory, maintenance, notifications, reports, and users from a centralized web application.

This repository contains the **StockForge .NET Web Application**. It is the web-based administrative and business-management system and is designed according to the finalized StockForge web UI/UX specification.

> **Important:** This repository is for the **.NET web application only**. It does not contain Flutter/Dart application architecture or Flutter-specific implementation details.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Project Goals](#project-goals)
- [Technology Stack](#technology-stack)
- [Core Modules](#core-modules)
- [Final Web Screen Scope](#final-web-screen-scope)
- [User Roles](#user-roles)
- [Application Workflow](#application-workflow)
- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Database Design](#database-design)
- [API Structure](#api-structure)
- [Authentication and Authorization](#authentication-and-authorization)
- [Inventory Rules](#inventory-rules)
- [Validation](#validation)
- [Audit Logging](#audit-logging)
- [UI/UX Guidelines](#uiux-guidelines)
- [Figma Design Structure](#figma-design-structure)
- [Responsive Design](#responsive-design)
- [Security](#security)
- [Performance](#performance)
- [Development Workflow](#development-workflow)
- [Implementation Priority](#implementation-priority)
- [Testing](#testing)
- [Future Scalability](#future-scalability)

---

# Project Overview

**StockForge** is a web-based Hardware Inventory Management System.

The system provides a centralized platform for managing the complete hardware business workflow:

```text
Products
   ↓
Categories
   ↓
Suppliers
   ↓
Purchases
   ↓
Inventory
   ↓
Customers
   ↓
Sales / Orders
   ↓
Maintenance
   ↓
Reports
```

The system also provides:

- User management
- Role-based access control
- Notifications
- Audit logging
- Dashboard analytics
- Search and filtering
- Reporting and exports

The web application is intended for authorized business users who need to manage operational data through a professional and responsive interface.

---

# Team Members

StockForge is developed as a team project by the following members:

| # | Name | Enrollment No. | Role | GitHub |
|---:|---|---|---|---|
| 1 | **Khush Dobariya** | `24SOECE11007` | **Team Leader** | [github.com/khushop03](https://github.com/khushop03) |
| 2 | **Rajvi Lunagariya** | `24SOECE11019` | **Backend Developer** | [github.com/RJV-44](https://github.com/RJV-44) |
| 3 | **Abhay Vekariya** | `24SOECE11049` | **Frontend Developer** | [github.com/avekariya779-del](https://github.com/avekariya779-del) |

## Team Responsibilities

### Khush Dobariya — Team Leader

- Project planning and coordination
- Overall system architecture coordination
- .NET web application integration
- Module planning and development coordination
- UI/UX and Figma coordination
- GitHub repository and team workflow management

### Rajvi Lunagariya — Backend Developer

- ASP.NET Core backend development
- REST API development
- Business logic
- Database integration
- Authentication and authorization
- Backend validation and services

### Abhay Vekariya — Frontend Developer

- Web UI implementation
- ASP.NET Core views/frontend development
- Responsive design implementation
- Reusable UI components
- Form and client-side validation
- Frontend integration with backend APIs

---

# Project Goals

StockForge aims to:

1. Centralize hardware inventory information.
2. Reduce manual inventory management.
3. Manage products and categories efficiently.
4. Manage suppliers and customers.
5. Manage purchase orders.
6. Manage sales/orders.
7. Track stock movements.
8. Identify low-stock and out-of-stock products.
9. Track maintenance/service records.
10. Provide business reports and analytics.
11. Control access using roles and permissions.
12. Maintain an auditable history of important business actions.
13. Provide a scalable foundation for future features.

---

# Technology Stack

## Frontend / Web UI

- ASP.NET Core web application
- Razor Views or MVC-based UI
- HTML5
- CSS3
- JavaScript
- Responsive UI components

## Backend

- ASP.NET Core
- C#
- RESTful Web API
- Application services
- Business logic
- Validation
- Authentication and authorization

## Database

Recommended:

- Microsoft SQL Server
- Entity Framework Core
- Entity Framework Core Migrations

## Development Tools

- Visual Studio or Visual Studio Code
- .NET SDK
- SQL Server / SQL Server Express / LocalDB
- Git
- GitHub

---

# Core Modules

The StockForge web application contains the following modules:

1. Authentication
2. Dashboard
3. Products
4. Categories
5. Suppliers
6. Customers
7. Purchases
8. Sales / Orders
9. Inventory
10. Maintenance
11. Notifications
12. Reports & Analytics
13. Users & Roles
14. Settings as an application/admin section rather than a separate primary screen

---

# Final Web Screen Scope

The final Figma planning scope contains **31 primary screens**.

| # | Screen | Module |
|---:|---|---|
| 1 | Login | Authentication |
| 2 | Forgot Password | Authentication |
| 3 | Dashboard | Dashboard |
| 4 | Product List | Products |
| 5 | Add Product | Products |
| 6 | Product Details | Products |
| 7 | Edit Product | Products |
| 8 | Category List | Categories |
| 9 | Add/Edit Category | Categories |
| 10 | Supplier List | Suppliers |
| 11 | Add Supplier | Suppliers |
| 12 | Supplier Details | Suppliers |
| 13 | Edit Supplier | Suppliers |
| 14 | Customer List | Customers |
| 15 | Add Customer | Customers |
| 16 | Customer Details | Customers |
| 17 | Edit Customer | Customers |
| 18 | Purchase Order List | Purchases |
| 19 | Create Purchase Order | Purchases |
| 20 | Purchase Order Details | Purchases |
| 21 | Edit Purchase Order | Purchases |
| 22 | Sales Order List | Sales |
| 23 | Create Sales Order | Sales |
| 24 | Sales Order Details | Sales |
| 25 | Inventory Overview | Inventory |
| 26 | Stock Movement History | Inventory |
| 27 | Maintenance List | Maintenance |
| 28 | Maintenance Details | Maintenance |
| 29 | Notifications | Notifications |
| 30 | Reports & Analytics | Reports |
| 31 | Users & Roles | Administration |

### Not counted as separate primary screens

The following are reusable components or states:

- Delete confirmation
- Deactivate confirmation
- Activate confirmation
- Unsaved changes confirmation
- Stock adjustment dialog
- Approval dialog
- Receive purchase dialog
- Success toast
- Error toast
- Loading state
- Empty state
- Permission denied state
- Search/no-results state

---

# User Roles

StockForge uses role-based and permission-based access.

## Administrator

Full system access.

Can manage:

- Users
- Roles
- Permissions
- Products
- Categories
- Suppliers
- Customers
- Purchases
- Sales
- Inventory
- Maintenance
- Reports
- System administration

## Inventory Manager

Primarily manages:

- Products
- Categories
- Inventory
- Stock movements
- Inventory reports

## Purchase Manager

Primarily manages:

- Suppliers
- Purchase orders
- Purchase approvals
- Purchase receipts
- Purchase reports

## Sales Manager

Primarily manages:

- Customers
- Sales/orders
- Sales processing
- Sales reports

## Maintenance Staff

Primarily manages:

- Maintenance records
- Assigned maintenance tasks
- Maintenance status
- Maintenance notes

## Viewer

Read-only access to permitted modules.

---

# Application Workflow

The standard application workflow is:

```text
Login
  ↓
Authentication
  ↓
Authorization
  ↓
Dashboard
  ↓
Select Module
  ↓
List / Search / Filter
  ↓
View / Create / Edit
  ↓
Client Validation
  ↓
API Request
  ↓
Backend Authorization
  ↓
Business Validation
  ↓
Database Operation
  ↓
Audit Log
  ↓
Notification if Required
  ↓
Response
  ↓
Updated UI
```

---

# Main Business Workflows

## Product Workflow

```text
Create Category
      ↓
Create Product
      ↓
Set Product Information
      ↓
Set Pricing
      ↓
Set Minimum Stock
      ↓
Product Available
```

## Purchase Workflow

```text
Supplier
   ↓
Create Purchase Order
   ↓
Submit
   ↓
Approve
   ↓
Order
   ↓
Receive
   ↓
Increase Stock
   ↓
Create Stock Movement
   ↓
Complete
```

## Sales Workflow

```text
Customer
   ↓
Create Sales Order
   ↓
Confirm
   ↓
Process
   ↓
Complete
   ↓
Decrease Stock
   ↓
Create Stock Movement
```

## Maintenance Workflow

```text
Product
   ↓
Create Maintenance Record
   ↓
Assign Staff
   ↓
In Progress
   ↓
Complete
   ↓
Record Cost / Notes
```

---

# Architecture

StockForge should use a layered .NET architecture.

Recommended layers:

```text
Presentation
     ↓
Application
     ↓
Domain
     ↓
Infrastructure
     ↓
Database
```

## Presentation Layer

Responsible for:

- Web pages
- Controllers
- Views
- ViewModels
- Request handling
- User-facing validation messages

## Application Layer

Responsible for:

- Use cases
- Business workflows
- DTOs
- Services
- Interfaces
- Validators

## Domain Layer

Responsible for:

- Entities
- Business concepts
- Enums
- Domain rules
- Domain interfaces

## Infrastructure Layer

Responsible for:

- Entity Framework Core
- Database access
- Repositories
- Authentication infrastructure
- External services
- Migrations

---

# Project Structure

Recommended .NET solution structure:

```text
StockForge/
│
├── StockForge.sln
│
├── StockForge.Web/
│   ├── Controllers/
│   │   ├── AuthController.cs
│   │   ├── DashboardController.cs
│   │   ├── ProductsController.cs
│   │   ├── CategoriesController.cs
│   │   ├── SuppliersController.cs
│   │   ├── CustomersController.cs
│   │   ├── PurchaseOrdersController.cs
│   │   ├── SalesOrdersController.cs
│   │   ├── InventoryController.cs
│   │   ├── MaintenanceController.cs
│   │   ├── NotificationsController.cs
│   │   ├── ReportsController.cs
│   │   └── UsersController.cs
│   │
│   ├── Views/
│   │   ├── Shared/
│   │   ├── Auth/
│   │   ├── Dashboard/
│   │   ├── Products/
│   │   ├── Categories/
│   │   ├── Suppliers/
│   │   ├── Customers/
│   │   ├── PurchaseOrders/
│   │   ├── SalesOrders/
│   │   ├── Inventory/
│   │   ├── Maintenance/
│   │   ├── Notifications/
│   │   ├── Reports/
│   │   └── Users/
│   │
│   ├── ViewModels/
│   ├── wwwroot/
│   │   ├── css/
│   │   ├── js/
│   │   ├── images/
│   │   └── lib/
│   │
│   ├── Program.cs
│   └── appsettings.json
│
├── StockForge.Api/
│   ├── Controllers/
│   ├── Middleware/
│   ├── Filters/
│   ├── Extensions/
│   └── Program.cs
│
├── StockForge.Application/
│   ├── Features/
│   │   ├── Authentication/
│   │   ├── Products/
│   │   ├── Categories/
│   │   ├── Suppliers/
│   │   ├── Customers/
│   │   ├── Purchases/
│   │   ├── Sales/
│   │   ├── Inventory/
│   │   ├── Maintenance/
│   │   ├── Notifications/
│   │   ├── Reports/
│   │   └── Users/
│   │
│   ├── DTOs/
│   ├── Interfaces/
│   ├── Services/
│   └── Validators/
│
├── StockForge.Domain/
│   ├── Entities/
│   ├── Enums/
│   ├── ValueObjects/
│   ├── Interfaces/
│   └── Exceptions/
│
├── StockForge.Infrastructure/
│   ├── Data/
│   │   ├── StockForgeDbContext.cs
│   │   └── Configurations/
│   │
│   ├── Repositories/
│   ├── Services/
│   ├── Identity/
│   └── Migrations/
│
└── StockForge.Tests/
    ├── Unit/
    └── Integration/
```

If the project is implemented as a single ASP.NET Core project for a semester project, maintain the same conceptual separation through folders, services, interfaces, and feature areas.

---

# Database Design

The main database entities are:

```text
Users
Roles
Permissions
RolePermissions

Categories
Products

Suppliers
Customers

PurchaseOrders
PurchaseOrderItems

SalesOrders
SalesOrderItems

StockMovements

MaintenanceRecords

Notifications

AuditLogs
```

## Main Relationships

```text
Role
 └── Users

Category
 └── Products

Supplier
 └── PurchaseOrders
       └── PurchaseOrderItems
             └── Products

Customer
 └── SalesOrders
       └── SalesOrderItems
             └── Products

Product
 ├── StockMovements
 └── MaintenanceRecords

User
 ├── Notifications
 └── AuditLogs
```

---

# Important Database Fields

## Products

```text
ProductId
ProductCode
Name
Description
CategoryId
Unit
PurchasePrice
SellingPrice
MinimumStockLevel
CurrentStock
IsActive
CreatedAt
UpdatedAt
CreatedBy
UpdatedBy
```

## Categories

```text
CategoryId
Name
Description
IsActive
CreatedAt
UpdatedAt
```

## Suppliers

```text
SupplierId
SupplierCode
CompanyName
ContactPerson
Email
Phone
Address
City
State
PostalCode
TaxNumber
Notes
IsActive
CreatedAt
UpdatedAt
```

## Customers

```text
CustomerId
CustomerCode
Name
CompanyName
Email
Phone
Address
City
State
PostalCode
TaxNumber
Notes
IsActive
CreatedAt
UpdatedAt
```

## Purchase Orders

```text
PurchaseOrderId
PurchaseOrderNumber
SupplierId
OrderDate
ExpectedDate
Status
Subtotal
TaxAmount
DiscountAmount
TotalAmount
Notes
CreatedBy
CreatedAt
UpdatedAt
```

## Purchase Order Items

```text
PurchaseOrderItemId
PurchaseOrderId
ProductId
Quantity
UnitPrice
Discount
Tax
LineTotal
```

## Sales Orders

```text
SalesOrderId
SalesOrderNumber
CustomerId
OrderDate
Status
Subtotal
TaxAmount
DiscountAmount
TotalAmount
Notes
CreatedBy
CreatedAt
UpdatedAt
```

## Sales Order Items

```text
SalesOrderItemId
SalesOrderId
ProductId
Quantity
UnitPrice
Discount
Tax
LineTotal
```

## Stock Movements

```text
StockMovementId
ProductId
MovementType
Quantity
PreviousStock
NewStock
ReferenceType
ReferenceId
Reason
CreatedBy
CreatedAt
```

## Maintenance Records

```text
MaintenanceId
ProductId
ReferenceNumber
IssueDescription
MaintenanceType
Priority
Status
AssignedTo
StartDate
ExpectedCompletionDate
CompletionDate
Cost
Notes
CreatedBy
CreatedAt
UpdatedAt
```

## Notifications

```text
NotificationId
UserId
Type
Title
Message
ReferenceType
ReferenceId
IsRead
CreatedAt
ReadAt
```

## Audit Logs

```text
AuditLogId
UserId
Action
EntityType
EntityId
OldValue
NewValue
IpAddress
CreatedAt
```

---

# API Structure

The application should use RESTful ASP.NET Core APIs.

## Authentication

```http
POST /api/auth/login
POST /api/auth/logout
POST /api/auth/forgot-password
POST /api/auth/reset-password
GET  /api/auth/me
```

## Products

```http
GET    /api/products
GET    /api/products/{id}
POST   /api/products
PUT    /api/products/{id}
DELETE /api/products/{id}
```

## Categories

```http
GET    /api/categories
POST   /api/categories
PUT    /api/categories/{id}
DELETE /api/categories/{id}
```

## Suppliers

```http
GET    /api/suppliers
GET    /api/suppliers/{id}
POST   /api/suppliers
PUT    /api/suppliers/{id}
```

## Customers

```http
GET    /api/customers
GET    /api/customers/{id}
POST   /api/customers
PUT    /api/customers/{id}
```

## Purchase Orders

```http
GET  /api/purchase-orders
GET  /api/purchase-orders/{id}
POST /api/purchase-orders
PUT  /api/purchase-orders/{id}

POST /api/purchase-orders/{id}/approve
POST /api/purchase-orders/{id}/receive
POST /api/purchase-orders/{id}/cancel
```

## Sales Orders

```http
GET  /api/sales-orders
GET  /api/sales-orders/{id}
POST /api/sales-orders
PUT  /api/sales-orders/{id}

POST /api/sales-orders/{id}/complete
POST /api/sales-orders/{id}/cancel
```

## Inventory

```http
GET  /api/inventory
GET  /api/inventory/movements
POST /api/inventory/adjust
```

## Maintenance

```http
GET  /api/maintenance
GET  /api/maintenance/{id}
POST /api/maintenance
PUT  /api/maintenance/{id}
```

## Reports

```http
GET /api/reports/inventory
GET /api/reports/purchases
GET /api/reports/sales
GET /api/reports/maintenance
```

---

# Authentication and Authorization

Authentication establishes the user's identity.

Authorization determines what the authenticated user can do.

Recommended permissions include:

```text
product.view
product.create
product.update
product.delete

category.view
category.create
category.update

supplier.view
supplier.create
supplier.update

customer.view
customer.create
customer.update

purchase.view
purchase.create
purchase.update
purchase.approve
purchase.receive

sales.view
sales.create
sales.update
sales.complete

inventory.view
inventory.adjust
inventory.movement.view

maintenance.view
maintenance.create
maintenance.update

reports.view
reports.export

user.view
user.create
user.update
user.manage_roles
```

The frontend should hide actions the user cannot perform, but **backend authorization must always remain the final security boundary**.

---

# Inventory Rules

Inventory is one of the core modules of StockForge.

## Purchase Receipt

Stock increases when the purchase is actually received.

```text
Purchase Order Created
        ↓
Approved
        ↓
Ordered
        ↓
Received
        ↓
Stock Increased
        ↓
Stock Movement Created
```

Creating a purchase order alone should not increase stock.

## Sales Completion

Stock decreases when the sales order is fulfilled/completed according to the business transaction policy.

```text
Sales Order
    ↓
Confirmed
    ↓
Processed
    ↓
Completed
    ↓
Stock Decreased
    ↓
Stock Movement Created
```

## Manual Adjustment

Manual stock adjustment must:

- Require authorization.
- Validate quantity.
- Record the previous stock.
- Record the new stock.
- Require a reason.
- Create a stock movement.
- Create an audit record.

Stock-changing operations should never silently modify inventory without an auditable movement.

---

# Validation

Validation should happen at three levels.

## Client-Side Validation

Used for:

- Required fields
- Email format
- Number format
- Basic ranges
- Immediate user feedback

## Backend Validation

Used for:

- Business rules
- Authorization
- Duplicate detection
- Stock availability
- Status transitions
- Transaction validation

## Database Validation

Used for:

- Primary keys
- Foreign keys
- Unique constraints
- Required fields
- Data integrity

Client-side validation must never replace backend validation.

---

# Common Validation Rules

## Products

- Product code is required.
- Product code must be unique.
- Product name is required.
- Category is required.
- Prices cannot be negative.
- Minimum stock cannot be negative.
- Products referenced by transactions should not be physically deleted.
- Inactive products cannot be selected for new transactions.

## Categories

- Name is required.
- Name should be unique.
- Categories referenced by products should not be physically deleted.
- Inactive categories cannot be assigned to new products.

## Suppliers

- Company name is required.
- Supplier code must be unique.
- Email must be valid where provided.
- Phone must follow the accepted format.

## Customers

- Customer name is required.
- Customer code must be unique.
- Email must be valid where provided.
- Phone must follow the accepted format.

## Purchase Orders

- Supplier is required.
- At least one item is required.
- Product is required.
- Quantity must be greater than zero.
- Price cannot be negative.
- Only authorized users can approve.
- Stock changes only when goods are received.

## Sales Orders

- Customer is required.
- At least one item is required.
- Product must be active.
- Quantity must be greater than zero.
- Available-stock rules must be enforced.
- Completed orders cannot be edited.

## Maintenance

- Product is required.
- Issue description is required.
- Priority is required.
- Status transitions must be valid.
- Completion date is required when completed.
- Cost cannot be negative.

---

# Audit Logging

Important business operations should create audit records.

Audit logging should cover:

- User changes
- Role/permission changes
- Product changes
- Price changes
- Stock adjustments
- Purchase approvals
- Purchase receipts
- Sales completion
- Maintenance status changes

Audit logs should contain:

```text
Who
What
Which Entity
Previous Value
New Value
When
IP Address
```

---

# UI/UX Guidelines

The web application follows a professional light-theme business UI.

## Primary Color

```text
#4CAF7D
```

## Main Colors

```text
Background:       #FFFFFF
Surface:          #F7F9F8
Primary Text:     #1F2937
Secondary Text:   #6B7280
Border:           #E5E7EB
```

## Main Application Layout

```text
+---------------------------------------------------------------+
| Top Bar: Search | Notifications | User Menu                  |
+----------------------+----------------------------------------+
| Sidebar              | Main Content                           |
|                      |                                        |
| Dashboard            | Page Header                            |
| Products             | Breadcrumbs                            |
| Categories           | Filters / Actions                      |
| Suppliers            | Content                                |
| Customers            |                                        |
| Purchases            |                                        |
| Sales / Orders       |                                        |
| Inventory            |                                        |
| Maintenance          |                                        |
| Notifications        |                                        |
| Reports              |                                        |
| Users & Roles        |                                        |
| Settings             |                                        |
+----------------------+----------------------------------------+
```

---

# Standard List Page

All major list screens should follow a consistent pattern:

```text
Page Title
Breadcrumb

[Search] [Filters] [Export] [Primary Action]

---------------------------------------------------------
| Column | Column | Column | Status | Actions          |
---------------------------------------------------------
| Data   | Data   | Data   | Badge  | View/Edit/Delete |
---------------------------------------------------------

Pagination
```

Every list should support appropriate:

- Loading state
- Empty state
- Error state
- Search results
- No filtered results
- Pagination

---

# Standard Form Page

```text
Page Header
Breadcrumb

Section Card
    Field
    Field
    Field

Section Card
    Field
    Field

Action Bar
[Cancel] [Save]
```

Desktop forms can use two columns.

Smaller screens should switch to one column.

---

# Standard Details Page

```text
Page Header
Status Badge
[Edit] [Other Actions]

Summary Card

Information Sections

Related Records

Activity / History
```

Details pages should prioritize readable information and provide editing actions only where the user's permission and record status allow them.

---

# Figma Design Structure

The Figma project should be organized as:

```text
01 - Design System
02 - Components
03 - Authentication
04 - Dashboard
05 - Products
06 - Categories
07 - Suppliers
08 - Customers
09 - Purchases
10 - Sales
11 - Inventory
12 - Maintenance
13 - Notifications
14 - Reports
15 - Users & Roles
16 - Responsive States
17 - Prototype Flow
```

Recommended component naming:

```text
Button/Primary
Button/Secondary
Button/Danger

Input/Text
Input/Number
Input/Search
Input/Date

Table/Default
Table/Empty
Table/Loading

Badge/Success
Badge/Warning
Badge/Error
Badge/Neutral

Card/KPI
Card/Information

Modal/Confirmation
Modal/Delete

Navigation/Sidebar
Navigation/Topbar
```

---

# Responsive Design

StockForge is desktop-first but should remain usable on tablets and smaller screens.

## Desktop

- Persistent sidebar
- Two-column forms
- Full data tables
- Dashboard grid

## Tablet

- Collapsible sidebar
- Reduced table columns
- Responsive cards
- Flexible forms

## Small Screens

- Collapsed navigation
- Single-column forms
- Horizontal table scrolling where unavoidable
- Stacked action buttons
- Priority information displayed first

---

# Security

The .NET web application should implement:

- Secure authentication
- Password hashing
- Role/permission authorization
- HTTPS
- Input validation
- Anti-forgery protection where applicable
- Secure session/token handling
- SQL injection protection
- Audit logging
- Rate limiting for sensitive endpoints where appropriate

Internal exception details and stack traces must not be exposed to end users.

---

# Transaction Consistency

Purchase receipt, sales completion, and inventory adjustment operations may modify multiple database records.

These operations should use database transactions.

Example:

```text
Receive Purchase Order
        ↓
Validate Purchase Order
        ↓
Validate Items
        ↓
Update Product Stock
        ↓
Create Stock Movement Records
        ↓
Update Purchase Order Status
        ↓
Create Audit Log
        ↓
Commit Transaction
```

If a required operation fails, the transaction should roll back.

---

# Error Handling

Use a consistent backend error format.

Example:

```json
{
  "success": false,
  "message": "Unable to complete the operation.",
  "errors": [
    {
      "field": "quantity",
      "message": "Quantity must be greater than zero."
    }
  ]
}
```

The UI should convert backend errors into clear user-facing messages.

---

# Performance

For scalability:

- Use server-side pagination.
- Avoid loading large datasets unnecessarily.
- Add indexes to commonly searched fields.
- Avoid N+1 database queries.
- Use asynchronous .NET operations.
- Use DTOs instead of returning unnecessary entity data.
- Optimize dashboard queries.
- Lazy-load large datasets where appropriate.
- Cache suitable read-heavy data.

Recommended indexed fields include:

```text
Products.ProductCode
Products.Name
Products.CategoryId

Suppliers.SupplierCode
Suppliers.CompanyName

Customers.CustomerCode
Customers.Name

PurchaseOrders.PurchaseOrderNumber
PurchaseOrders.SupplierId
PurchaseOrders.Status
PurchaseOrders.OrderDate

SalesOrders.SalesOrderNumber
SalesOrders.CustomerId
SalesOrders.Status
SalesOrders.OrderDate

StockMovements.ProductId
StockMovements.CreatedAt

MaintenanceRecords.ProductId
MaintenanceRecords.Status
MaintenanceRecords.AssignedTo

Notifications.UserId
Notifications.IsRead
```

---

# Development Workflow

## 1. Clone the Repository

```bash
git clone <repository-url>
cd StockForge
```

## 2. Restore Dependencies

```bash
dotnet restore
```

## 3. Configure Database

Update the connection string in the appropriate configuration file.

Example:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=StockForgeDb;Trusted_Connection=True;TrustServerCertificate=True"
  }
}
```

Do not commit production credentials or secrets to source control.

## 4. Apply Migrations

```bash
dotnet ef database update
```

If Entity Framework tools are not installed:

```bash
dotnet tool install --global dotnet-ef
```

## 5. Build

```bash
dotnet build
```

## 6. Run

```bash
dotnet run
```

The actual development URL is determined by the project's `launchSettings.json` and ASP.NET Core configuration.

---

# Testing

The project should include:

## Unit Tests

Test:

- Business rules
- Validators
- Services
- Calculations
- Status transitions

## Integration Tests

Test:

- API endpoints
- Database operations
- Authentication
- Authorization
- Purchase workflows
- Sales workflows
- Inventory updates

## UI Tests

Test important user flows:

```text
Login
Product Creation
Purchase Order Creation
Purchase Receipt
Sales Order Creation
Sales Completion
Stock Adjustment
Maintenance Update
Report Generation
User Permission Enforcement
```

---

# Implementation Priority

Development should follow this order:

## Phase 1 — Foundation

```text
Authentication
Design System
Application Shell
Dashboard
```

## Phase 2 — Master Data

```text
Categories
Products
Suppliers
Customers
```

## Phase 3 — Procurement & Inventory

```text
Purchases
Inventory
Stock Movements
```

## Phase 4 — Sales

```text
Sales / Orders
```

## Phase 5 — Operations

```text
Maintenance
Notifications
```

## Phase 6 — Administration

```text
Reports
Users & Roles
```

## Phase 7 — Quality

```text
Security
Audit Logging
Validation
Performance
Testing
Responsive Design
```

---

# Future Scalability

The architecture should allow future additions without redesigning the core system.

Possible future modules include:

- Advanced reporting
- Barcode scanning
- Product suppliers mapping
- Purchase returns
- Sales returns
- Inventory transfers
- Warehouse management
- Multiple warehouses
- Advanced notifications
- Email notifications
- File/document attachments
- Advanced audit history
- Dashboard customization
- More granular permissions

These features are **not part of the current 31-screen final scope** unless explicitly added later.

---

# Design Reference

The complete UI/UX design specification should be treated as the primary reference when creating the Figma design and implementing the .NET web application.

The implementation should remain consistent with:

- The 31-screen final scope
- The defined modules
- The navigation structure
- The database entities
- The role/permission model
- The purchase workflow
- The sales workflow
- The inventory rules
- The maintenance workflow
- The reusable UI component system

---

# Project Scope Summary

```text
StockForge
│
├── Authentication
├── Dashboard
├── Products
├── Categories
├── Suppliers
├── Customers
├── Purchases
├── Sales / Orders
├── Inventory
├── Maintenance
├── Notifications
├── Reports & Analytics
└── Users & Roles
```

### Final UI Scope

**31 primary web screens**

### Main Architecture

**ASP.NET Core + C# + REST API + Entity Framework Core + SQL Server**

### Design Approach

**Responsive, professional, light-theme business web application**

### Security Approach

**Authentication + Role-Based Access Control + Permission-Based Authorization + Audit Logging**

### Data Approach

**Relational database with transactional inventory operations and traceable stock movements**

---

# Important Project Rule

StockForge should be developed **one module at a time**.

For each module, define and implement:

1. Purpose
2. Features
3. Users/Roles
4. Workflow
5. Inputs
6. Outputs
7. Database tables and fields
8. Validations
9. UI screens and navigation
10. APIs/backend logic
11. Security/permissions
12. Testing requirements

Do not move to the next module until the current module is finalized.

---

# Source and Scope Note

The original uploaded semester proposal describes a Flutter/Dart frontend and Dart/Serverpod backend. That proposal was reviewed as the source material for the project context, but this README intentionally defines the **StockForge .NET Web Application** separately, according to the finalized StockForge web-app design scope.

The web application specification is the authoritative design reference for this .NET repository.
