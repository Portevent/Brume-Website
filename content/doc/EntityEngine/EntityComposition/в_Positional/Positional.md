---
title: Positional
path: /EntityEngine/EntityComposition/в_Positional
alias: 
- Positional
tag: 
- class
---
Positional is a MonoBehaviour object that has a Coordinate and a Dimension  
It can be moved, and will raise PositionnableEvent  

![Positional](Positional.svg "Positional")

---
# Summary :
name|description
----|----
[SilentlyMove]({{< ref "#silentlymove" >}}) | `Change the coordinate without raising an OnMove event`

---
# Functions :

---
### SilentlyMove
Change the coordinate without raising an OnMove event

#### Parameters
name|type|description
-----|-----|-----
**newCoordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate
