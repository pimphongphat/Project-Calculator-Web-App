# Project-Calculator-Web-App
Simple Software Development Documents Implement


|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|


```mermaid
classDiagram
    class Calculator {
        +add(a: number, b: number): number
        +subtract(a: number, b: number): number
        +multiply(a: number, b: number): number
        +divide(a: number, b: number): number
    }

    class User {
        -name: string
        -email: string
        +login()
        +logout()
        +useCalculator(calc: Calculator)
    }

    class History {
        +operations: string[]
        +addOperation(operation: string)
        +getOperations(): string[]
    }

    Calculator --|> User : uses
    Calculator --> History : maintains
    User --> History : accesses
