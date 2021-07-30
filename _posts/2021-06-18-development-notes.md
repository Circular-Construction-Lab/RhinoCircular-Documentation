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

# Release
### Generate MD5 Checksum
Adding MD5 checksum ensures clients receive binaries undamaged and untempered.
Click **Read More**  to expand instructions.

{::options parse_block_html="true" /}
<details>
<summary markdown="span">Read More</summary>

Original Article: [How To: How and when to use CheckSum (MD5)](https://support.esri.com/en/technical-article/000020408)

1. Open Windows PowerShell from the Windows menu.
![Image](https://s3-us-west-2.amazonaws.com/ist-app-support-files/000020408/00N39000003LL2C-0EMf2000000FWqG.png)
   
2. Type command: `Get-FileHash`
![Image](https://s3-us-west-2.amazonaws.com/ist-app-support-files/000020408/00N39000003LL2C-0EMf2000000FWu8.png)
   
3. Drag and drop the file to be verified from the local directory into the PowerShell window. If the file is stored on a network drive, open the file directory either via a UNC path or a mapped letter drive in Windows File Explorer, then drag and drop the file into the PowerShell window as shown below. In this example, the ArcGIS Pro 2.3 executable file is used.
![Image](https://s3-us-west-2.amazonaws.com/ist-app-support-files/000020408/00N39000003LL2C-0EMf2000000FWqV.png)
   
4. After the filename, press the spacebar and enter -Algorithm MD5 to ensure the MD5 algorithm is used. An example of the final command is displayed below, where <filepath> is the full path of the file. In this example, the path is 'C:\arcgis\ArcGISPro_23_167023.exe'.
> Get-FileHash <filepath> -Algorithm MD5

5. Press Enter. The output is the checksum value using the MD5 algorithm.
![Image](https://s3-us-west-2.amazonaws.com/ist-app-support-files/000020408/00N39000003LL2C-0EMf2000000FWuI.png)

</details>
{::options parse_block_html="false" /}