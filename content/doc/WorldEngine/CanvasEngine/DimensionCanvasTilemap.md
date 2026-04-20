---
title: DimensionCanvasTilemap
path: /WorldEngine/CanvasEngine
alias: 
- Dimension Canvas Tilemap
tag: 
- class
---
CanvasTilemap are Canvas that are linked to a tilemap  

![DimensionCanvasTilemap](DimensionCanvasTilemap.svg "DimensionCanvasTilemap")

---
# Summary :
name|description
----|----
[RegisterTilemap]({{< ref "#registertilemap" >}}) | `Register current tilemap and make it visible`
[UnregisterTilemap]({{< ref "#unregistertilemap" >}}) | `Unregister current Tilemap and make it less visible`
[DisplayAllCell]({{< ref "#displayallcell" >}}) | `Display all cells on Tilemap`
[UpdateCell]({{< ref "#updatecell" >}}) | `Specification of UpdateCell to update Tilemap`
[OnNewCell]({{< ref "#onnewcell" >}}) | `On new cell, display it on the tilemap`
[ToChangeData]({{< ref "#tochangedata" >}}) | `Convert all Cells to ChangeData for bulk Tilemap edit`
[UpdateBoardFromTilemapEvent]({{< ref "#updateboardfromtilemapevent" >}}) | `Convert Tilemap event to changes among Cell`
[ImportTilemap]({{< ref "#importtilemap" >}}) | `Import data from Unity Tilemap`

---
# Functions :

---
### RegisterTilemap
Register current tilemap and make it visible

---
### UnregisterTilemap
Unregister current Tilemap and make it less visible

---
### DisplayAllCell
Display all cells on Tilemap

---
### UpdateCell
Specification of UpdateCell to update Tilemap

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|
**cell**|[Cell]({{< ref "Cell" >}})|

---
### OnNewCell
On new cell, display it on the tilemap

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate
**cell**|[Cell]({{< ref "Cell" >}})|Cell

---
### ToChangeData
Convert all Cells to ChangeData for bulk Tilemap edit

#### Return
- `TileChangeData[]` : TileChangeData[]

---
### UpdateBoardFromTilemapEvent
Convert Tilemap event to changes among Cell

#### Parameters
name|type|description
-----|-----|-----
**updatedTilemap**|`Tilemap`|Tilemap that raise the events
**tiles**|`Tilemap.SyncTile[]`|Events

---
### ImportTilemap
Import data from Unity Tilemap

#### Parameters
name|type|description
-----|-----|-----
**newTilemap**|`Tilemap`|Tilemap
