---
title: ChunkManager
path: /BoardEngine
alias: 
- Chunk Manager
tag: 
- class
---
Linked to a [World]({{< ref "World" >}}), generate and unload world part as the player moves around
![ChunkManager.svg]({{< ref "ChunkManager.svg" >}})

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
