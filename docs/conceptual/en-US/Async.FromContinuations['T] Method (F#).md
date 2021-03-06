# Async.FromContinuations<'T> Method (F#)

Creates an asynchronous computation that captures the current success, exception and cancellation continuations. The callback must eventually call exactly one of the given continuations.

**Namespace/Module Path:** Microsoft.FSharp.Control

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
static member FromContinuations : (('T -> unit) * (exn -> unit) * (OperationCanceledException -> unit) -> unit) -> Async<'T>

// Usage:
Async.FromContinuations (callback)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*callback*
Type: **('T -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**) &#42; (**[exn](http://msdn.microsoft.com/en-us/library/e1569b69-3b30-440b-8c6f-966d1c6a06ab)**-&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**) &#42; (****T:System.OperationCanceledException****-&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**) -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


The function that accepts the current success, exception, and cancellation continuations.



**An asynchronous computation that provides the callback with the current continuations.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
The argument for this method is a lambda expression that takes three continuation functions, which are typically called **cont** (the success continuation), **ccont** (the cancel continuation) and **econt** (the error continuation), as the following code shows:


```
Async.FromContinuations (fun (cont, ccont, econt) -> ...)
```

>[!WARNING] {If you use this method, you must call exactly one of the continuation functions or else throw an exception, in which case F# calls **econt** with the exception on your behalf. If you call more than one continuation, call any continuation more than once, or both call a continuation and throw an exception, any subsequent use of the resulting async object may have undefined behavior.

}
**The following example illustrates how to use Async.FromContinuations to wrap an event-based asynchronous computation as an F# async.**
**[!CODE [FsAsyncAPIs#23](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis/FSharp/fs/program.fs#23)]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Async Class &#40;F&#35;&#41;](Control.Async+Class+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

