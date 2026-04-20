---
title: RuleTile
path: /WorldGeneratorEngine/Tools/ToClean/RuleTile
alias: 
- Rule Tile
tag: 
- struct
---
Rule Tile are tile with a defined orientation  
Quickly documented, to rewrite  

![RuleTile](RuleTile.svg "RuleTile")

---
# Summary :
name|description
----|----
[FromNeighbors]({{< ref "#fromneighbors" >}}) | `Create RuleTile from a list of neighbors`

---
# Functions :

---
### FromNeighbors
Create RuleTile from a list of neighbors

#### Parameters
name|type|description
-----|-----|-----
**neighbors**|`bool[]`|List of the surrounding Tiles
**randomOrientation**|`bool`|For symmetric tiles, set orientation to first possible or random among possibles

#### Return
- [RuleTile]({{< ref "RuleTile" >}}) : RuleTile

#### Exceptions
- `ArgumentOutOfRangeException` : 
