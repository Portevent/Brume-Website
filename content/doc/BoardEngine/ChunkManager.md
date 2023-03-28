---
title: ChunkManager
path: /BoardEngine
alias: 
- Chunk Manager
tag: 
- class
---
Linked to a [World]({{< ref "World" >}}), generate and unload world part as the player moves around
```d2
# Nodes :
BoardEngine: {
    World: World {
       link: World
    }
    WorldManager: World Manager {
       link: WorldManager
    }
}
GameplayManager: {
    GameManager: Game Manager {
       link: GameManager
    }
}

# Links :
BoardEngine.ChunkManager -> BoardEngine.World: Load Chunks {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.ChunkManager -> BoardEngine.World: Unload Chunks {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.WorldManager -> BoardEngine.ChunkManager: Update view coordinate {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
GameplayManager.GameManager -> BoardEngine.ChunkManager: Update Player coordinate {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}

```
---
# Summary :
name|description
----|----
[UpdateCoordinate]({{< ref "#updatecoordinate" >}}) | `Update the view position to load new chunks and unload far-away chunk`
[Rerender]({{< ref "#rerender" >}}) | `Force the World to rerender all chunk`

---
# Functions :

---
### UpdateCoordinate
Update the view position to load new chunks and unload far-away chunk

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|New Coordinate
**forceUpdateChunk**|`bool`|Optional (default is False), set to True to force Updating the check even if no movement is made

---
### Rerender
Force the World to rerender all chunk
