---
title: AnimationManager
path: /AnimationEngine
alias: 
- Animation Manager
tag: 
- class
---
Register all animations that must be play and process them
Animations are queued as [AnimationData]({{< ref "AnimationData" >}}) object, and animation are played first in first out
If an Entity is not Ready, the current animation will wait for it and thus delay all the other  

![AnimationManager](AnimationManager.svg "AnimationManager")

---
# Summary :
name|description
----|----
[AddAnimation]({{< ref "#addanimation" >}}) | `Queue a new animation`
[ProcessQueue]({{< ref "#processqueue" >}}) | `Process the next animation in the queue`

---
# Functions :

---
### AddAnimation
Queue a new animation

#### Parameters
name|type|description
-----|-----|-----
**animationData**|[AnimationData]({{< ref "AnimationData" >}})|AnimationData to queue

---
### ProcessQueue
Process the next animation in the queue
