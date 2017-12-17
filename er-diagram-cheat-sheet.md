# ER Diagram Cheat Sheet

## Entity

Basic entity.

```uml
@startuml
    entity entity1 {
        attribute
    }
    entity entity2 {
        attribute
    }
@enduml
```

In case of using space in entity name.

```uml
@startuml
    entity "entity 1" as entity1 {
        attribute
    }
    entity "entity 2" as entity2 {
        attribute
    }
@enduml
```

Change "E" to another character.
All character can be used only if this character is single.
You can change color at same time.

```uml
@startuml
    entity master <<M, DDAA00>> {
        attribute
    }
    entity 主テーブル <<主, 00AADD>> {
        attribute
    }
@enduml
```

Change entity color.

```uml
@startuml
    entity red #red {
        attribute
    }
    entity blue #blue {
        attribute
    }
    entity custermize #AAEEBB {
        attribute
    }
    entity gradation1 #red-green {
        attribute
    }
    entity gradation2 #red|green {
        attribute
    }
    entity gradation3 #red/green {
        attribute
    }
    entity gradation4 #red\green {
        attribute
    }
@enduml
```

Labeling.

```uml
@startuml
    entity entity1 <label type 1> {
        attribute
    }
    entity entity2 <<label type 2>> {
        attribute
    }
@enduml
```

## Attribute

There are some symbol placed at first of attribute.

```uml
@startuml
    entity "symbol for attribute" {
        + green circle
        - red square
        # yellow diamond
        ~ blue triangle
        * black circle
        nothing
    }
@enduml
```

Attribute can be bold, italic, underline and other style.

```uml
@startuml
    entity "style of attribute" {
        normal
        <b> bold
        <i> italic
        <u> underline
        <color:RED> red
    }
@enduml
```

Separator can be used as many times as desired.
And there are some style of separator.

```uml
@startuml
    entity "style of separator" {
        normal
        --
        double
        ==
        dot
        ..
        bold
        __
    }
@enduml
```

Can write title in separator.

```uml
@startuml
    entity "title in separator" {
        -- normal --
        == double ==
        .. dot ..
        __ bold __
    }
@enduml
```

## Relation


## Other





