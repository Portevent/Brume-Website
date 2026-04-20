---
title: Dimension
path: /WorldEngine/DimensionEngine
alias: 
- Dimension
tag: 
- class
---
World is divided in multiple layer, called Dimension  
Entities are positioned on a Dimension, and can only interact with other element
on the same Dimension  

![Dimension](Dimension.svg "Dimension")

---
# Summary :
name|description
----|----
[new]({{< ref "#new" >}}) | `The main canvas that entities can pass through`
[AddCanvas]({{< ref "#addcanvas" >}}) | `Adds a canvas to this dimension`
[RemoveCanvas]({{< ref "#removecanvas" >}}) | `Removes a canvas from this dimension`
[GetAdditionalCanvases]({{< ref "#getadditionalcanvases" >}}) | `Gets all canvases except the passable canvas`

---
# Functions :

---
### new
The main canvas that entities can pass through

---
### AddCanvas
Adds a canvas to this dimension

#### Parameters
name|type|description
-----|-----|-----
**dimensionCanvas**|[DimensionCanvas]({{< ref "DimensionCanvas" >}})|The canvas to add
**canvasName**|`string`|Optionnal canvas name

#### Exceptions
- `ArgumentNullException` : Thrown when canvas is null

---
### RemoveCanvas
Removes a canvas from this dimension

#### Parameters
name|type|description
-----|-----|-----
**dimensionCanvas**|[DimensionCanvas]({{< ref "DimensionCanvas" >}})|The canvas to remove

#### Return
- `bool` : True if the canvas was removed, false if it wasn't found

#### Exceptions
- `InvalidOperationException` : Thrown when trying to remove the passable canvas

---
### GetAdditionalCanvases
Gets all canvases except the passable canvas

#### Return
- `IEnumerable<DimensionCanvas>` : Collection of additional canvases
