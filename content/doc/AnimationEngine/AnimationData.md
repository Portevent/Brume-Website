---
title: AnimationData
path: /AnimationEngine
alias: 
- Animation Data
tag: 
- struct
---
Structure holding data about an [Entity]({{< ref "Entity" >}}) doing an entityAnimation.
Can hold a list of [Entity]({{< ref "Entity" >}}) to wait for
AnimationData are queued inside [AnimationManager]({{< ref "AnimationManager" >}}), and are resolved one by one
```d2
# Nodes :
AnimationEngine: {
    AnimationManager: Animation Manager {
       link: AnimationManager
    }
}

# Links :
AnimationEngine.AnimationManager -> AnimationEngine.AnimationData: Process {
source-arrowhead: {}
target-arrowhead: Queue of{shape: arrow}
}

```