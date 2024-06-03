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

![EntityManager](EntityManager.svg "EntityManager")

---
# Summary :
name|description
----|----
[ClearEvent]({{< ref "#clearevent" >}}) | `Setup the class, removing the listener on events`
[GetEntity]({{< ref "#getentity" >}}) | `Return Entity at coordinate`
[GetEntities]({{< ref "#getentities" >}}) | `Return all registered Entites`
[RegisterEntity]({{< ref "#registerentity" >}}) | `Add a new entity to the board`
[CellFree]({{< ref "#cellfree" >}}) | `Check if a cell contains no entity`
[CellOccupied]({{< ref "#celloccupied" >}}) | `Check if a cell contains an entity`
[MoveEntity]({{< ref "#moveentity" >}}) | `Move an Entity toward a Cell. Will check if destination cell is free, and will return a failing Movement if not.
Will also trigger animation move to`
[MoveEntity]({{< ref "#moveentity" >}}) | `Move an Entity from a Cell toward another Cell. Will check if "from" cell is occupied,
and if destination cell is free, and will return a failing Movement if not.
Will also trigger animation move to`
[TpEntity]({{< ref "#tpentity" >}}) | `Tp an Entity to a Cell.
Will Trigger animation tp to, and also trigger a Telefrag if target cell is occupied.`
[TpEntity]({{< ref "#tpentity" >}}) | `Tp an Entity from a Cell to another Cell.
Will Trigger animation tp to, and also trigger a Telefrag if target cell is occupied.`
[Kill]({{< ref "#kill" >}}) | `Kill an Entity`
[Unregister]({{< ref "#unregister" >}}) | `Remove an Entity from the game (remove it from EntityManager, delete its gameobject)`
[Summons]({{< ref "#summons" >}}) | `Create an Entity linked to a summoner's spell`
[CreateEntity]({{< ref "#createentity" >}}) | `Create an Entity`
[InstantiateGameObject]({{< ref "#instantiategameobject" >}}) | `Instantiate a Gameobject linked to an entityName`
[UpdateEntityCoordinate]({{< ref "#updateentitycoordinate" >}}) | `Update an Entity coordinate, without animating`

---
# Functions :

---
### ClearEvent
Setup the class, removing the listener on events

---
### GetEntity
Return Entity at coordinate

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate

#### Return
- [Entity]({{< ref "Entity" >}}) : Entity or null

---
### GetEntities
Return all registered Entites

#### Return
- `List<Entity>` : Entity list

---
### RegisterEntity
Add a new entity to the board

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to register
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|Coordiantes

---
### CellFree
Check if a cell contains no entity

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|Cell to check

#### Return
- `bool` : Boolean

---
### CellOccupied
Check if a cell contains an entity

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|Cell to check

#### Return
- `bool` : Boolean

---
### MoveEntity
Move an Entity toward a Cell. Will check if destination cell is free, and will return a failing Movement if not.
Will also trigger animation move to

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to move to
**to**|[Coordinate]({{< ref "Coordinate" >}})|Destination

#### Return
- [Movement]({{< ref "Movement" >}}) : Movement which correspond to the result of the function : NoDestination, Obstructed or Success

---
### MoveEntity
Move an Entity from a Cell toward another Cell. Will check if "from" cell is occupied,
and if destination cell is free, and will return a failing Movement if not.
Will also trigger animation move to

#### Parameters
name|type|description
-----|-----|-----
**from**|[Coordinate]({{< ref "Coordinate" >}})|From
**to**|[Coordinate]({{< ref "Coordinate" >}})|Destination

#### Return
- [Movement]({{< ref "Movement" >}}) : Movement which correspond to the result of the function :
NoEntity, NoDestination, Obstructed or Success

---
### TpEntity
Tp an Entity to a Cell.
Will Trigger animation tp to, and also trigger a Telefrag if target cell is occupied.

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to tp to
**to**|[Coordinate]({{< ref "Coordinate" >}})|Destination

#### Return
- [Movement]({{< ref "Movement" >}}) : Movement which correspond to the result of the function :
NoDestination, Telefrag or Success

---
### TpEntity
Tp an Entity from a Cell to another Cell.
Will Trigger animation tp to, and also trigger a Telefrag if target cell is occupied.

#### Parameters
name|type|description
-----|-----|-----
**from**|[Coordinate]({{< ref "Coordinate" >}})|From
**to**|[Coordinate]({{< ref "Coordinate" >}})|Destination

#### Return
- [Movement]({{< ref "Movement" >}}) : Movement which correspond to the result of the function :
NoDestination, Telefrag or Success

---
### Kill
Kill an Entity

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity

---
### Unregister
Remove an Entity from the game (remove it from EntityManager, delete its gameobject)

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to unregister
**checkSummoner**|`bool`|Set this to false to not check if the entity is summoned by another one. Will cause issue if properly set to false

---
### Summons
Create an Entity linked to a summoner's spell

#### Parameters
name|type|description
-----|-----|-----
**summoner**|[Entity]({{< ref "Entity" >}})|Entity summoning
**spell**|[Spell]({{< ref "Spell" >}})|Summons linked to spell
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate where to summon
**entityName**|`string`|Entity to summon

#### Return
- [Entity]({{< ref "Entity" >}}) : Return the summoned entity

---
### CreateEntity
Create an Entity

#### Parameters
name|type|description
-----|-----|-----
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate where to create
**entityName**|`string`|Entity to summon
**checkCell**|`bool`|Verify if cell exist and is free

#### Return
- [Entity]({{< ref "Entity" >}}) : Return the created entity

---
### InstantiateGameObject
Instantiate a Gameobject linked to an entityName

#### Parameters
name|type|description
-----|-----|-----
**entityName**|`string`|Entity to Instantiate
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate to create to

#### Return
- [Entity]({{< ref "Entity" >}}) : Return the instantiated entity

---
### UpdateEntityCoordinate
Update an Entity coordinate, without animating

#### Parameters
name|type|description
-----|-----|-----
**entity**|[Entity]({{< ref "Entity" >}})|Entity to update
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|coordinate
