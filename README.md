#InMemory Database Engine
#Advanced Data Management System in C-Sharp
This project is a high-performance In-Memory Data Engine developed with a focus on software architecture, clean code principles, and advanced design patterns. The system provides a robust framework for managing relational data structures entirely in memory, featuring a fluent API and a modular query system.

##Architecture and Design Patterns
The system is built using a decoupled architecture, ensuring that each component has a single responsibility. To achieve this, the project implements 8 core design patterns:

###Creational Patterns
   Singleton: The Database class is implemented as a Singleton, ensuring a single source of truth for all tables across the application.

   Builder: Tables are defined through a step-by-step construction process, allowing for a readable and fluid schema definition.

   Prototype: Used for the Table Cloning feature, enabling the creation of deep, independent copies of existing tables and their rows.

###Structural Patterns
   Facade: Provides a simplified DBClient interface, hiding the complexity of the internal engine and operations from the end-user.

   Composite: Powering the Query System. it allows nesting simple conditions into combined logical structures (AND/OR) for complex data filtering.

##3Behavioral Patterns
   Command: Every data operation (Insert, Update, Delete, Query) is encapsulated as an object, ensuring a consistent flow of Validation, Execution, and Result.

   Observer: Used for the Logging System. The database notifies registered observers whenever a data change occurs, allowing for extensible reactions.

   Iterator: Provides multiple strategies for traversing table rows, supporting different sorting and filtering methods.

##Key Features
###Fluent Table Definition: Clean and readable syntax for creating tables and schemas.

##3Dynamic Schema Validation: Strict type enforcement (String, Int, Bool) during all data operations.

##3Complex Logical Queries: Support for deeply nested search conditions and logical operators.

##3Decoupled Design: Every class follows the Single Responsibility Principle for maximum maintainability and testing.
