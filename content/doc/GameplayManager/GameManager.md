---
title: GameManager
path: /GameplayManager
alias: 
- Game Manager
tag: 
- class
---
Keep track of the Player

![GameManager](GameManager.svg "GameManager")

---
# Summary :
name|description
----|----
[PlayerCastSpell]({{< ref "#playercastspell" >}}) | `Invoked when a spell is casted by the player. Delegate the effects application to MagicManager`
[OnTelefrag]({{< ref "#ontelefrag" >}}) | `When a telefrag is generated, cast the Telefrag spell from the DeckManager`
[PassTurn]({{< ref "#passturn" >}}) | `Called when the player pass its turn`
[UpdateDestinationGlyph]({{< ref "#updatedestinationglyph" >}}) | `Set a Glyph on the destination to indicate the user its entity will move there`

---
# Functions :

---
### PlayerCastSpell
Invoked when a spell is casted by the player. Delegate the effects application to MagicManager

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell casted
**target**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate where the spell is casted

---
### OnTelefrag
When a telefrag is generated, cast the Telefrag spell from the DeckManager

#### Parameters
name|type|description
-----|-----|-----
**movement**|[Movement]({{< ref "Movement" >}})|The telefrag Movement

---
### PassTurn
Called when the player pass its turn

---
### UpdateDestinationGlyph
Set a Glyph on the destination to indicate the user its entity will move there

#### Parameters
name|type|description
-----|-----|-----
**coordinates**|[Coordinate]({{< ref "Coordinate" >}})|Coordinate where the player is going
