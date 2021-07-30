---

category: Notes
type: 'Notes'
url_path: '/dev_notes_vs'
title: 'Dev Notes - Visual Studio'

layout: null
---

### Download and Install Visual Studio Templates for Grasshopper
Needed to compile Grasshopper plug-ins. 
Fairly straightforward, posting the link here so it is easier to find.
* [RhinoCommon and Grasshopper templates for Rhino 7](https://marketplace.visualstudio.com/items?itemName=McNeel.Rhino7Templates)

Older versions:
* [Grasshopper Templates for V6](https://marketplace.visualstudio.com/items?itemName=McNeel.GrasshopperAssemblyforv6)
* [Grasshopper Assembly for V5](https://marketplace.visualstudio.com/items?itemName=McNeel.GrasshopperAssemblyforv5)

### Setting up VSCode for Grasshopper Plug-In Deployment

I wrote a writeup for this. It is here: [Automate Rhino Plugin Deployment](https://i.hongjunwu.com/Automate-Rhino-Plugin-Development)

One who is new to the project should modify the **./CircularConstruction/CircularConstruction-REFERENCE.csproj** to one's own path in the post build events.
Once that is done, rename this file to **CircularConstruction.csproj**. This file will get ignored by Git when committing, pushing, and pulling the repository.
Therefore avoiding the problem of overwriting other people's workspace during collaboration.

### Let Visual Studio Build .gha Instead of .dll

* In its Vanilla state, Visual Studio will build the plug-in in `.dll` by default, but it is not the appropriate format (`.gha`) for Rhino to read and load it.
* To solve this problem, add the following line into `CircularConstruction.csproj`:

```cs
<PropertyGroup>
    ...
    <TargetExt>.gha</TargetExt>
    ...
</PropertyGroup>
```
