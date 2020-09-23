<div align="center">

## Hide your program in the Ctrl\-Alt\-Delete Dialog\!


</div>

### Description

Always wanted to hide your program in Ctrl-Alt-Delete Dialog box, So people dont close it from there when you dont want them to....Well use this code and your problems will be solved...They cannot close your program unless you let them through yours...MUST HAVE!!!!
 
### More Info
 
Create a Module and put the code below and call the Subs like...        Show_Program_In_CTRL_ALT_DELETE , And Hide_Program_In_CTRL-ALT-DELETE

Hides your Program in the Ctrl-Alt-Delete...not permanently...


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Neo](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/neo.md)
**Level**          |Unknown
**User Rating**    |4.8 (91 globes from 19 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/neo-hide-your-program-in-the-ctrl-alt-delete-dialog__1-2393/archive/master.zip)





### Source Code

```
' ----Api Declares for this code
Public Declare Function GetCurrentProcessId Lib "kernel32" () As Long
Public Declare Function RegisterServiceProcess Lib "kernel32" (ByVal dwProcessID As Long, ByVal dwType As Long) As Long
' ----Public Declares for this code
Public Const RSP_SIMPLE_SERVICE = 1
Public Const RSP_UNREGISTER_SERVICE = 0
' ----What makes it invisible/visible in Ctrl-alt-delete
' Note: That if you run this program from your development
'    enviorment(VB) you will not see your development
'    enviorment(VB) or your programs name in the
'    Ctrl-Alt-Delete Dialog.
'    From AciD email Me at Buckwheat9@juno.com
Public Sub Hide_Program_In_CTRL_ALT_Delete()
Dim pid As Long
Dim reserv As Long
pid = GetCurrentProcessId()
regserv = RegisterServiceProcess(pid, RSP_SIMPLE_SERVICE)
End Sub
Public Sub Show_Program_In_CTRL_ALT_DELETE()
Dim pid As Long
Dim reserv As Long
pid = GetCurrentProcessId()
regserv = RegisterServiceProcess(pid, RSP_UNREGISTER_SERVICE)
End Sub
```

