# santander-dev-week

Java RESTful API criada para Santander Dev Week.

## Diagrama de classes

```mermaid
classDiagram
  class User {
    - name: String
    - account: Account
    - features: Feature[]
    - card: Card
    - news: News[]
  }
  
  class Account {
    - number: String
    - agency: String
    - balance: Number
    - limit: Number
  }
  
  class Feature {
    - icon: String
    - description: String
  }
  
  class Card {
    - number: String
    - limit: Number
  }
  
  class News {
    - icon: String
    - description: String
  }

  User "1" -- "1" Account : has
  User "1" -- "1" Card : has
  User "1" -- "0..*" Feature : has
  User "1" -- "0..*" News : has
```

