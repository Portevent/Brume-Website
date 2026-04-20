---
title: EntityRegistry
path: /EntityEngine/EntityManagement
alias: 
- Entity Registry
tag: 
- class
---
Keep track of all [Positional]({{< ref "Positional" >}}), and register / unregister them as needed  

![EntityRegistry](EntityRegistry.svg "EntityRegistry")

---
# Summary :
name|description
----|----
[Register]({{< ref "#register" >}}) | `Register Positional`
[Unregister]({{< ref "#unregister" >}}) | `Unregister Positional`
[TryGet]({{< ref "#tryget" >}}) | `Get Positional at coordinate (or null)`
[Get]({{< ref "#get" >}}) | `Get Positional`
[GetAllInAllDimensions]({{< ref "#getallinalldimensions" >}}) | `Check if a cell contains a Positional`

---
# Functions :

---
### Register
Register Positional

---
### Unregister
Unregister Positional

---
### TryGet
Get Positional at coordinate (or null)

#### Return
- [Entity]({{< ref "Entity" >}}) : Positional or null

---
### Get
Get Positional

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|`DimensionCoordinate`|DimensionCoordinate

#### Return
- [Entity]({{< ref "Entity" >}}) : Positional

#### Exceptions
- `InvalidOperationException` : 

---
### GetAllInAllDimensions
Check if a cell contains a Positional

#### Return
- `IReadOnlyList<Entity>` : Boolean
