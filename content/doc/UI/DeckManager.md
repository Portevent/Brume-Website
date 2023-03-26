---
title: DeckManager
path: /UI
alias: 
- Deck Manager
tag: 
- class
---
A DeckManager link the player Grimoire to the UI and the GameController
It is in charged of understand the user intents, cast spell or move when need
```d2
# Nodes :
BoardEngine: {
    Coordinate: Coordinate
}

# Links :
BoardEngine.Coordinate -- UI.DeckManager: {style.stroke-dash: 3}

```
---
# Summary :
name|description
----|----
[Setup]({{< ref "#setup" >}}) | `Setup all spells in the grimoire inside handSpells.
Setup the Onclick listener for click on tile`
[ApplyCooldown]({{< ref "#applycooldown" >}}) | `Apply the`
[OnClick]({{< ref "#onclick" >}}) | `Execute actions when a cell is clicked. It can be either casting a spell or moving toward`

---
# Functions :

---
### Setup
Setup all spells in the grimoire inside handSpells.
Setup the Onclick listener for click on tile

---
### ApplyCooldown
Apply the

---
### OnClick
Execute actions when a cell is clicked. It can be either casting a spell or moving toward

#### Parameters
name|type|description
-----|-----|-----
**clickedTile**|[Coordinate]({{< ref "Coordinate" >}})|The coordinate of the clickedTile
