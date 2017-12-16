### ER Diagram

```uml
@startuml
    entity "foo" {
        + foo_id
        --
        name
        ...
    }
    entity "bar" {
        + bar_id
        --
        # foo_id
        name
        ...
    }
    foo ||-ri-o{ bar
@enduml
```