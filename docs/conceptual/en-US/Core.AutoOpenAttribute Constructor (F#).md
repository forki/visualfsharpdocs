# Core.AutoOpenAttribute Constructor (F#)

Creates an attribute used to mark a namespace or module path to be automatically opened when an assembly is referenced.

**Namespace/Module Path**: Microsoft.FSharp.Core

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signatures:
new AutoOpenAttribute : string -> AutoOpenAttribute
new AutoOpenAttribute : unit -> AutoOpenAttribute

// Usage:
new AutoOpenAttribute (path)
new AutoOpenAttribute ()
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*path*
Type: [string](http://msdn.microsoft.com/en-us/library/12b97856-ec80-4f70-a018-afb0753f755a)


The namespace or module to be automatically opened when an assembly is referenced or an enclosing module opened.



**A new AutoOpenAttribute instance.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]

## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Core.AutoOpenAttribute Class &#40;F&#35;&#41;](Core.AutoOpenAttribute+Class+28%F%2329%.md)

[Microsoft.FSharp.Core Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Core+Namespace+28%F%2329%.md)

