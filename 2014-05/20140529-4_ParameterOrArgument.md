![Parameter and Argument](https://dl.dropboxusercontent.com/u/367600/blog_assets/ParameterAndArgument_20140604.png)

今天以前，我不知道答案。現在以後，不能再傻傻分不清了。

Bart De Smet 在《[C# 4.0 Unleashed](http://amzn.to/1lSS9vS)》一書的 Methods 一章提到：

> ... The distinction is quite simple, though. Parameters live on a declaration site, whereas arguments are specified in a call site. 
>
> ... Depending on the angle you approach them, they’re very similar: One makes up the receiving end; the other makes up the sending end.

何時該用 Parameter，何時該用 Argument？就用你當時的「視角」（或者說情境）來分辨：

- 如果是在「寫」 Function/Method，那麼你可能會宣告（或定義）該 Function/Method 的 **parameter**。例：function SayHello accept two **parameters**。
- 如果是「呼叫」 Function/Method，這時就應該說 **argument**。例：pass two **arguments** to function SayHello。

至於中文的表示法，我的建議是，就用英文表達吧。不失真，又不難懂。