# Async.Parallel<'T> Method (F#)

Creates an asynchronous computation that executes all the given asynchronous computations, initially queueing each as work items and using a fork/join pattern.

**Namespace/Module Path:** Microsoft.FSharp.Control

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
static member Parallel : seq<Async<'T>> -> Async<'T []>

// Usage:
Async.Parallel (computations)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*computations*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;**[Async](http://msdn.microsoft.com/en-us/library/e0b28ea2-dea5-4021-b2b9-d7d4761babde)**&lt;'T&gt;&gt;**


A sequence of distinct computations to be parallelized.



**A computation that returns an array of values from the sequence of input computations.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
If all child computations succeed, an array of results is passed to the success continuation. If any child computation raises an exception, then the overall computation will trigger an exception, and cancel the others. The overall computation will respond to cancellation while executing the child computations. If cancelled, the computation will cancel any remaining child computations but will still wait for the other child computations to complete.

**The following code example shows how to use Async.Parallel to run computations that write to a number of files asynchronously.**
**[!CODE [FsAsyncAPIs#32](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis/FSharp/fs/program.fs#32)]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Async Class &#40;F&#35;&#41;](Control.Async+Class+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

