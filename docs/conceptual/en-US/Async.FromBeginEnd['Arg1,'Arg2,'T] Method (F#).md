# Async.FromBeginEnd<'Arg1,'Arg2,'T> Method (F#)

Creates an asynchronous computation in terms of a Begin/End pair of actions in the style used in CLI APIs.

**Namespace/Module Path**: Microsoft.FSharp.Control

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
static member FromBeginEnd : 'Arg1 * 'Arg2 * ('Arg1 * 'Arg2 * AsyncCallback * obj -> IAsyncResult) * (IAsyncResult -> 'T) * ?(unit -> unit) -> Async<'T>

// Usage:
Async.FromBeginEnd (arg1, arg2, beginAction, endAction)
Async.FromBeginEnd (arg1, arg2, beginAction, endAction, cancelAction = cancelAction)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*arg1*
Type: **'Arg1**


The first argument for the operation.


*arg2*
Type: **'Arg2**


The second argument for the operation.


*beginAction*
Type: **'Arg1 &#42; 'Arg2 &#42;****T:System.AsyncCallback****&#42;**[obj](http://msdn.microsoft.com/en-us/library/dcf2430f-702b-40e5-a0a1-97518bf137f7)**-&gt;****T:System.IAsyncResult**


The function initiating a traditional CLI asynchronous operation.


*endAction*
Type: **T:System.IAsyncResult****-&gt;   'T**


The function completing a traditional CLI asynchronous operation.


*cancelAction*
Type: **(**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**-&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)**)**


An optional function to be executed when a cancellation is requested.



**An asynchronous computation wrapping the given Begin/End functions.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This overload should be used if the operation is qualified by two arguments. For example, the following code creates an asynchronous computation for a web service call.


```f#
Async.FromBeginEnd(arg1,arg2,ws.BeginGetWeather,ws.EndGetWeather)
```
When the computation is run, *beginFunc* is executed, with a callback which represents the continuation of the computation. When the callback is invoked, the overall result is fetched using *endFunc*.

The computation will respond to cancellation while waiting for the completion of the operation. If a cancellation occurs, and *cancelAction* is specified, then it is executed, and the computation continues to wait for the completion of the operation. If *cancelAction* is not specified, then cancellation causes the computation to stop immediately, and subsequent invocations of the callback are ignored.

For an example, see [Async.FromBeginEnd&lt;'T&gt; Method (F#)](http://msdn.microsoft.com/en-us/library/eb24fcb5-36fb-4c9b-8343-02148b327b56).


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Async Class &#40;F&#35;&#41;](Control.Async+Class+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

