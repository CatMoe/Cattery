---
title: 解决Windows11一些非人类问题的办法
date: 2022-06-19 14:32:08
---

## 恢复Windows 10的开始菜单和任务栏
> https://github.com/valinet/ExplorerPatcher
拿走不谢

## 恢复Windows 10的右键菜单
恢复Windows 10的
`reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve`
恢复Windows 11的
`reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /va /f`
以上均需**管理员权限** 更改完成后重启`explorer.exe`即可

