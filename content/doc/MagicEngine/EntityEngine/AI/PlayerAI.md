---
title: PlayerAI
path: /MagicEngine/EntityEngine/AI
alias: 
- PlayerAI
tag: 
- class
---
PlayerAI is an IntentAI that listen to InputManager to setup Intent and actually play turn  

![PlayerAI](PlayerAI.svg "PlayerAI")

---
# Summary :
name|description
----|----
[CheckWorldInteraction]({{< ref "#checkworldinteraction" >}}) | `Called when Player move around. If in quest mode, will allow interaction with WorldInteractionAction`
[PathFindTo]({{< ref "#pathfindto" >}}) | `PathFindToward a destination
Called by DeckManager`

---
# Functions :

---
### CheckWorldInteraction
Called when Player move around. If in quest mode, will allow interaction with WorldInteractionAction

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|Coordinates

---
### PathFindTo
PathFindToward a destination
Called by DeckManager

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|
