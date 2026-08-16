# StockForge — .NET Web App UI/UX Design Specification

## 1. Document Purpose

This document is the **final UI/UX design specification** for the StockForge Hardware Inventory Management System web application.

It defines what needs to be designed in **Figma** and provides a consistent reference for implementing the web interface.

This document focuses on **UI/UX design only**.

It does not define:

- Database architecture
- API implementation
- C# backend architecture
- Entity Framework implementation
- Server configuration
- Repository architecture
- Backend transaction logic

---

# 2. Project Overview

**StockForge** is a Hardware Inventory Management System designed to help hardware businesses manage products, categories, suppliers, customers, purchases, sales/orders, inventory, maintenance, notifications, reports, and users.

The web application provides a centralized business-management interface for authorized users.

The web design should make business operations:

- Simple
- Fast
- Clear
- Consistent
- Professional
- Easy to understand
- Easy to scale

---

# 3. Design Scope

The final web application design contains **32 primary screens**, including a public-facing Landing Page.

These 32 screens are the approved scope for the Figma design.

Additional dialogs, popups, drawers, loading states, empty states, and confirmation states are considered **UI components/states**, not separate primary screens.

---

# 4. Team Members

| # | Name | Enrollment No. | Role | GitHub |
|---:|---|---|---|---|
| 1 | **Khush Dobariya** | `24SOECE11007` | **Team Leader** | https://github.com/khushop03 |
| 2 | **Rajvi Lunagariya** | `24SOECE11019` | **Backend Developer** | https://github.com/RJV-44 |
| 3 | **Abhay Vekariya** | `24SOECE11049` | **Frontend Developer** | https://github.com/avekariya779-del |

---

# 5. Design Goals

The StockForge web interface should follow these principles:

1. **Clarity** — users should immediately understand what each page does.
2. **Consistency** — similar actions and components should look and behave the same.
3. **Efficiency** — frequent business operations should require minimal unnecessary steps.
4. **Hierarchy** — important information should receive stronger visual emphasis.
5. **Scalability** — the design system should work as the application grows.
6. **Responsiveness** — the interface should remain usable on desktop, tablet, and smaller screens.
7. **Accessibility** — text, controls, status indicators, and navigation should be easy to use.
8. **Business Focus** — tables, forms, statuses, stock information, and actions should be prioritized.

---

# 6. Target Users

The UI should support the following user roles.

## Administrator

Full access to the application's available modules.

## Inventory Manager

Mainly works with:

- Products
- Categories
- Inventory
- Stock information

## Purchase Manager

Mainly works with:

- Suppliers
- Purchase orders
- Purchase order status

## Sales Manager

Mainly works with:

- Customers
- Sales/orders
- Order status

## Maintenance Staff

Mainly works with:

- Maintenance records
- Assigned maintenance work
- Maintenance status

## Viewer

Primarily views information without performing management actions.

### UI Rule

Users should only see navigation items and actions relevant to their permissions.

---

# 7. Overall Application Layout

After login, the application should use a consistent layout.

```text
+----------------------------------------------------------------+
| StockForge | Search                         | Notifications | User |
+----------------------+-----------------------------------------+
|                      |                                         |
| Sidebar              | Page Header                             |
|                      | Breadcrumb                              |
| Dashboard            |                                         |
| Products             | Main Content                            |
| Categories           |                                         |
| Suppliers            |                                         |
| Customers            |                                         |
| Purchases            |                                         |
| Sales / Orders       |                                         |
| Inventory            |                                         |
| Maintenance          |                                         |
| Notifications        |                                         |
| Reports              |                                         |
| Users & Roles        |                                         |
+----------------------+-----------------------------------------+
```

---

# 8. Navigation

## Primary Sidebar

The sidebar should contain:

1. Dashboard
2. Products
3. Categories
4. Suppliers
5. Customers
6. Purchases
7. Sales / Orders
8. Inventory
9. Maintenance
10. Notifications
11. Reports
12. Users & Roles
13. Settings/Profile area

## Sidebar Behavior

The sidebar should support:

- Active menu state
- Hover state
- Collapsed state
- Expanded state
- Icons
- Permission-based visibility
- Tooltips when collapsed

The active module should always be visually identifiable.

---

# 9. Top Bar

The top bar should contain:

