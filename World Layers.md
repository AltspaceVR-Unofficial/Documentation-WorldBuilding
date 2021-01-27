# Teleportation Navigation & Documenting The Layers In AltspaceVR
****
## Introduction
AltspaceVR makes use of the object layer system within Unity to provide additional features to world develoeprs. These include, but are not limited to, the ability to use the teleport tool, and apply lights to the player avatar.

Layers will be documented here as they are found and observed. See [To-Do](#to-do) for current status of this document.

## Adding Layers To Your World
To add a layer listed in this document for use:
1. In the top right of the Unity editor window, click the `Layers` drop down.
2. Select `Edit Layers`.
3. In the **Inspector** pane, scroll down to the relevant layer and label it accordingly.<sup>a</sup>

To add a relevant _Game Object_ to a layer:
1. In the **Scene Editor** pane, select the relevant object.
2. In the **Inspector** pane, beneath the object name, select the `Layer` drop-down.
3. Select the desired layer.

<sup>a</sup> Name does not have to be exact. It just needs to be on the correct layer number and be identifiable.
****
## `Layer 14` • Navigation & Teleportation
Oft referred to as the "NavMesh", this layer allows the horizontal surface of any collider part of it to be navigated upon using the teleport control. Use this on ground surfaces and places designed for standing on.

## `Layer 15` • Player Lighting
_Exact use unknown. Purportedly, any light added to this layer will effect player models. — Check back later._
****
## To-Do
- [x] Document the "Navigation Mesh" layer (`Layer 14`).
- [ ] Document the "Player Lighting" layer (`Layer 15`).
- [ ] Research additional layers available to world developers.
- [ ] Document additional layers available to world developers.
