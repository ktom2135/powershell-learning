

```
function Rider {
    $rider = Get-ChildItem -Path 'C:\Program Files\JetBrains\*\bin\rider64.exe' | Select-Object -First 1
    &$rider (Get-ChildItem -Path *.sln | Select-Object -First 1)
}
```
```
function WebStorm {
    $webstorm = Get-ChildItem -Path 'C:\Program Files\JetBrains\*\bin\webstorm64.exe' | Select-Object -First 1
    &$webstorm .
}

```