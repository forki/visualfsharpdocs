# Seq.iter<'T> Function (F#)

Applies the given function to each element of the collection.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Seq

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Seq.iter : ('T -> unit) -> seq<'T> -> unit

// Usage:
Seq.iter action source
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*action*
Type: **'T -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


A function to apply to each element of the sequence.


*source*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T&gt;**


The input sequence.



**exceptions tag is not supported!!!!**

## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function is named **Iterate** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following example illustrates the use of Seq.iter.**
**[!CODE [FsSamples101#1003](../CodeSnippet/VS_Snippets_Fsharp/fssamples101/FSharp/fs/beginners.fs#1003)]**
**Seq.iter: (1, 1) (2, 4) (3, 9) (4, 16) (5, 25)****The following example illustrates the use of Seq.iter to work with CSV (Comma-Separated Value) files.**
**[!CODE [FsSamples101#2003](../CodeSnippet/VS_Snippets_Fsharp/fssamples101/FSharp/fs/intermediate.fs#2003)]**
**-------Enumeration 1------**
**line System.String[]**
**line System.String[]**
**-------Enumeration 2------**
**line has 8 entries**
**line has 7 entries**
**-------Enumeration 3------**
**lengths of entries: [|7; 0; 6; 0; 6; 5; 0; 1|]**
**lengths of entries: [|5; 0; 6; 0; 4; 0; 2|]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Seq Module &#40;F&#35;&#41;](Collections.Seq+Module+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