- Global search
- Notifications
- User profile
- User name
- User role
- Profile/settings access
- Logout

The top bar should remain visually consistent across all authenticated screens.

---

# 10. Breadcrumbs

Inner pages should use breadcrumbs.

Example:

```text
Dashboard / Products
Dashboard / Products / Product Details
Dashboard / Purchases / Purchase Order Details
```

Breadcrumbs should help users understand where they are and return to the previous hierarchy level.

---

# 11. Visual Design System

## 11.1 Theme

Use a **light, clean, modern, professional business theme**.

Avoid overly decorative UI.

The interface should prioritize readability and operational efficiency.

---

## 11.2 Color Palette

### Primary

```text
#4CAF7D
```

Use for:

- Primary buttons
- Active navigation
- Selected controls
- Main actions
- Important positive states

### Background

```text
#FFFFFF
```

### Secondary Surface

```text
#F7F9F8
```

### Primary Text

```text
#1F2937
```

### Secondary Text

```text
#6B7280
```

### Border

```text
#E5E7EB
```

### Status Colors

Use consistent semantic colors:

- Success → Green
- Warning → Amber/Orange
- Error → Red
- Information → Blue
- Neutral → Gray

Status must not depend on color alone. Use text labels and/or icons where appropriate.

---

# 12. Typography

Use a clean modern sans-serif typeface.

Recommended hierarchy:

```text
Page Title
Section Title
Card Title
Body Text
Secondary Text
Caption
```

Typography should provide clear visual hierarchy without excessive font sizes.

---

# 13. Spacing

Use a consistent spacing system throughout the application.

Recommended base spacing:

```text
4px
8px
12px
16px
24px
32px
40px
48px
```

Do not use arbitrary spacing from screen to screen.

---

# 14. Border Radius

Use a consistent rounded style.

Recommended:

```text
Small controls: 6px
Inputs/buttons: 8px
Cards: 12px
Large containers: 12–16px
```

Avoid excessive rounding that makes the application look playful rather than professional.

---

# 15. Shadows

Use subtle shadows only when necessary.

Recommended usage:

- Cards
- Dropdowns
- Modals
- Floating elements

Most content containers should primarily use borders and surface contrast rather than heavy shadows.

---

# 16. Primary UI Components

The Figma design system should contain reusable components.

## Buttons

- Primary
- Secondary
- Outline
- Danger
- Icon button
- Disabled
- Loading

## Inputs

- Text input
- Number input
- Search input
- Date input
- Select
- Multi-select
- Text area
- Toggle

## Data Components

- Table
- Pagination
- Filter bar
- Search bar
- Sort control
- Tabs
- Status badge

## Feedback Components

- Toast
- Alert
- Confirmation modal
- Delete modal
- Error message
- Empty state
- Loading state

## Business Components

- KPI card
- Product selector
- Customer selector
- Supplier selector
- Order item row
- Price summary
- Stock indicator
- Activity/history item

---

# 17. Button Rules

## Primary Button

Used for the main action:

```text
Create
Save
Submit
Approve
Complete
```

## Secondary Button

Used for supporting actions:

```text
Cancel
Back
Close
```

## Danger Button

Used for destructive actions:

```text
Delete
Deactivate
Cancel Order
```

Primary actions should be visually stronger than secondary actions.

---

# 18. Form Design

All forms should use a consistent structure.

```text
Page Header
Breadcrumb

+---------------------------------------+
| Section Title                         |
|                                       |
| Field                 Field           |
|                                       |
| Field                 Field           |
+---------------------------------------+

+---------------------------------------+
| Section Title                         |
|                                       |
| Field                                 |
|                                       |
| Description                           |
+---------------------------------------+

[Cancel] [Save]
```

## Form Rules

- Labels should be clear.
- Required fields should be identifiable.
- Related fields should be grouped.
- Validation messages should appear near the relevant field.
- Primary action should be easy to find.
- Long forms should be divided into logical sections.
- Desktop forms may use two columns.
- Smaller screens should use one column.

---

# 19. Data Table Design

Tables are a major part of StockForge because the system manages business records.

Standard table structure:

```text
Search        Filters        Export       Add/Create

------------------------------------------------------------
| Column | Column | Column | Status | Actions              |
------------------------------------------------------------
| Data   | Data   | Data   | Badge  | View Edit More       |
| Data   | Data   | Data   | Badge  | View Edit More       |
------------------------------------------------------------

Showing 1–10 of 120                         < 1 2 3 >
```

