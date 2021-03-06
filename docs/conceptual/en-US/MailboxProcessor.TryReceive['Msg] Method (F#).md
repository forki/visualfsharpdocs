# MailboxProcessor.TryReceive<'Msg> Method (F#)

Waits for a message. This will consume the first message in arrival order.

**Namespace/Module Path:** Microsoft.FSharp.Control

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
member this.TryReceive : ?int -> Async<'Msg option>

// Usage:
mailboxProcessor.TryReceive ()
mailboxProcessor.TryReceive (timeout = timeout)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*timeout*
Type: [int](http://msdn.microsoft.com/en-us/library/025d5455-3622-4ea5-9573-3ecbd4ee1375)


An optional timeout in milliseconds. Defaults to -1 which corresponds to **F:System.Threading.Timeout.Infinite**.



**An asynchronous computation ([Async](http://msdn.microsoft.com/en-us/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7) object) that returns the received message or None if the timeout is exceeded.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This method is for use within the body of the agent. Returns **None** if a timeout is given and the timeout is exceeded. This method is for use within the body of the agent. For each agent, at most one concurrent reader may be active, so no more than one concurrent call to [Receive](http://msdn.microsoft.com/en-us/library/46a1d8e6-3906-45c2-9722-0ddab574cc6a), **TryReceive**, [Scan](http://msdn.microsoft.com/en-us/library/e86368a3-4f97-4b51-a487-4c6b5456fcbe) or [TryScan](http://msdn.microsoft.com/en-us/library/05aa6c91-fe9f-4830-a2d7-6dfa5a2ab376) may be active.

**The following example shows how to use TryReceive. If a message is not received within 10 seconds, a timeout occurs and the message ID increments by 1.**
**[!CODE [FsMailboxProcessor#18](../CodeSnippet/VS_Snippets_Fsharp/fsmailboxprocessor/FSharp/fs/program.fs#18)]**
**A sample session follows. Notice that the message number 2 is skipped due to the timeout.**
**Mailbox Processor TestType some text and press Enter to submit a message.Type 'Stop' to close the program.&gt; test1Reply: Message number 0 was received. Message contents: test1&gt; test2Reply: Message number 1 was received. Message contents: test2&gt; test3Reply: Message number 3 was received. Message contents: test3&gt; StopPress Enter to continue.**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.MailboxProcessor&#60;'Msg&#62; Class &#40;F&#35;&#41;](Control.MailboxProcessor%3C%27Msg%3E+Class+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

