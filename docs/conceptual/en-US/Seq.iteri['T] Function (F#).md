# Seq.iteri<'T> Function (F#)

Applies the given function to each element of the collection. The integer passed to the function indicates the index of element.

**Namespace/Module Path**: Microsoft.FSharp.Collections.Seq

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Seq.iteri : (int -> 'T -> unit) -> seq<'T> -> unit

// Usage:
Seq.iteri action source
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*action*
Type: [int](http://msdn.microsoft.com/en-us/library/025d5455-3622-4ea5-9573-3ecbd4ee1375)**-&gt; 'T -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


A function to apply to each element of the sequence that can also access the current index.


*source*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T&gt;**


The input sequence.



**exceptions tag is not supported!!!!**

## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function is named **IterateIndexed** in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.

**The following code shows how to use Seq.iteri and compares its behavior to related functions.**
**[!CODE [FsSequences#43](../CodeSnippet/VS_Snippets_Fsharp/fssequences/FSharp/fs/program.fs#43)]**
**Output**
**Seq.iter: element is 1**
**Seq.iter: element is 2**
**Seq.iter: element is 3**
**Seq.iteri: element 0 is 1**
**Seq.iteri: element 1 is 2**
**Seq.iteri: element 2 is 3**
**Seq.iter2: elements are 1 4**
**Seq.iter2: elements are 2 5**
**Seq.iter2: elements are 3 6**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Seq Module &#40;F&#35;&#41;](Collections.Seq+Module+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

