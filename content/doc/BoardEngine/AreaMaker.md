---
title: AreaMaker
path: /BoardEngine
alias: 
- Area Maker
tag: 
- class
---
Convert Area to Coordinates[]
```d2
# Nodes :
BoardEngine: {
    Area: Area {
       link: Area
    }
    SelectionManager: Selection Manager {
       link: SelectionManager
    }
    Coordinate: Coordinate {
       link: Coordinate
    }
}
MagicEngine: {
    MagicManager: Magic Manager {
       link: MagicManager
    }
}

# Links :
BoardEngine.AreaMaker -> BoardEngine.Coordinate: ...make a list of Coordinate {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.Area -> BoardEngine.AreaMaker: Convert an Area to... {
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.AreaMaker -> MagicEngine.MagicManager: Get Spells' AoE {style.stroke-dash: 3
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}
BoardEngine.AreaMaker -> BoardEngine.SelectionManager: Get Spells' range cast {style.stroke-dash: 3
source-arrowhead: {}
target-arrowhead: {shape: arrow}
}

```
---
# Summary :
name|description
----|----
[GetArea]({{< ref "#getarea" >}}) | `Convert an Area to a list of valid Coordinate`
[CoordinateInPattern]({{< ref "#coordinateinpattern" >}}) | `Check if a coordinate meet the rules of the pattern`
[IsCoordinateValid]({{< ref "#iscoordinatevalid" >}}) | `Check if a coordinate meet the requirement of the pattern.
3 different check are valuated :
- Coordinates in pattern (e.g. the coordinate is on a diagonal or a line for a star pattern)
- Coordinates in minimal range (if the coordinates is beyond the minimal range)
- Coordinates in maximal range (if the coordinates doesn't not exceed the maximal range)`
[CoordinateInMinimalRange]({{< ref "#coordinateinminimalrange" >}}) | `Check if a coordinate is beyond the minimal range of the patten`
[CoordinateInMaxRange]({{< ref "#coordinateinmaxrange" >}}) | `Check if a coordinate is below the maximal range of the patten`

---
# Functions :

---
### GetArea
Convert an Area to a list of valid Coordinate

#### Parameters
name|type|description
-----|-----|-----
**area**|[Area]({{< ref "Area" >}})|Area defining pattern and range
**origin**|[Coordinate]({{< ref "Coordinate" >}})|From where the area come from (used only for "Self" area)
**target**|[Coordinate]({{< ref "Coordinate" >}})|Where to compute the area

#### Return
- `Coordinate[]` : 

---
### CoordinateInPattern
Check if a coordinate meet the rules of the pattern

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|The coordinates to check
**pattern**|`Pattern`|The pattern to use

#### Return
- `bool` : True if the coordinate is inside the pattern shape

---
### IsCoordinateValid
Check if a coordinate meet the requirement of the pattern.
3 different check are valuated :
- Coordinates in pattern (e.g. the coordinate is on a diagonal or a line for a star pattern)
- Coordinates in minimal range (if the coordinates is beyond the minimal range)
- Coordinates in maximal range (if the coordinates doesn't not exceed the maximal range)

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|The coordinates to check
**area**|[Area]({{< ref "Area" >}})|The Area to compare to

#### Return
- `bool` : A boolean:
True if the coordinate is contains within the pattern
False otherwise


---
### CoordinateInMinimalRange
Check if a coordinate is beyond the minimal range of the patten

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|The coordinates to check
**pattern**|`Pattern`|The pattern to use
**minRange**|`int`|Minimum range

#### Return
- `bool` : True if the coordinate is not below the minimal range

---
### CoordinateInMaxRange
Check if a coordinate is below the maximal range of the patten

#### Parameters
name|type|description
-----|-----|-----
**coordinate**|[Coordinate]({{< ref "Coordinate" >}})|The coordinates to check
**pattern**|`Pattern`|The pattern to use
**maxRange**|`int`|Minimum range

#### Return
- `bool` : True if the coordinate is not beyond the maximal range
