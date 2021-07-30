---

category: Notes
type: 'Notes'
url_path: '/dev_notes'
title: 'Developer Notes'

layout: null
---

This portion is some notes and quick solutions that occurred during development and worthwhile to jog down.

# Jekyll
### Documentation for this website's template:
> [Carte Documentation](https://github.com/Wiredcraft/carte)

### Running jekyll on your localhost:

> `bundle exec jekyll serve`

### Building this documentation and upload to Github pages:

> `bundle exec jekyll build --destination docs/`


# Visual Studio
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