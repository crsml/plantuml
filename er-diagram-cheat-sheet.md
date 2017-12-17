# ER Diagram Cheat Sheet

## Entity

Basic entity.
In case of using space in entity name, you can use keyword "as".

```uml
@startuml
    entity entity1 {
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

## Separator

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

## Relation (Cardinality)

Basic relation.
You can specify the position.

```uml
@startuml
    entity entity {
    }
    entity up {
    }
    entity down {
    }
    entity right {
    }
    entity left {
    }

    entity -up- up
    entity -do- down
    entity -ri- right
    entity -le- left
@enduml
```

Labeling.

```uml
@startuml
    entity entity1 {
    }
    entity entity2 {
    }

    entity1 -ri- entity2 : labeling
    entity1 -ri- entity2 : arrow >
    entity1 -ri- entity2 : arrow <
@enduml
```

Style of cardinality.

```uml
@startuml
    entity entity1 {
    }
    entity entity2 {
    }

    entity1 -ri- entity2 : one >
    entity1 -ri-o| entity2 : zero or one >
    entity1 -ri-o{ entity2 : zero or many >
    entity1 -ri-|| entity2 : one and only one >
    entity1 -ri-|{ entity2 : one or many >
    entity1 -ri-{ entity2 : many >
@enduml
```

## Other





