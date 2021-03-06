# Seq.isEmpty<'T> Function (F#)

Tests whether a sequence has any elements.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Seq

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Seq.isEmpty : seq<'T> -> bool

// Usage:
Seq.isEmpty source
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*source*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T&gt;**


The input sequence.



**exceptions tag is not supported!!!!**
**true if the input sequence is empty. Otherwise, returns false.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
The first element of the *source* sequence, if there is one, is evaluated on each call. To avoid this, you can create a cached sequence by using [Seq.cache](http://msdn.microsoft.com/en-us/library/d197f9cc-08bf-4986-9869-246e72ca73f0).

This function is named **IsEmpty** in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.

**The following code shows how to use Seq.isEmpty.**
**[!CODE [FsSequences#42](../CodeSnippet/VS_Snippets_Fsharp/fssequences/FSharp/fs/program.fs#42)]**
**Output**
**true**
**false**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Seq Module &#40;F&#35;&#41;](Collections.Seq+Module+28%F%2329%.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

