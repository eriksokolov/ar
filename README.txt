vi:
  Set-PSreadlineoption -editmode vi
german + ru keyboard layout:
  $list = Get-WinUserLanguageList; $list.Clear(); $list.Add("de-DE"); $list.Add("ru-RU"); Set-WinUserLanguageList $list -Force
Set German Time:
  Set-TimeZone -id "W. Europe Standard Time"
