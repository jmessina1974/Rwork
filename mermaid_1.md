```mermaid
classDiagram
    class Libro {
        +String titulo
        +String autores
        +String isbn
        +boolean isAvailable()
    }

class Revista {
        +String titulo
        +String autores
        +String isbn
        +boolean isAvailable()
    }
    class Miembro {
        +String name
        +String memberId
        +borrowBook(Book book)
        +returnBook(Book book)
    }

    class Bibliotecario {
        +String name
        +String employeeId
        +addBook(Book book)
        +removeBook(Book book)
    }

    class Biblioteca {
        +String name
        +List<Book> books
        +List<Member> members
        +List<Librarian> librarians
        +addMember(Member miembro)
        +removeMember(Member miembro)
    }

    Revista --> Biblioteca : Contiene
    Libro --> Biblioteca : Contiene
    Miembro --> Biblioteca : Registra
    Bibliotecario --> Biblioteca : Administra
