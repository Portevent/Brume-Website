---
title: World
path: /BoardEngine/WorldEngine
alias: 
- World
tag: 
- class
---
Hold information about a Biome
Use a [WorldGenerator]({{< ref "WorldGenerator" >}}) to feed it with tile  

![World](World.svg "World")

---
# Summary :
name|description
----|----
[AddWorldInteractiveElement]({{< ref "#addworldinteractiveelement" >}}) | `Add a World Interactive Element to this world and register all the tiles from which it is accessible`
[RemoveWorldInteractiveElement]({{< ref "#removeworldinteractiveelement" >}}) | `Remove a World Interactive Element from this world and unregister all the tiles from which it was accessible`

---
# Functions :

---
### AddWorldInteractiveElement
Add a World Interactive Element to this world and register all the tiles from which it is accessible

#### Parameters
name|type|description
-----|-----|-----
**element**|`WorldInteractiveElement`|Element to register

---
### RemoveWorldInteractiveElement
Remove a World Interactive Element from this world and unregister all the tiles from which it was accessible

#### Parameters
name|type|description
-----|-----|-----
**element**|`WorldInteractiveElement`|Element to unregister