## Table Rules

- Use readable column names.
- Keep action controls consistent.
- Use status badges.
- Support sorting where useful.
- Support filtering where useful.
- Use pagination.
- Do not overcrowd tables with unnecessary columns.
- Important information should appear before less important information.

---

# 20. Search and Filters

Major list screens should support appropriate search/filter controls.

Common filters:

- Keyword
- Status
- Category
- Supplier
- Customer
- Date range
- Priority

Filters should be visually grouped and easy to clear.

Example:

```text
[ Search products... ]

[Category ▼] [Status ▼] [Stock Status ▼] [Clear Filters]
```

---

# 21. Status Badges

Use consistent badge styles.

Examples:

```text
Active
Inactive

In Stock
Low Stock
Out of Stock

Draft
Submitted
Approved
Ordered
Received
Completed
Cancelled

Open
In Progress
On Hold
Completed
Cancelled
```

Status labels should remain consistent throughout all screens.

---

# 22. UI States

Every major screen should have the following designed states where applicable.

## Loading

Use:

- Skeletons
- Progress indicators
- Disabled duplicate actions

## Empty

Example:

```text
No products found

There are no products available.

[Add Product]
```

## No Search Results

```text
No matching products

Try changing your search or filters.
```

## Error

```text
Unable to load products.

Please try again.

[Retry]
```

## Permission Denied

```text
You don't have permission to access this page.
```

---

# 23. Notifications

Notifications should be accessible from the top bar and the Notifications screen.

Notification categories may include:

- Low stock
- Out of stock
- Purchase updates
- Sales/order updates
- Maintenance updates
- System alerts

Notification states:

- Read
- Unread

Unread notifications should have a clear visual distinction.

---

# 24. Responsive Design

The design should be desktop-first but responsive.

## Desktop

- Persistent sidebar
- Full top bar
- Multi-column forms
- Full data tables
- Dashboard card grid

## Tablet

- Collapsible sidebar
- Flexible cards
- Reduced table columns
- Responsive forms

## Small Screens

- Collapsed navigation
- Single-column forms
- Horizontally scrollable tables where necessary
- Stacked actions
- Priority information displayed first

The responsive design should preserve functionality rather than simply shrinking desktop layouts.

---

# 25. Final 32-Screen List

## Public

1. Landing Page

## Authentication

2. Login
3. Forgot Password

## Dashboard

4. Dashboard

## Products

4. Product List
5. Add Product
6. Product Details
7. Edit Product

## Categories

8. Category List
9. Add/Edit Category

## Suppliers

10. Supplier List
11. Add Supplier
12. Supplier Details
13. Edit Supplier

## Customers

14. Customer List
15. Add Customer
16. Customer Details
17. Edit Customer

## Purchases

18. Purchase Order List
19. Create Purchase Order
20. Purchase Order Details
21. Edit Purchase Order

## Sales / Orders

22. Sales Order List
23. Create Sales Order
24. Sales Order Details

## Inventory

25. Inventory Overview
26. Stock Movement History

## Maintenance

27. Maintenance List
28. Maintenance Details

## Notifications

29. Notifications

## Reports

30. Reports & Analytics

## Administration

31. Users & Roles

---

# 26. Screen Specifications

# 26.1 Landing Page

### Purpose

Introduce StockForge to visitors before authentication and provide a clear path into the web application. This public-facing home page is different from the authenticated Dashboard.

### UI Sections

- Header with StockForge logo, navigation, and Login CTA
- Hero section with “Hardware Inventory Management, Simplified.”
- Supporting description of StockForge
- Primary Login / Get Started CTA
- Key Features section
- Why StockForge / business benefits section
- Simple workflow overview
- Final call-to-action
- Footer

### Key Features

- Product Management
- Inventory Management
- Purchase Management
- Sales / Order Management
- Maintenance Management
- Reports & Analytics

### Workflow Visual

```text
Products
   ↓
Purchases
   ↓
Inventory
   ↓
Sales / Orders
   ↓
Maintenance
   ↓
Reports
```

### Navigation

```text
Landing Page
   ↓
Login
   ↓
Dashboard
```

