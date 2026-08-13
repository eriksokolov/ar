vi:
  Set-PSreadlineoption -editmode vi
custom keyboard layout list:
  $list = Get-WinUserLanguageList; $list.Clear(); $list.Add("de-DE"); $list.Add("ru-RU"); Set-WinUserLanguageList $list -Force
