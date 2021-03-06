# Observable.map<'T,'U> Function (F#)

Returns an observable which transforms the observations of the source by the given function. The transformation function is executed once for each subscribed observer. The returned object also propagates error observations arising from the source and completes when the source completes.

**Namespace/Module Path:** Microsoft.FSharp.Control.Observable

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Observable.map : ('T -> 'U) -> IObservable<'T> -> IObservable<'U>

// Usage:
Observable.map mapping source
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*mapping*
Type: **'T -&gt; 'U**


The function applied to observations from the source.


*source*
Type: [IObservable](http://msdn.microsoft.com/en-us/library/04855e2b-42e4-4342-860a-b86566c4f2d9)**&lt;'T&gt;**


The input Observable.



**An Observable of the type specified by mapping.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function is named **Map** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable, Portable




## See Also
[Control.Observable Module &#40;F&#35;&#41;](Control.Observable+Module+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

