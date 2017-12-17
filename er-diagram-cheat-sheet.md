# ER Diagram Cheat Sheet

## Contents

- [Entity](#entity)
  - [Basic Entity](#basic-entity)
  - [Mark Character](#mark-character)
  - [Entity Color](#entity-color)
  - [Entity Label](#entity-label)
- [Attribute](#attribute)
  - [Attribute Symbol](#attribute-symbol)
  - [Attribute Style](#attribute-style)
- [Separator](#separator)
  - [Separator Style](#separator-style)
  - [Separator Title](#separator-title)
- [Relation](#relation)
  - [Basic Relation](#basic-relation)
  - [Relation Label](#relation-label)
  - [Cardinality](#cardinality)
- [Package](#package)
  - [Package Style](#package-style)
  - [Package Relation](#package-relation)
- [Other](#other)
  - [Skin Parameter](#skin-parameter)
  - [Constant Value](#constant-value)
  - [Memo](#memo)

## Entity

### Basic Entity

```uml
@startuml
    entity entity1 {
        primary_key
        --
        attribute
    }
    entity "entity 2" as entity2 {
    }
@enduml
```

### Mark Character

```uml
@startuml
    entity master <<M, DDAA00>> {
    }
    entity 主テーブル <<主, 00AADD>> {
    }
@enduml
```

### Entity Color

```uml
@startuml
    entity red #red {
    }
    entity blue #blue {
    }
    entity custermize #AAEEBB {
    }
    entity gradation1 #red-green {
    }
    entity gradation2 #red|green {
    }
    entity gradation3 #red/green {
    }
    entity gradation4 #red\green {
    }
@enduml
```

### Entity Label

```uml
@startuml
    entity entity1 <label type 1> {
    }
    entity entity2 <<label type 2>> {
    }
@enduml
```

## Attribute

### Attribute Symbol

```uml
@startuml
    entity "attribute symbol" {
        + green circle
        - red square
        # yellow diamond
        ~ blue triangle
        * black circle
        nothing
    }
@enduml
```

### Attribute Style

```uml
@startuml
    entity "attribute style" {
        normal
        <b> bold
        <i> italic
        <u> underline
        <color:RED> red
    }
@enduml
```

## Separator

### Separator Style

```uml
@startuml
    entity "separator style" {
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

### Separator Title

```uml
@startuml
    entity "separator title" {
        -- normal --
        == double ==
        .. dot ..
        __ bold __
    }
@enduml
```

## Relation

### Basic Relation

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

### Relation Label

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

### Cardinality

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

## Package

### Package Style

```uml
@startuml
    package default {
        entity entity1 {
        }
    }

    package node <<Node>> {
        entity entity2 {
        }
    }

    package rectangle <<Rectangle>> {
        entity entity3 {
        }
    }

    package frame <<Frame>> {
        entity entity4 {
        }
    }

    package cloud <<Cloud>> {
        entity entity5 {
        }
    }

    package database <<Database>> {
        entity entity6 {
        }
    }

    package folder <<Folder>> {
        entity entity7 {
        }
    }
@enduml
```

### Package Relation

```uml
@startuml
    package package1 <<Node>> {
        entity entity1 {
        }
    }

    package package2 <<Node>> {
        entity entity2 {
        }
    }

    package1 -ri- package2
@enduml
```

## Other

### Skin Parameter

```uml
@startuml
    skinparam class {
        BackgroundColor PaleGreen
        ArrowColor SeaGreen
        BorderColor Green
    }

    entity entity1 {
    }
    entity entity2 {
    }

    entity1 -ri- entity2
@enduml
```

### Constant Value

```uml
@startuml
    !define RED #FFAAAA

    entity entity1 RED {
    }
    entity entity2 RED {
    }
@enduml
```

### Memo

```uml
@startuml
    entity entity1 {
    }
    entity entity2 {
    }

    note top of entity1 : this is note1.
    note bottom of entity2 : this is note2.
    note right of entity2 : this is note3.\nnext line.

    entity1 -ri- entity2
    note on link : this is note4.
@enduml
```
