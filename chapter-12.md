# A practical interlude

1) Create a directory called LABS and share it, make sure that the share permissions are set so that Everyone has read/write access, and local Administrators have full control. Set the caching mode for documents since this is for file primarily.
```powershell
new-item -ItemType Directory C:\Users\martin\Desktop\LABS | Out-Null
```
```powershell
Import-Module SmbShare
```
```powershell
$sharefolder = New-SmbShare -Name LABS -Path C:\Users\martin\Desktop\LABS -ChangeAccess Everyone -FullAccess Administrators -CachingMode Documents
```
```powershell
$sharefolder | Get-SmbShareAccess
```
