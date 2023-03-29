---
title: EntityManager
path: /MagicEngine/EntityEngine
alias: 
- Entity Manager
tag: 
- class
---
Keep track of all [Entity]({{< ref "Entity" >}}), and register / unregister them as needed.
Entity Manager also move [Entity]({{< ref "Entity" >}}) around using [BoardManager]({{< ref "BoardManager" >}}) to determine if a cell exist and can be used. The main task of Entity Manager is handling when two [Entity]({{< ref "Entity" >}}) need to switch places.
Every displacement generate a [Movement]({{< ref "Movement" >}})
It is also where [Entity]({{< ref "Entity" >}}) are instancied.
![EntityManager.svg]({{< ref "EntityManager.svg" >}})

---
# Summary :
name|description
----|----
[Unregister]({{< ref "#unregister" >}}) | `Remove an Entity from the game (remove it from EntityManager, delete its gameobject)`

---
# Functions :

---
### Unregister
Remove an Entity from the game (remove it from EntityManager, delete its gameobject)

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to unregister
**checkSummoner**|`bool`|Set this to false to not check if the entity is summoned by another one. Will cause issue if properly set to false
