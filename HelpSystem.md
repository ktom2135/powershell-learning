help 后面跟着命令，可以得到帮助，
```

help Get-Service

```


help 可以跟随通配符，将列出所有包含关键字的cmdlet, function等
```

help *log*

```


可选参数（包括参数类型）放在中括号中，所有不在中括号中的都是必选参数。


```

help get-eventlog

名称
    Get-EventLog

语法
    Get-EventLog [-LogName] <string> [[-InstanceId] <long[]>]  [<CommonParameters>]

    Get-EventLog  [<CommonParameters>]

    由于[-LogName] <string> 不在中括号中，所以它是必选参数
```

读取文件内容：
```
Get-Content
```
以下将读取hosts文件
```
Get-Content C:\Windows\System32\drivers\etc\hosts
```

从某个文件中取得计算机名，然后读取log,
小括号代表先执行（以数学意义上的小括号为准）
Get-EventLong Application -computer (get-content .)

Q: windows 哪一个命令能够将cmdlet命令的输出转换到html？
A: help html
e.g. 将进行信息输出成Html
ps |  ConvertTo-Html
