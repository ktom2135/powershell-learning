* 想在启动Powershell的时候加入一些Alias,
#
* 思路：
* * 在PowerShell启动的时候运行一个PS脚本
#
* 查看PowerShell profile
* 
```
   $profile
```
* Value       :  C:\Users\Administrator\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1

* 打开文件，在文件中加入对应PS方法，可以直接在powershell中使用，
* 比如：
* 加入 function .. {cd ..}
* 在PowerShell中输入 .. 可以进入上一级目录
* 

#

* 进一步， 将PowerShell扩展放入一个文件中：
* 比如在 C:\initPS.ps1文件中加入 function .. {cd ..}
* 然后在Microsoft.PowerShell_profile.ps1中加入 . c:\initPS.ps1
* 再次打开PowerShell， 输入 .. 可以看到我们进入了上一级目录

#
issue:
无法加载文件 C:\Users\MN\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1，因为在此系统上禁止运行脚本。

solution:
```
set-ExecutionPolicy RemoteSigned
```