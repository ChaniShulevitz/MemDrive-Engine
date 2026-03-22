##MemDrive Engine -
A robust, high-performance In-Memory Data Management System built from scratch using Advanced Design Patterns and Clean Code principles. This engine mimics core database functionalities including dynamic schema definition, CRUD operations, and a complex querying system.

 #Architecture & Design Patterns
The system is architected using 8 core design patterns to ensure scalability, maintainability, and decoupling.

 #Creational Patterns
Builder Pattern: Used for the Table construction process. It provides a fluent API to define table names and add columns step-by-step before finalizing the object.

Singleton Pattern: Ensures there is only one instance of the Database manager across the application, providing a global point of access to tables.

Prototype Pattern: Implemented for the Table Cloning requirement. It allows creating an independent deep copy of a table (schema and rows) without affecting the original data.

# Structural Patterns
Facade Pattern: Provides a simplified DBClient interface. Users interact with a clean API (e.g., db.Insert, db.Query) while the complex logic remains hidden.

Composite Pattern: Powering the Query & Condition System. It allows building complex logical trees (AND/OR conditions) that can be evaluated as a single unit against data rows.

# Behavioral Patterns
Command Pattern: Every data operation (Insert, Update, Delete, Query) is encapsulated as a standalone object. This ensures a uniform execution structure: Validation -> Execution -> Result.

Observer Pattern: Handles Change Reactions and Logging. The system automatically notifies registered loggers whenever a data mutation occurs.

Iterator Pattern: (Optional/Implemented) Provides different strategies for traversing table rows, such as insertion order or sorted by specific columns.

# Key Features
Dynamic Schema: Define tables with specific data types (String, Int, Bool).

Complex Queries: Support for nested conditions and logical operators.

Data Integrity: Validation logic built into every operation.

Independent Cloning: Full decoupled copies of datasets.
