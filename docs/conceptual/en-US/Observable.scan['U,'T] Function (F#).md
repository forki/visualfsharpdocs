# Observable.scan<'U,'T> Function (F#)

Returns an observable which, for each observer, allocates an item of state and applies the given accumulating function to successive values arising from the input. The returned object will trigger observations for each computed state value, excluding the initial value. The returned object propagates all errors arising from the source and completes when the source completes.

**Namespace/Module Path**: Microsoft.FSharp.Control.Observable

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Observable.scan : ('U -> 'T -> 'U) -> 'U -> IObservable<'T> -> IObservable<'U>

// Usage:
Observable.scan collector state source
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*collector*
Type: **'U -&gt; 'T -&gt; 'U**


The function to update the state with each observation.


*state*
Type: **'U**


The initial state.


*source*
Type: [IObservable](http://msdn.microsoft.com/en-us/library/04855e2b-42e4-4342-860a-b86566c4f2d9)**&lt;'T&gt;**


The input Observable.



**An observable that triggers on the updated state values.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
For each observer, the registered intermediate observing object is not thread safe. That is, observations arising from the source must not be triggered concurrently on different threads.

This function is named **Scan** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Observable Module &#40;F&#35;&#41;](Control.Observable+Module+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

