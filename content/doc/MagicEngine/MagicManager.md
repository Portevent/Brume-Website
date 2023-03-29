---
title: MagicManager
path: /MagicEngine
alias: 
- Magic Manager
tag: 
- class
---
ManicManager is a class used for processing SpellEffect

![MagicManager](MagicManager.svg "MagicManager")

---
# Summary :
name|description
----|----
[Cast]({{< ref "#cast" >}}) | `Cast a spell on a target`
[CastEffect]({{< ref "#casteffect" >}}) | `Execute a spellEffect`
[ValidateEntity]({{< ref "#validateentity" >}}) | `Check if a SpellEffect is valid on an entity and can be applied on it`
[ValidatePlayerSpellConditions]({{< ref "#validateplayerspellconditions" >}}) | `Check if a Spell can be casted by the player on a target (from player position)`
[ValidateSpellRange]({{< ref "#validatespellrange" >}}) | `Check if a caster can cast a spell from a point to a target (validate range Condition)`
[ValidateSpellConditions]({{< ref "#validatespellconditions" >}}) | `Check if a caster can cast a spell from a point to a target (validate all SpellCondition)`
[ValidateCondition]({{< ref "#validatecondition" >}}) | `Validate a single SpellCondition`

---
# Functions :

---
### Cast
Cast a spell on a target

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell being casted
**caster**|[Entity]({{< ref "Entity" >}})|Entity casting the spell
**origin**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate from which the spell is casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate on which the spell is casted

---
### CastEffect
Execute a spellEffect

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|The spell from which the effect is from
**caster**|[Entity]({{< ref "Entity" >}})|Entity casting the spell
**effect**|[SpellEffect]({{< ref "SpellEffect" >}})|The effect being casted
**origin**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate from which the spell is casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate on which the spell is casted

#### Exceptions
- `ArgumentOutOfRangeException` : 

---
### ValidateEntity
Check if a SpellEffect is valid on an entity and can be applied on it

#### Parameters
name|type|description
-----|-----|-----
**effect**|[SpellEffect]({{< ref "SpellEffect" >}})|SpellEffect being process
**target**|[Entity]({{< ref "Entity" >}})|The targeted entity
**caster**|[Entity]({{< ref "Entity" >}})|The entity casting the SpellEffect (used for criteria like "is an ally")

#### Return
- `bool` : A boolean, true if the entity is valid and this SpellEffect can be applied on it

#### Exceptions
- `ArgumentOutOfRangeException` : unknown Criteria

---
### ValidatePlayerSpellConditions
Check if a Spell can be casted by the player on a target (from player position)

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell intended
**target**|[Coordinate]({{< ref "Coordinate" >}})|Target intended

#### Return
- `bool` : boolean, true if the spell can be cast on that tile

---
### ValidateSpellRange
Check if a caster can cast a spell from a point to a target (validate range Condition)

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell intended
**caster**|[Entity]({{< ref "Entity" >}})|Entity trying to cast the spell
**origin**|[Coordinate]({{< ref "Coordinate" >}})|from which the spell is casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|target where the spell is intended 

#### Return
- `bool` : boolean, true if the spell can be cast on that tile

---
### ValidateSpellConditions
Check if a caster can cast a spell from a point to a target (validate all SpellCondition)

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell intended
**caster**|[Entity]({{< ref "Entity" >}})|Entity trying to cast the spell
**origin**|[Coordinate]({{< ref "Coordinate" >}})|from which the spell is casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|target where the spell is intended 

#### Return
- `bool` : boolean, true if the spell can be cast on that tile

#### Exceptions
- `ArgumentOutOfRangeException` : unknown ConditionOperator

---
### ValidateCondition
Validate a single SpellCondition

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell intended
**condition**|[SpellCondition]({{< ref "SpellCondition" >}})|SpellCondition tested
**caster**|[Entity]({{< ref "Entity" >}})|Entity trying to cast the spell
**origin**|[Coordinate]({{< ref "Coordinate" >}})|from which the spell is casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|target where the spell is intended 

#### Return
- `bool` : boolean, true if the SpellCondition is validated

#### Exceptions
- `InvalidSpellCondition` : the SpellCondition has a format error
- `ArgumentOutOfRangeException` : unknown ConditionType
