---

category: Notes
type: 'Notes'
url_path: '/dev_notes_release'
title: 'Dev Notes - Release'

layout: null
---

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