vi:
  Set-PSreadlineoption -editmode vi
german + ru keyboard layout:
  $list = Get-WinUserLanguageList; $list.Clear(); $list.Add("de-DE"); $list.Add("ru-RU"); Set-WinUserLanguageList $list -Force
Set German Time:
  Set-TimeZone -id "W. Europe Standard Time"
#:
  < > | ‘
localonly:
  start ms-cxh:localonly
User Shell Folders:
  Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\User Shell Folders
  Screenshot String Value:
    {B7BEDE81-DF94-4682-A7D8-57A52620B86F}
