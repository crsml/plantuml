# Plant UML

- コードブロック内で定義した定数は使える

```uml
@startuml
    !define RED #ff0000
    !define BLUE #0000FF

    entity "parent" RED {
        + parent_id
        --
    }

    entity "child" BLUE {
        + parent_id
        + child_id
        --
    }

    parent ||--o{ child

@enduml
```

- 同じmdファイル内の別のコードブロック内で定義した定数は使えない

```uml
@startuml

    entity "parent" RED {
        + parent_id
        --
    }

    entity "child" BLUE {
        + parent_id
        + child_id
        --
    }

    parent ||--o{ child

@enduml
```

- 別ファイルをincludeするのは、ローカルなら使えるけどPegmatiteは使えない

```uml
@startuml
    !include inc/settings.pu

    entity "parent" RED {
        + parent_id
        --
    }

    entity "child" BLUE {
        + parent_id
        + child_id
        --
    }

    parent ||--o{ child

@enduml
```
