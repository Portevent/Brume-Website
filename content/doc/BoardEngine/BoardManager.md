---
title: BoardManager
path: /BoardEngine
alias: 
- Board Manager
tag: 
- class
---
Use the [WorldManager]({{< ref "WorldManager" >}}) to compute existing cell ([Coordinate]({{< ref "Coordinate" >}})) and free cell toward/away.
Also communicate with [EntityManager]({{< ref "EntityManager" >}}) to determine if a cell is free.
```d2
# Nodes :
BoardEngine: {
    WorldManager: World Manager {
       link: WorldManager
    }
    Coordinate: Coordinate {
       link: Coordinate
    }
}
MagicEngine: {
    MagicManager: Magic Manager {
       link: MagicManager
    }
}

# Links :
BoardEngine.BoardManager -- BoardEngine.Coordinate: {style.stroke-dash: 3}
BoardEngine.WorldManager -> BoardEngine.BoardManager: Get active World {style.stroke-dash: 3
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.BoardManager -> MagicEngine.MagicManager: Manipulate Cell {style.stroke-dash: 3
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}

```
---
# Summary :
name|description
----|----
[CellFree]({{< ref "#cellfree" >}}) | `Determinate if a cell is free (cell exist and no entity there)`

---
# Functions :

---
### CellFree
Determinate if a cell is free (cell exist and no entity there)

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|

#### Return
- `bool` : 
