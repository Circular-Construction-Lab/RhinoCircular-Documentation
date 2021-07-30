---

category: Usage
type: 'USAGE'
url_path: '/usage'
title: 'Setup RhinoCircular'

layout: null
---

This post will talk about setting up RhinoCircular.

## System requirements

RhinoCircular is developed on:
* Windows 10 and 11
* Rhino 7
* Visual Studio 2019

RhinoCircular is fully supported for:
* Windows 10 and 11
* Rhino 6 and 7 

## About the CircularConstruction Binary

The standard release package for RhinoCircular is a file called **CircularConstruction.gha**.

The newest information for RhinoCircular will be updated here once we release a beta version of RhinoCircular. 


## Most Recent Release
Version: 0.00.20210730    
Download Binary: [Download](https://circular-construction-lab.github.io/RhinoCircular-Documentation/)    
Check Sum MD5: 000000000000000000000000000000000000000    

Release Notes:    
Currently we will put temporary placeholders here.

## Install
Before you install, you might want to check whether the binary you downloaded is original and complete.
This reduces the risk of installing broken plug-in caused by internet issues during download, or plug-in that is maliciously changed by others.
Just follow this article: [How To: How and when to use CheckSum (MD5)](https://support.esri.com/en/technical-article/000020408)

There is a directory that Rhino and Grasshopper can see and load Grasshopper plug-ins.
To find this directory, first open up Grasshopper from Rhino, then go to **Special Folders- Component Folder**.

<img src="img/development-notes/gh_special_folders_comp_folder.png" alt="drawing" width="1200"/>

A folder most likely located in **C:\Users\YOUR_USER_NAME\AppData\Roaming\Grasshopper\Libraries** will open. 
This is the place where Grasshopper loads all its plug-ins.

With a peace of mind that your copy of RhinoCircular is original, we can proceed to install.
Drag the **CircularConstruction.gha** into this directory and restart Rhino.
Re-open Grasshopper, and you should be all set.