# List.sum<^T> Function (F#)

Returns the sum of the elements in the list.

**Namespace/Module Path:** Microsoft.FSharp.Collections.List

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
List.sum : ^T list -> ^T (requires ^T with static member (+) and ^T with static member Zero)

// Usage:
List.sum list
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*list*
Type: **^T**[list](http://msdn.microsoft.com/en-us/library/c627b668-477b-4409-91ed-06d7f1b3e4a7)


The input list.



**The resulting sum.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function is named **Sum** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code example illustrates the use of List.sum, [List.sumBy](http://msdn.microsoft.com/en-us/library/b7623389-0fe1-4762-9c67-51079903ab7d), and [List.average](http://msdn.microsoft.com/en-us/library/2b9a627b-106d-4548-8c4c-ab5058b8f8e1).**
**[!CODE [FsLists#11](../CodeSnippet/VS_Snippets_Fsharp/fslists/FSharp/fs/program.fs#11)]**
**Output**
**1.000000**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.List Module &#40;F&#35;&#41;](Collections.List+Module+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

