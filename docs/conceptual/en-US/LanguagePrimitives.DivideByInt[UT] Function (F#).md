# LanguagePrimitives.DivideByInt<^T> Function (F#)

Divides a value by an integer.

**Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
DivideByInt : ^T -> int -> ^T (requires ^T with static member DivideByInt)

// Usage:
DivideByInt x y
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*x*
Type: **^T**


The dividend, or numerator.


*y*
Type: [int](http://msdn.microsoft.com/en-us/library/025d5455-3622-4ea5-9573-3ecbd4ee1375)


The divisor, or denominator.



**The quotient.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
If a type supports **DivideByInt**, the type supports exact division (floating-point division), rather than integer division, which rounds down to the nearest integer result.

Functions like [Seq.average](http://msdn.microsoft.com/en-us/library/609d793b-c70f-4e36-9ab4-d928056d65b8) work only if the element type supports exact division. If you try to use **Seq.average** with an integer sequence, you get an error that indicates that the element type must implement **DivideByInt**. Typically, you can resolve this error by using [Seq.averageBy](http://msdn.microsoft.com/en-us/library/47c855c1-2dbd-415a-885e-b909d9d3e4f8) and adding a cast to a floating-point value. The following code shows how to use **Seq.averageBy** with an integer sequence.


```f#
let average = [ 1 .. 10 ]
|> Seq.averageBy (fun elem -> float elem)
printfn "%f" average
```

## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library VersionsF# Core Library Versions**

Supported in: 2.0, 4.0, PortablePortable2.0, 4.0, Portable




## See Also
[Core.LanguagePrimitives Module &#40;F&#35;&#41;](Core.LanguagePrimitives+Module+28%F%2329%.md)

[Microsoft.FSharp.Core Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Core+Namespace+28%F%2329%.md)