### Important Rule

The Landing Page is public and must not display private business data, inventory quantities, customer information, supplier information, purchase orders, sales orders, notifications, or user-specific dashboard content.

### Responsive Behavior

- Desktop: full navigation, large hero, feature grid, workflow, footer
- Tablet: condensed navigation and responsive feature grid
- Small screen: collapsed navigation, stacked hero, single-column features, vertical workflow

### Design Style

Use the same StockForge visual system: `#4CAF7D` primary color, light theme, clean typography, subtle borders, restrained shadows, consistent spacing, and professional business-focused styling.

---

# 26.2 Login

### Purpose

Provide secure entry into the StockForge web application.

### UI Elements

- StockForge logo/brand
- Email/username field
- Password field
- Show/hide password
- Remember me
- Login button
- Forgot password link
- Validation/error message

### States

- Default
- Field validation error
- Invalid credentials
- Loading
- Disabled login button

### Navigation

```text
Login
 ├── Forgot Password
 └── Successful Login → Dashboard
```

---

# 26.3 Forgot Password

### Purpose

Allow users to request password recovery.

### UI Elements

- Email field
- Submit button
- Back to login
- Success message
- Error state

### Navigation

```text
Login → Forgot Password → Login
```

---

# 26.4 Dashboard

### Purpose

Provide an overview of the business and inventory.

### UI Sections

#### KPI Cards

- Total Products
- Total Stock
- Low Stock
- Out of Stock
- Pending Purchases
- Pending Orders

#### Analytics

- Stock overview
- Purchase trend
- Sales trend
- Top products

#### Recent Activity

- Recent purchases
- Recent sales/orders
- Recent maintenance

#### Quick Actions

- Add Product
- Create Purchase Order
- Create Sales Order
- Add Supplier
- Add Customer

### Design Priority

Important warnings such as low stock and out-of-stock items should be highly visible.

---

# 26.5 Product List

### Purpose

Display and manage all products.

### UI Elements

- Page title
- Breadcrumb
- Search
- Category filter
- Status filter
- Stock filter
- Add Product button
- Product table
- Pagination

### Table Columns

```text
Product Code
Product Name
Category
Purchase Price
Selling Price
Current Stock
Minimum Stock
Status
Actions
```

### Actions

- View
- Edit
- Activate/deactivate

---

# 26.6 Add Product

### Purpose

Create a new product.

### Sections

#### Product Information

- Product code
- Product name
- Description
- Category
- Unit

#### Pricing

- Purchase price
- Selling price

#### Inventory

- Minimum stock level
- Initial stock where applicable

### Actions

```text
Cancel
Save Product
```

---

# 26.7 Product Details

### Purpose

Display complete product information.

### UI Sections

- Product summary
- Product information
- Category
- Pricing
- Current stock
- Minimum stock
- Stock status
- Recent stock movements
- Related purchase/sales information where appropriate

### Actions

- Edit
- Activate/deactivate

---

# 26.8 Edit Product

### Purpose

Modify an existing product.

### Design

Use the same structure as Add Product with existing information populated.

The interface should clearly distinguish editable and non-editable information where applicable.

---

# 26.9 Category List

### Purpose

Display and manage product categories.

### UI Elements

- Search
- Add Category
- Category table
- Status
- Product count
- Actions
- Pagination

### Table Columns

```text
Category
Description
Product Count
Status
Actions
```

---

# 26.10 Add/Edit Category

### UI Elements

- Category name
- Description
- Active/inactive status
- Save
- Cancel

The same screen structure can be used for both creating and editing.

---

# 26.11 Supplier List

### Purpose

Manage suppliers.

### UI Elements

- Search
- Status filter
- Add Supplier
- Supplier table
- Pagination

### Table Columns

```text
Supplier Code
Company
Contact Person
Phone
Email
Status
Actions
```

---

# 26.12 Add Supplier

### Sections

#### Supplier Information

- Supplier code
- Company name
- Contact person

#### Contact

- Email
- Phone

#### Address

- Address
- City
- State
- Postal code

#### Additional

- Tax number
- Notes
- Active status

---

# 26.13 Supplier Details

### UI Sections

- Supplier summary
- Contact information
- Address
- Purchase history
- Relevant business information

### Actions

- Edit
- Activate/deactivate

