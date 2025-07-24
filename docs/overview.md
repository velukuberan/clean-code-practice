# ✅ Overview
A modular, scalable **Library Management System** designed using the SOLID principles. The focus is not just functionality, but how to design software that is maintainable, extensible, and testable.

## 📦 Core Features

- **Book Management**
  - Add, update, delete, search books
  - Categorize books (genre, tags)
- **User Management**
  - Roles: Member, Librarian
  - Registration, account management
- **Borrowing System**
  - Borrow/return books
  - Limit validation, due dates
  - Fine calculation for overdue returns
- **Notification System**
  - Email, SMS, and In-App alerts
  - Notify about due dates, fines, etc.
- **Reports Module**
  - Generate reports (borrowed books, late returns, user stats)

## 🧱 Architecture (Domain-Driven Skeleton)

```
/src
  /Books
    Book.ts
    BookCategory.ts
    BookRepository.ts
    IBookRepository.ts

  /Users
    User.ts
    Member.ts
    Librarian.ts
    IUserRepository.ts

  /Borrowing
    Borrowing.ts
    BorrowingService.ts
    FineCalculator.ts

  /Notifications
    INotifier.ts
    EmailNotifier.ts
    SMSNotifier.ts
    InAppNotifier.ts

  /Reports
    ReportGenerator.ts
    BorrowedBooksReport.ts
    OverdueReport.ts

  /Shared
    Result.ts (Success/Failure wrapper)
    DateProvider.ts (abstracted date logic)

  /Interfaces
    IBookManager.ts
    IUserManager.ts
    IBorrowingPolicy.ts
```

## 📅 2-Week Learning & Build Plan

| Day    | Focus                | Activities                                         | SOLID Focus      |
|--------|----------------------|----------------------------------------------------|------------------|
| Day 1  | Setup + Book Entity  | Project setup, define Book, Category, BookRepository| SRP              |
| Day 2  | User Management      | Create User, Member, Librarian, roles, permissions  | SRP              |
| Day 3  | Borrowing Logic      | Design Borrowing entity, borrowing rules            | SRP              |
| Day 4  | Fine Calculation     | Add FineCalculator, decouple policies               | OCP              |
| Day 5  | Notification Interface| Create INotifier + EmailNotifier                   | OCP, DIP         |
| Day 6  | Add SMS + InApp Notifiers| Use INotifier, inject dynamically              | OCP, LSP         |
| Day 7  | Interface Refinement | Split into small interfaces (IBorrower, IAdmin)     | ISP              |
| Day 8  | Dependency Inversion | Inject all services via interfaces                  | DIP              |
| Day 9  | Reporting System     | Borrowed books report, overdue report               | SRP, DIP         |
| Day 10 | Testing + Mocks      | Unit test borrowing, fine calc, notifiers           | SRP              |
| Day 11 | Refactoring          | Refactor for clean interfaces, remove tight coupling| All              |
| Day 12 | Containerization (Optional)| Add Docker setup (DB + App)                  | -                |
| Day 13 | Docs + README        | Add usage docs, diagrams, SOLID summary             | -                |
| Day 14 | Review               | Final cleanup, submittable build                    | -                |

## 🔧 Technologies (pick your stack)

- **Language:** TypeScript / PHP / Python
- **Testing:** Jest (TS), PHPUnit (PHP), Pytest (Python)
- **Email/SMS:** Mocked services for learning
- **Persistence:** In-memory or SQLite (real DB optional)
- **Architecture:** DDD-inspired folder and interface design

## 📚 Learning Outcomes

- Understand and apply all SOLID principles
- Design using interfaces and abstractions
- Avoid code smells (God classes, rigid design)
- Write testable, extensible modules
- Prepare for real-world software engineering
