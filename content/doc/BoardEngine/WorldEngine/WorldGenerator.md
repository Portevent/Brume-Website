---
title: WorldGenerator
path: /BoardEngine/WorldEngine
alias: 
- World Generator
tag: 
- class
---
Abstract class that define the base of a WorldGenerator as a Scriptable Object.
For a given [Coordinate]({{< ref "Coordinate" >}}), will return a list of Tile.  

![WorldGenerator](WorldGenerator.svg "WorldGenerator")

---
# Summary :
name|description
----|----
[Rebuild]({{< ref "#rebuild" >}}) | `Return the number of tilemaps required for this world`
[Setup]({{< ref "#setup" >}}) | `Setup function called when World is created`

---
# Functions :

---
### Rebuild
Return the number of tilemaps required for this world

---
### Setup
Setup function called when World is created

#### Parameters
name|type|description
-----|-----|-----
**world**|[World]({{< ref "World" >}})|Reference to the parent World
