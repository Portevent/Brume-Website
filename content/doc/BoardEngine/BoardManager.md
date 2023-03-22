---
title: BoardManager
alias: 
- Board Manager
tag: 
- class
---
Use the [WorldManager]({{< ref "WorldManager" >}}) to compute existing cell ([Coordinate]({{< ref "Coordinate" >}})) and free cell toward/away.\
Also communicate with [EntityManager]({{< ref "EntityManager" >}}) to determine if a cell is free.

---
# Summary :
name|description
----|----
[CellFree]({{< ref "#cellfree" >}}) | `Determinate if a cell is free (cell exist and no entity there)`

---
### CellFree
Determinate if a cell is free (cell exist and no entity there)

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|

#### Return
- `bool` : 