---

# 26.14 Edit Supplier

Use the Add Supplier structure with existing information populated.

---

# 26.15 Customer List

### Purpose

Manage customers.

### UI Elements

- Search
- Status filter
- Add Customer
- Customer table
- Pagination

### Table Columns

```text
Customer Code
Name
Company
Phone
Email
Status
Actions
```

---

# 26.16 Add Customer

### Sections

#### Customer Information

- Customer code
- Name
- Company name

#### Contact

- Email
- Phone

#### Address

- Address
- City
- State
- Postal code

#### Additional

- Tax number
- Notes
- Active status

---

# 26.17 Customer Details

### UI Sections

- Customer summary
- Contact information
- Address
- Order history
- Relevant customer information

### Actions

- Edit
- Activate/deactivate

---

# 26.18 Edit Customer

Use the Add Customer structure with existing information populated.

---

# 26.19 Purchase Order List

### Purpose

Manage purchase orders.

### UI Elements

- Search
- Supplier filter
- Status filter
- Date range
- Create Purchase Order
- Purchase order table
- Pagination

### Table Columns

```text
PO Number
Supplier
Order Date
Expected Date
Total
Status
Actions
```

---

# 26.20 Create Purchase Order

### Purpose

Create a purchase order for a supplier.

### Sections

#### Supplier

- Supplier selector
- Supplier summary

#### Order Information

- PO number
- Order date
- Expected date
- Notes

#### Items

Each row should contain:

- Product
- Quantity
- Unit price
- Discount
- Tax
- Line total

#### Summary

- Subtotal
- Discount
- Tax
- Total

### Actions

```text
Cancel
Save Draft
Submit
```

---

# 26.21 Purchase Order Details

### UI Sections

- PO summary
- Supplier information
- Order information
- Item list
- Amount summary
- Status
- Activity/history

### Contextual Actions

Depending on status:

- Edit
- Submit
- Approve
- Receive
- Cancel

Actions should only appear when appropriate.

---

# 26.22 Edit Purchase Order

Use the Create Purchase Order layout.

The editing experience should depend on the order status.

Completed/received records should not appear as normally editable.

---

# 26.23 Sales Order List

### Purpose

Manage customer sales/orders.

### UI Elements

- Search
- Customer filter
- Status filter
- Date range
- Create Sales Order
- Sales order table
- Pagination

### Table Columns

```text
Order Number
Customer
Order Date
Total
Status
Actions
```

---

# 26.24 Create Sales Order

### Sections

#### Customer

- Customer selector
- Customer information

#### Items

Each row:

- Product
- Quantity
- Unit price
- Discount
- Tax
- Line total

#### Summary

- Subtotal
- Discount
- Tax
- Total

#### Additional

- Notes

### Actions

```text
Cancel
Save
Confirm
```

---

# 26.25 Sales Order Details

### UI Sections

- Order summary
- Customer information
- Items
- Amount summary
- Status
- Activity/history

### Contextual Actions

Depending on status:

- Edit
- Confirm
- Process
- Complete
- Cancel

---

# 26.26 Inventory Overview

### Purpose

Provide a centralized view of current inventory.

### KPI Cards

- Total Products
- Total Stock
- Low Stock
- Out of Stock

### Filters

- Search
- Category
- Stock status

### Table Columns

```text
Product
Category
Current Stock
Minimum Stock
Stock Status
Last Movement
Actions
```

### Visual Priority

Low-stock and out-of-stock items should be immediately noticeable.

---

# 26.27 Stock Movement History

### Purpose

Display the history of stock changes.

### Filters

- Product
- Movement type
- Date range
- User

### Table Columns

```text
Date
Product
Movement Type
Quantity
Previous Stock
New Stock
Reference
User
```

### Movement Types

- Purchase Receipt
- Sales Issue
- Manual Adjustment
- Return
- Maintenance Consumption
- Other approved movement

---

# 26.28 Maintenance List

### Purpose

Display and manage maintenance records.

### Filters

- Search
- Status
- Priority
- Date

### Table Columns

```text
Reference
Product
Issue
Priority
Assigned To
Status
Start Date
Expected Completion
Actions
```

---

# 26.29 Maintenance Details

### UI Sections

