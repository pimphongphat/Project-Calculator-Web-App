# Project-Calculator-Web-App
Simple Software Development Documents Implement

[Mermaid Live Editor](https://mermaid.live/edit#pako:eNqNUj1PwzAU_CuWp0RNq3y1STx0gYGNAbFAGFzbBEuJHfkDEUr-O25KQgIdasnS0_nu6d75HSGRlEEESY21vuW4UrgpBXBnQMANromtsZEKHM_46awwpR5GQNjmwFQADmPpj8WMq-3BKEzM1YLG1oa3dXe1gPJ3Ttk19L4U8-keNVvMtRa4YQhoo7ioZjBrMK__46taVlx4_hKR1iwgq9lvih5xJZrF6l80dse1e-sWmcuWKWy4FHp08vyy_JL7keFN3JE6N1QxMzG15__tNlmZ_f16_bU_p4WAm0dfIOwn0wi4uIRx94c3CJcMTAjTQyMYwIYpp6BuDYd5S2jeWMNKiFxJ2St2-1DCUvSOiq2RD50gEBllWQBtS7FhP4s7gi0WEB3hB0RZlGySXZoXaZRFRbyNAthBVGzyMErSMEvCNEvzOOsD-Cml04ebIonDIou3uyhPdnEaD92ehsdT8_4b1ej8RA)

[Markdown Online Editor](https://stackedit.io/)

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
