### Lược đồ Class - Hệ thống Quản lý Thư viện

```mermaid
classDiagram
    class Book {
        +String bookID
        +String title
        +updateStatus()
    }
    class Member {
        +String memberID
        +borrowBook()
    }
    class Loan {
        +String loanID
        +Date borrowDate
    }
    Member "1" -- "0..*" Loan
    Book "1" -- "0..1" Loan
