# List.average<^T> Function (F#)

Returns the average of the elements in the list.

**Namespace/Module Path:** Microsoft.FSharp.Collections.List

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
List.average : ^T list -> ^T (requires ^T with static member (+) and ^T with static member DivideByInt and ^T with static member Zero)

// Usage:
List.average list
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*list*
Type: **^T**[list](http://msdn.microsoft.com/en-us/library/c627b668-477b-4409-91ed-06d7f1b3e4a7)


The input list.



**exceptions tag is not supported!!!!**
**The resulting average.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function cannot be used directly on a list of integers since it requires that the type support an exact division operation, which is indicated by the constraint that the element type must support [DivideByInt](http://msdn.microsoft.com/en-us/library/24b70b03-c9fb-4edf-b04e-c9d8355fe1ca) Floating point types support **DivideByInt**. To compute the average of a list of integers, see the example in [List.averageBy](http://msdn.microsoft.com/en-us/library/936cc9ec-62af-464d-8726-7999c2f48403).

This function is named **Average** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code example illustrates the use of List.average.**
**[!CODE [FsLists#111](../CodeSnippet/VS_Snippets_Fsharp/fslists/FSharp/fs/program.fs#111)]**
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

