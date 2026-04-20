---
title: WorldGenerator
path: /WorldEngine/WorldGenerationEngine
alias: 
- World Generator
tag: 
- class
---
Manage a dictionary of DimensionGenerator mapped by name, so it can generate Dimensions on demand  

![WorldGenerator](WorldGenerator.svg "WorldGenerator")

---
# Summary :
name|description
----|----
[RegisterDimensionsGeneratorsFromCode]({{< ref "#registerdimensionsgeneratorsfromcode" >}}) | `Automatically load dimension generators from a folder`
[CheckForMissingGenerators]({{< ref "#checkformissinggenerators" >}}) | `Small unit test to verify that each dimension name has a dimension manager`
[Generate]({{< ref "#generate" >}}) | `Generate a new Dimension from its name`

---
# Functions :

---
### RegisterDimensionsGeneratorsFromCode
Automatically load dimension generators from a folder

---
### CheckForMissingGenerators
Small unit test to verify that each dimension name has a dimension manager

---
### Generate
Generate a new Dimension from its name

#### Parameters
name|type|description
-----|-----|-----
**dimensionName**|`DimensionName`|Dimension name
**entrance**|[DimensionEntrance]({{< ref "DimensionEntrance" >}})|If specified, will align new dimension entrance with this

#### Return
- [Dimension]({{< ref "Dimension" >}}) : 
