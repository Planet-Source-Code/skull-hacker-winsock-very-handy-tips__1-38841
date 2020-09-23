<div align="center">

## Winsock Very Handy Tips \!


</div>

### Description

This code shows all the handy tips of winsock

such as connect until connected if disconnected

close the conenction and a few more bits of winsock code !
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Skull Hacker](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/skull-hacker.md)
**Level**          |Intermediate
**User Rating**    |2.8 (11 globes from 4 users)
**Compatibility**  |VB 6\.0
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/skull-hacker-winsock-very-handy-tips__1-38841/archive/master.zip)





### Source Code

```
Ok in your VB project if you are making any type of program eg. Trojan , Chat Program or what ever in your connect button make sure you have the following code.
If Winsock1.State = 0 Then
Winsock1.RemoteHost = Text1.Text
Winsock1.RemotePort = 1000
Winsock1.Connect
Do Until Winsock1.State = sckConnected
  DoEvents: DoEvents: DoEvents: DoEvents
Loop
End If
Ok lets look at If Winsock1.State = 0 Then
this tells winsock only to go ahead with the
command if winsock isnt connected this way the
crappy all ready conencted error will not come
up.
now look at this bit of code
Do Until Winsock1.State = sckConnected
This tells winsock to keep trying to connect
until connected.
Now in a command button or what ever when you have a button sending some data always put this
code.
If Winsock1.State = 0 Then Label.Caption = "Not Connected"
strdata = "data"
If Winsock1.State = sckConnected Then
Winsock1.SendData strdata
End If
This tells winsock of the state is 0 it will
say you are not connected.
Now lets look at this code.
if winsock1.state = sckClosing then winsock1.close
label.caption = "Disconnected."
That code should be put in form load it tells
winsock if it gets disconnected it will close
and tell a label its disconnected so this will
prevent the gay error were if you get dissed you
can still connect again !
I hope you enjoyed these tips have fun winsock
prgraming i find it very awsome !
```

