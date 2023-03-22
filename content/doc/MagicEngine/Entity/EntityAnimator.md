---
title: EntityAnimator
slug: EntityAnimator
alias: 
- Entity Animator
tag: 
- class
---
An EntityAnimator represent the state in which an Entity is for the animation\
The main parameter of an EntityAnimator is a boolean : ready\
This indicate to the AnimationManager whether this is Entity is idle and ready to make an animation, or busy doing\
one yet.
Everytime "ready" change, AnimationManager.ProcessQueue() is called to check the next animation

---
# Summary :
name|description
----|----
[ApplyMoveTo]({{< ref "#applymoveto" >}}) | `Try to move toward MoveTo`
[TpTo]({{< ref "#tpto" >}}) | `Teleport to destination while playing the Tp Animation`
[BlinkTo]({{< ref "#blinkto" >}}) | `Teleport to destination without playing any animation`
[Cast]({{< ref "#cast" >}}) | `Call the Cast animation`
[Hurt]({{< ref "#hurt" >}}) | `Call the Hurt animation`
[PrepareTp]({{< ref "#preparetp" >}}) | `Call the PrepareTp animation`
[AnimationEnd]({{< ref "#animationend" >}}) | `Called by EntityAnimatorEvent when the animator want to notify its animation is ended`

---
### ApplyMoveTo
Try to move toward MoveTo

---
### TpTo
Teleport to destination while playing the Tp Animation

#### Parameters
name|type|description
-----|-----|-----
**animationTarget**|[Coordinate]({{< ref "Coordinate" >}})|Destination where to Tp

---
### BlinkTo
Teleport to destination without playing any animation

#### Parameters
name|type|description
-----|-----|-----
**animationTarget**|[Coordinate]({{< ref "Coordinate" >}})|Destination where to Tp

---
### Cast
Call the Cast animation

---
### Hurt
Call the Hurt animation

---
### PrepareTp
Call the PrepareTp animation

---
### AnimationEnd
Called by EntityAnimatorEvent when the animator want to notify its animation is ended
