---
title: DimensionCanvas
path: /WorldEngine/CanvasEngine
alias: 
- Dimension Canvas
tag: 
- class
---
Canvas are a set of Coordinate linking to Cell (color and tile)  

![DimensionCanvas](DimensionCanvas.svg "DimensionCanvas")

---
# Summary :
name|description
----|----
[GetCell]({{< ref "#getcell" >}}) | `Get Cell`
[GetCell]({{< ref "#getcell" >}}) | `Get Cell`
[CellExists]({{< ref "#cellexists" >}}) | `Check if Cell exists`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell (use default creator)`
[SetCell]({{< ref "#setcell" >}}) | `Set Cell (use default creator)`
[RemoveCell]({{< ref "#removecell" >}}) | `Remove Cell`
[UpdateCell]({{< ref "#updatecell" >}}) | `Called when a Cell Color or Till is updated`
[OnNewCell]({{< ref "#onnewcell" >}}) | `Called when a new Cell is created`
[GetAllCells]({{< ref "#getallcells" >}}) | `Return all Cells`
[Clear]({{< ref "#clear" >}}) | `Clear all Cells`
[GetDefaultCell]({{< ref "#getdefaultcell" >}}) | `Create a Default Cell for when only color is specified`

---
# Functions :

---
### GetCell
Get Cell

#### Parameters
name|type|description
-----|-----|-----
**position**|`Vector3Int`|position

#### Return
- [Cell]({{< ref "Cell" >}}) : Cell

---
### GetCell
Get Cell

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate

#### Return
- [Cell]({{< ref "Cell" >}}) : Cell

---
### CellExists
Check if Cell exists

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate

#### Return
- `bool` : Bool

---
### SetCell
Set Cell

#### Parameters
name|type|description
-----|-----|-----
**position**|`Vector3Int`|position
**cell**|[Cell]({{< ref "Cell" >}})|Cell

---
### SetCell
Set Cell

#### Parameters
name|type|description
-----|-----|-----
**position**|`Vector3Int`|position
**tilebase**|`TileBase`|Tilebase

---
### SetCell
Set Cell

#### Parameters
name|type|description
-----|-----|-----
**position**|`Vector3Int`|position
**tilebase**|`TileBase`|Tilebase
**color**|`Color`|Color

---
### SetCell
Set Cell

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate
**tilebase**|`TileBase`|Tilebase

---
### SetCell
Set Cell (use default creator)

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate
**cell**|[Cell]({{< ref "Cell" >}})|Cell

---
### SetCell
Set Cell (use default creator)

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate
**color**|`Color`|color

---
### RemoveCell
Remove Cell

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate

---
### UpdateCell
Called when a Cell Color or Till is updated

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate of cell
**cell**|[Cell]({{< ref "Cell" >}})|Cell updated

---
### OnNewCell
Called when a new Cell is created

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate of cell
**cell**|[Cell]({{< ref "Cell" >}})|Cell created

---
### GetAllCells
Return all Cells

#### Return
- `List<Cell>` : Cells

---
### Clear
Clear all Cells

---
### GetDefaultCell
Create a Default Cell for when only color is specified

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate
**color**|`Color`|Color

#### Return
- [Cell]({{< ref "Cell" >}}) : Cell
