EditMode Vi:
  Set-PSreadlineoption -editmode vi
Keyboard Layout:
  $list = Get-WinUserLanguageList; $list.Clear(); $list.Add("de-DE"); $list.Add("ru-RU"); Set-WinUserLanguageList $list -Force
Set German Time:
  Set-TimeZone -id "W. Europe Standard Time"
Local Only:
  start ms-cxh:localonly
User Shell Folders:
  Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\User Shell Folders
  Screenshot String Value:
    {B7BEDE81-DF94-4682-A7D8-57A52620B86F}
Boot UpTime:
  (get-ciminstance win32_operatingsystem).lastbootuptime
Password LastSet:
  Properties -> attributeditor -> pwlastset
UX Windows Update:
  Computer\hkey_local_machine\software\Policies\Microsoft\Windows\WindowsUpdate
ScreenClip:
  start-process explorer.exe „ms-screenclip:“
Part of Domain:
  (get-ciminstance win32_computersystem).partofdomain
AD Query Window:
  rundll32.exe dsquery.dll,OpenQueryWindow
GP Html File:
  gpresult /h .\gp.html
SerialNumber:
  (Get-Ciminstance Win32_Bios).Serialnumber
Terminalserver License Manager:
  licmgr.exe
Windows Console Host:
  conhost.exe
Print Manager:
  printmanagement.msc
Check SecureBoot On Uefi Computers:
  reg query "HKLM\SYSTEM\CurrentControlSet\Control\SecureBoot\State" /v UEFISecureBootEnabled
Graphics Recovery:
  Win + Ctrl + Shift + B
No Lockscreen:
  Create Key:
    Computer\HKEY_local_machine\Software\Policies\Microsoft\Windows\Personalization
    Create Dword:
      NoLockScreen
      Change Value:
        0x1
AutoLogin:
  Create Key:  
    Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
    Create DataType:
      DefaultPassword
      Change Value
Chromium Import Export Ergonomic Link:
  chrome://bookmarks/
Disable WindowsSearch:
  sc config WSearch start= disabled
