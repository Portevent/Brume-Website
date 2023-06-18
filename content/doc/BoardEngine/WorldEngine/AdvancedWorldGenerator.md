---
title: AdvancedWorldGenerator
path: /BoardEngine/WorldEngine
alias: 
- Advanced World Generator
tag: 
- class
---
Scriptable Object that hold [WorldGenerationParameter]({{< ref "WorldGenerationParameter" >}}) used by a semi random procedural world builder.
For a given [Coordinate]({{< ref "Coordinate" >}}), will return a list of Tile.

![AdvancedWorldGenerator](AdvancedWorldGenerator.svg "AdvancedWorldGenerator")

---
# Summary :
name|description
----|----
[Setup]({{< ref "#setup" >}}) | `Setup function called when World is created`
[GetNoiseValue]({{< ref "#getnoisevalue" >}}) | `Generate a value from the parameted noise, that range from Min to Max (or -1 if outside of Noise)`
[GetHeightValue]({{< ref "#getheightvalue" >}}) | `Generate a value from GetNoiseValue, that range from Min to Max (or -1 if outside of Noise)`

---
# Functions :

---
### Setup
Setup function called when World is created

#### Parameters
name|type|description
-----|-----|-----
**world**|[World]({{< ref "World" >}})|Reference to the parent World

#### Exceptions
- `ArgumentOutOfRangeException` : 

---
### GetNoiseValue
Generate a value from the parameted noise, that range from Min to Max (or -1 if outside of Noise)

#### Parameters
name|type|description
-----|-----|-----
**x**|`int`|Coordinate
**y**|`int`|Coordinate

#### Return
- `float` : 

---
### GetHeightValue
Generate a value from GetNoiseValue, that range from Min to Max (or -1 if outside of Noise)

#### Parameters
name|type|description
-----|-----|-----
**x**|`int`|Coordinate
**y**|`int`|Coordinate

#### Return
- `int` : 