- Maintenance reference
- Product
- Issue description
- Maintenance type
- Priority
- Assigned user
- Start date
- Expected completion
- Completion date
- Cost
- Notes
- Status history

### Actions

- Edit
- Update status
- Complete
- Cancel where applicable

---

# 26.30 Notifications

### Purpose

Provide a centralized notification center.

### UI Elements

- All notifications
- Unread filter
- Notification list
- Read/unread state
- Mark as read
- Mark all as read
- Related record navigation

### Notification Card

Each notification may show:

```text
Icon
Title
Message
Time
Read/Unread state
Related action
```

---

# 26.31 Reports & Analytics

### Purpose

Provide visual business information.

### Report Categories

#### Inventory

- Current stock
- Low stock
- Out of stock
- Stock movements

#### Purchases

- Purchase summary
- Supplier purchases
- Purchase order status

#### Sales

- Sales summary
- Customer orders
- Product sales

#### Maintenance

- Maintenance summary
- Open maintenance
- Maintenance cost

### UI Elements

- Report selector
- Date filters
- Additional filters
- KPI summary
- Charts
- Data table
- Export action

---

# 26.32 Users & Roles

### Purpose

Provide an administrative interface for managing users and their roles.

### UI Elements

- Search
- Role filter
- Status filter
- Add user
- User table
- Role management

### Table Columns

```text
Name
Email
Role
Status
Last Login
Actions
```

### User Form

- Full name
- Email
- Phone
- Role
- Active/inactive status

### Role Interface

Display available permissions in a clear grouped structure.

Example:

```text
Products
[✓] View
[✓] Create
[✓] Edit
[ ] Delete

Inventory
[✓] View
[ ] Adjust Stock
```

---

# 27. Main Navigation Flow

The primary prototype flow should be:

```text
Login
  ↓
Dashboard
  ↓
Sidebar Navigation
  ├── Products
  ├── Categories
  ├── Suppliers
  ├── Customers
  ├── Purchases
  ├── Sales / Orders
  ├── Inventory
  ├── Maintenance
  ├── Notifications
  ├── Reports
  └── Users & Roles
```

---

# 28. Product Flow

```text
Product List
   ↓
Add Product
   ↓
Save
   ↓
Product Details
   ↓
Edit Product
```

---

# 29. Purchase Flow

```text
Purchase Order List
        ↓
Create Purchase Order
        ↓
Save / Submit
        ↓
Purchase Order Details
        ↓
Approve
        ↓
Receive
        ↓
Completed
```

---

# 30. Sales Flow

```text
Sales Order List
        ↓
Create Sales Order
        ↓
Save / Confirm
        ↓
Sales Order Details
        ↓
Process
        ↓
Complete
```

---

# 31. Inventory Flow

```text
Inventory Overview
        ↓
Select Product
        ↓
View Stock Information
        ↓
Stock Movement History
```

---

# 32. Maintenance Flow

```text
Maintenance List
        ↓
Maintenance Details
        ↓
Update Status
        ↓
In Progress
        ↓
Completed
```

---

# 33. Important Modal and State Designs

These are reusable UI states and are **not additional screens**.

## Confirmation Modal

Used for actions such as:

- Delete
- Deactivate
- Cancel
- Complete

Structure:

```text
Title
Description

[Cancel] [Confirm]
```

## Delete Confirmation

```text
Delete Product?

This action cannot be undone.

[Cancel] [Delete]
```

## Unsaved Changes

```text
You have unsaved changes.

Are you sure you want to leave?

[Stay] [Leave]
```

## Success Toast

```text
Product created successfully.
```

## Error Toast

```text
Unable to complete the action.
```

---

# 34. Figma File Structure

The Figma project should be organized into the following pages:

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

---

# 35. Figma Component Naming

Use predictable names.

```text
Button/Primary
Button/Secondary
Button/Danger
Button/Icon

Input/Text
Input/Number
Input/Search
Input/Date
Input/Select

Table/Default
Table/Loading
Table/Empty

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
Navigation/Breadcrumb

Toast/Success
Toast/Error
Toast/Warning
Toast/Info
```

---

# 36. Figma Variants

Reusable components should have variants.

Example:

```text
Button
 ├── Primary
 ├── Secondary
 ├── Danger
 ├── Disabled
 └── Loading

Input
 ├── Default
 ├── Focus
 ├── Filled
 ├── Error
 └── Disabled

Badge
 ├── Success
 ├── Warning
 ├── Error
 └── Neutral
```

