---
title: QuickPainter
path: /WorldGeneratorEngine/Tools
alias: 
- Quick Painter
tag: 
- class
---
Helper class to operate on DimensionCanvases  

![QuickPainter](QuickPainter.svg "QuickPainter")

---
# Summary :
name|description
----|----
[Picker]({{< ref "#picker" >}}) | `Select all Coordinates that match color from a given position`

---
# Functions :

---
### Picker
Select all Coordinates that match color from a given position

#### Parameters
name|type|description
-----|-----|-----
**canvas**|[DimensionCanvas]({{< ref "DimensionCanvas" >}})|Canvas
**from**|[Coordinate]({{< ref "Coordinate" >}})|Origin of zone
**color**|`Color`|Color that must match (if none, use the color of source)

#### Return
- `HashSet<Coordinate>` : 
