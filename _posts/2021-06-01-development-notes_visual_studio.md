---

category: Notes
type: 'Notes'
url_path: '/dev_notes_vs'
title: 'Dev Notes - Visual Studio'

layout: null
---

### Setting up VSCode for Grasshopper Plug-In Deployment

* I wrote a writeup for this. It is here: [Automate Rhino Plugin Deployment](https://i.hongjunwu.com/Automate-Rhino-Plugin-Development)

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
