# Set.IsProperSubsetOf<'T> Method (F#)

Evaluates to **true** if all elements of the first set are in the second, and at least one element of the second is not in the first.

**Namespace/Module Path:** Microsoft.FSharp.Collections

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
member this.IsProperSubsetOf : Set<'T> -> bool (requires comparison)

// Usage:
set.IsProperSubsetOf (otherSet)
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*otherSet*
Type: [Set](http://msdn.microsoft.com/en-us/library/50cebdce-0cd7-4c5c-8ebc-f3a9e90b38d8)**&lt;'T&gt;**


The set to test against.



**true if this set is a proper subset of otherSet. Otherwise, returns false.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
**The following code illustrates the use of the IsProperSubsetOf method.**
**[!CODE [FsSets#6](../CodeSnippet/VS_Snippets_Fsharp/fssets/FSharp/fs/program.fs#6)]**
**Output**
**set [1; 2; 3; 4; 5] is a proper subset of set [1; 2; 3; 4; 5; 6]: trueset [1; 2; 3; 4; 5; 6] is a proper subset of set [1; 2; 3; 4; 5; 6]: falseset [5; 6; 7; 8; 9; 10] is a proper subset of set [1; 2; 3; 4; 5; 6]: false**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Set&#60;'T&#62; Class &#40;F&#35;&#41;](Collections.Set%3C%27T%3E+Class+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

