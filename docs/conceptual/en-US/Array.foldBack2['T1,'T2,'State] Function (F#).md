# Array.foldBack2<'T1,'T2,'State> Function (F#)

Apply a function to pairs of elements drawn from the two collections, right-to-left, threading an accumulator argument through the computation. The two input arrays must have the same lengths, otherwise an **T:System.ArgumentException** is raised.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Array

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Array.foldBack2 : ('T1 -> 'T2 -> 'State -> 'State) -> 'T1 [] -> 'T2 [] -> 'State -> 'State

// Usage:
Array.foldBack2 folder array1 array2 state
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*folder*
Type: **'T1 -&gt; 'T2 -&gt; 'State -&gt; 'State**


The function to update the state given the input elements.


*array1*
Type: **'T1**[[]](http://msdn.microsoft.com/en-us/library/def20292-9aae-4596-9275-b94e594f8493)


The first input array.


*array2*
Type: **'T2**[[]](http://msdn.microsoft.com/en-us/library/def20292-9aae-4596-9275-b94e594f8493)


The second input array.


*state*
Type: **'State**


The initial state.



**exceptions tag is not supported!!!!**
**The final state.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
This function is named **FoldBack2** in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.

**The following code shows how to use Array.foldBack2.**
**[!CODE [FsArrays#47](../CodeSnippet/VS_Snippets_Fsharp/fsarrays/FSharp/fs/program.fs#47)]**
**Output**
**Ending balance: $1205.00**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Array Module &#40;F&#35;&#41;](Collections.Array+Module+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

