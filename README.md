````mermaid
classDiagram
    class Board{
      -Long id
      -String name
    }
    class Column{
      -Long id
      -String name
      -String kind
      -Integer order
    }
    class Card{
      -Long id
      -String title
      -String description
      -OffSetDateTime createdAt
    }
    class Block{
      -Long id
      -String blockCause
      -String unblockCause
      -OffSetDateTime blockIn
      -OffSetDateTime unblockIn
    }

    Board "1" -- "*" Column
    Column "1" -- "0..*" Card
    Block "1" -- "*" Card
````