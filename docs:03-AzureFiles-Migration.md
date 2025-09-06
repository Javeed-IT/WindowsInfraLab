# Azure Files Migration & Drive Mapping

## 1. Create File Share
- Storage Account: stinfrafiles123  
- File Share: itsales  
📸 Screenshot: `azure-files-share.png`

## 2. Copy Local Files to Azure
- Used **AzCopy** to upload D:\Shares\Sales  
- Command:
```powershell
C:\azcopy_windows_amd64_10.30.0\azcopy.exe copy "D:\Shares\Sales\*" "https://stinfrafiles123.file.core.windows.net/itsales?<SAS-TOKEN>" --recursive=true
