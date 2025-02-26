# Santander Dev Week 2023
Esta é uma API construida durante a Santander Dev Week 2023, parceria do Banco Santander com a plataforma de estudos DIO, a API segue a arquitetura REST e foi construida na linguagem JAVA com o framework SpringBoot

## Diagrama de Classes
```mermaid
classDiagram
    class User {
        -String name
        -Account account
        -List~Feature~ features
        -Card card
        -List~News~ news
    }

    class Account {
        -String number
        -String agency
        -String balance
        -String limit
    }

    class Feature {
        -String icon
        -String description
    }

    class Card {
        -String number
        -String limit
    }

    class News {
        -String icon
        -String description
    }

    User "1" *-- "1"Account
    User "1" *-- "1*"Card
    User "1"*-- "1..*" Feature
    User "1"*-- "1..*" News
```
