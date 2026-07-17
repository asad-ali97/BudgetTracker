# Budget Tracker (Java Swing)

A desktop budget management application built with Java and Swing to help track income, expenses, category spending, and current balance within a single session.

## Overview

This project provides a menu-driven GUI for personal budget tracking. Users can add income/expense records with dates, define spending limits by category, review balance and category-wise reports, and view sorted expense lists.

The app is currently in-memory only (no database/file persistence), making it suitable for learning, coursework, and core OOP/GUI demonstration.

## Key Features

- Add income entries with amount, source, and date
- Add expense entries with amount, category, and date
- View total income, total expenses, and net balance
- Category-wise expense report
- Set spending limit for a category
- Warning when category spending reaches/exceeds limit
- Sort expenses by amount
- Sort expenses by date
- Session summary including highest expense category
- Reset all in-session data

## Tech Stack

- Language: Java
- GUI: Java Swing (`javax.swing`)
- Date API: `java.time.LocalDate`
- Build style: Plain Java project (no Maven/Gradle required)

## Project Structure

- `BudgetTrackerApp.java` - application entry point
- `BudgetMenuGUI.java` - main GUI menu and user interactions
- `BudgetManager.java` - business logic and calculations
- `Income.java` - income model
- `Expense.java` - expense model
- `AddIncomeWindow.java` - standalone income input window component
- `AddExpenseWindow.java` - standalone expense input window component
- `Readme.txt` - earlier project description

## How It Works

1. App starts from `BudgetTrackerApp.main()`.
2. Main window (`BudgetMenuGUI`) initializes a single `BudgetManager` instance.
3. User actions (buttons/menu flow) call manager methods.
4. `BudgetManager` stores entries in memory using lists/maps and computes summaries/reports.

## Prerequisites

- JDK 17+ (recommended)
- Any Java IDE (IntelliJ IDEA/Eclipse/NetBeans) or terminal with `javac/java`

## Run Locally

### Option 1: IDE

1. Open the project folder.
2. Ensure package name is recognized as `budgettracker`.
3. Run `BudgetTrackerApp.java`.

### Option 2: Command Line

From the parent directory containing the `budgettracker` package folder:

```bash
javac budgettracker/*.java
java budgettracker.BudgetTrackerApp
```

## Usage Guide

- **Add Income**: enter amount, source, and date (`YYYY-MM-DD`)
- **Add Expense**: enter amount, category, and date (`YYYY-MM-DD`)
- **View Balance**: see total income, total expense, and remaining balance
- **Category Report**: view total spent per category
- **Set Category Limit**: define max threshold for a category
- **Sort Expenses**: list expenses by amount/date
- **Session Summary**: quick snapshot of key metrics
- **Reset Data**: clear all current session entries

## Validation and Error Handling

- Basic numeric validation for amount inputs
- Date format validation using `LocalDate.parse(...)`
- Dialog-based feedback for invalid input and operation results

## Current Limitations

- No persistent storage (all data is lost after app closes)
- No authentication or multi-user support
- No edit/delete operation for individual records
- Monetary values use `double` (not `BigDecimal`)
- Sorting is ascending only
- Currency/locale formatting is minimal

## Suggested Improvements

- Add file or database persistence (JSON/SQLite/MySQL)
- Introduce `BigDecimal` for financial precision
- Add edit/delete functionality for records
- Add monthly/yearly analytics dashboards
- Add export to CSV/PDF
- Add unit tests for `BudgetManager`
- Improve UI consistency by reusing `AddIncomeWindow` / `AddExpenseWindow` from main menu

## Academic Context

This project is well-suited for demonstrating:

- Object-Oriented Programming (models + manager + UI separation)
- Java Collections and Streams
- Event-driven GUI programming with Swing
- Input validation and exception handling

## License

No license file is currently included. Consider adding an open-source license (e.g., MIT) if this repository will be public.

## Author

Add your name, institution, and contact links here before publishing to GitHub.
