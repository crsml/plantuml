# Plant UML

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