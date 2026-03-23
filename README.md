classDiagram
    class Book {
        +String bookID
        +String title
        +String author
        +String isbn
        +String status
        +updateStatus()
    }

    class Member {
        +String memberID
        +String name
        +String address
        +borrowBook()
        +returnBook()
    }

    class Loan {
        +String loanID
        +Date borrowDate
        +Date dueDate
        +calculateFine()
    }

    class Librarian {
        +String employeeID
        +String name
        +manageBooks()
        +issueLoan()
    }

    Member "1" -- "0..*" Loan : thực hiện
    Book "1" -- "0..1" Loan : thuộc về
    Librarian "1" -- "0..*" Loan : xử lý
