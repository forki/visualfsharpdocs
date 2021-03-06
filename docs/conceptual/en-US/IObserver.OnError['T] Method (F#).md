# IObserver.OnError<'T> Method (F#)

Notify an observer of an error

**Namespace/Module Path**: System

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
abstract this.OnError : exn -> unit

// Usage:
iObserver.OnError (error)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*error*
Type: [exn](http://msdn.microsoft.com/en-us/library/e1569b69-3b30-440b-8c6f-966d1c6a06ab)


The exception to notify observers.




## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This API is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 API with the same name, **M:System.IObserver&#96;1.OnError(System.Exception)**.


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0




## See Also
[System.IObserver&#60;'T&#62; Interface &#40;F&#35;&#41;](System.IObserver%3C%27T%3E+Interface+28%F%2329%.md)

[System Namespace &#40;F&#35;&#41;](System+Namespace+28%F%2329%.md)

