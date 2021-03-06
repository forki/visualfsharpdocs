# Async.OnCancel Method (F#)

Generates a scoped, cooperative cancellation handler for use within an asynchronous workflow.

**Namespace/Module Path:** Microsoft.FSharp.Control

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
static member OnCancel : (unit -> unit) -> Async<IDisposable>

// Usage:
Async.OnCancel (interruption)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*interruption*
Type: [unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**-&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


The function that is executed on the thread performing the cancellation.



**An asynchronous computation that triggers the interruption if it is cancelled before being disposed.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
For example, the following code generates an asynchronous computation where, if a cancellation happens any time during the execution of the asynchronous computation in the scope of **holder**, then action **interruption** is executed on the thread that is performing the cancellation. This can be used to arrange for a computation to be asynchronously notified that a cancellation has occurred, for example, by setting a flag, or deregistering a pending I/O action.


```f#
async { use! holder = Async.OnCancel interruption ... }
```
**The following code example demonstrates the use of Async.OnCancel.**
**[!CODE [FsAsyncAPIs#8](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis/FSharp/fs/program.fs#8)]**
**Output**
**Started computations.**
**Sending cancellation signal.**
**Canceling operation.**
**Canceling operation.**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Async Class &#40;F&#35;&#41;](Control.Async+Class+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