This keeps the design consistent and makes implementation easier.

---

# 37. Accessibility Design

The UI should consider:

- Clear text hierarchy
- Readable font sizes
- Adequate contrast
- Visible focus states
- Clear labels
- Clear validation messages
- Keyboard-friendly controls
- Status indicators that do not depend only on color
- Meaningful button labels

---

# 38. Design Consistency Rules

Every module must follow the same visual system.

## Lists

Use the same:

- Page header
- Search area
- Filter area
- Table style
- Pagination
- Action placement

## Forms

Use the same:

- Label style
- Input style
- Section cards
- Validation style
- Action bar

## Details

Use the same:

- Page header
- Status badge
- Summary card
- Information sections
- Related information
- Action placement

## Navigation

Use the same:

- Sidebar
- Top bar
- Breadcrumbs
- Active states

---

# 39. Design Do / Don't

## Do

- Use consistent spacing.
- Reuse components.
- Keep tables readable.
- Make important actions obvious.
- Use clear status labels.
- Design empty/loading/error states.
- Keep navigation consistent.
- Use responsive layouts.
- Maintain a professional business appearance.

## Don't

- Create a different layout for every module.
- Use unnecessary colors.
- Overload tables with information.
- Hide important actions.
- Use color as the only status indicator.
- Create separate screens for simple confirmation dialogs.
- Add unnecessary decorative elements.
- Add new primary screens without updating the final screen scope.

---

# 40. Final Design Checklist

Before considering the Figma design complete:

## Design System

- [ ] Colors
- [ ] Typography
- [ ] Spacing
- [ ] Border radius
- [ ] Shadows
- [ ] Buttons
- [ ] Inputs
- [ ] Badges

## Components

- [ ] Sidebar
- [ ] Top bar
- [ ] Breadcrumb
- [ ] Tables
- [ ] Pagination
- [ ] Filters
- [ ] Cards
- [ ] Modals
- [ ] Toasts
- [ ] Empty states
- [ ] Loading states
- [ ] Error states

## Screens

- [ ] Landing Page
- [ ] Login
- [ ] Forgot Password
- [ ] Dashboard
- [ ] Product List
- [ ] Add Product
- [ ] Product Details
- [ ] Edit Product
- [ ] Category List
- [ ] Add/Edit Category
- [ ] Supplier List
- [ ] Add Supplier
- [ ] Supplier Details
- [ ] Edit Supplier
- [ ] Customer List
- [ ] Add Customer
- [ ] Customer Details
- [ ] Edit Customer
- [ ] Purchase Order List
- [ ] Create Purchase Order
- [ ] Purchase Order Details
- [ ] Edit Purchase Order
- [ ] Sales Order List
- [ ] Create Sales Order
- [ ] Sales Order Details
- [ ] Inventory Overview
- [ ] Stock Movement History
- [ ] Maintenance List
- [ ] Maintenance Details
- [ ] Notifications
- [ ] Reports & Analytics
- [ ] Users & Roles

## Prototype

- [ ] Login → Dashboard
- [ ] Sidebar navigation
- [ ] Product CRUD flow
- [ ] Supplier flow
- [ ] Customer flow
- [ ] Purchase flow
- [ ] Sales flow
- [ ] Inventory flow
- [ ] Maintenance flow
- [ ] Notifications flow
- [ ] Reports flow
- [ ] User management flow

## Responsive

- [ ] Desktop
- [ ] Tablet
- [ ] Small screen
- [ ] Collapsed sidebar
- [ ] Responsive forms
- [ ] Responsive tables

---

# 41. Final Screen Count

The final StockForge web application UI/UX design contains:

## **32 Primary Screens**

No additional primary screens should be added unless the project requirements are intentionally changed.

Dialogs, popups, drawers, confirmation states, loading states, empty states, and error states remain reusable UI components/states.

---

# 42. Final Design Direction

The final StockForge web design should feel:

```text
Professional
Modern
Clean
Simple
Business-focused
Data-oriented
Consistent
Responsive
Scalable
```

The design should prioritize **usability and operational efficiency over visual complexity**.

This document is the **final UI/UX/Figma design reference** for the StockForge .NET web application.
