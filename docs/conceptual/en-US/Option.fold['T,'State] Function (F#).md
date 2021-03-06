# Option.fold<'T,'State> Function (F#)

Evaluates the equivalent of [List.fold](http://msdn.microsoft.com/en-us/library/c272779e-bae7-4983-8d7f-16b345bb33a0) for an option.

**Namespace/Module Path**: Microsoft.FSharp.Core.Option

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
fold : ('State -> 'T -> 'State) -> 'State -> 'T option -> 'State

// Usage:
fold folder state option
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*folder*
Type: **'State -&gt; 'T -&gt; 'State**


A function to update the state data when given a value from an option.


*state*
Type: **'State**


The initial state.


*option*
Type: **'T**[option](http://msdn.microsoft.com/en-us/library/b08add48-34bf-4410-80a1-ef6a8daddc58)


The input option.



**The original state if the option is None, otherwise it returns the updated state with the folder and the option value.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
The expression **fold f s inp** evaluates to **match inp with None -&gt; s | Some x -&gt; f s x**.

This function is named **Fold** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code illustrates the use of Option.fold.**
**[!CODE [FsOptions#4](../CodeSnippet/VS_Snippets_Fsharp/fsoptions/FSharp/fs/program.fs#4)]**
**Output**
**[1; 2; 3; 4; 5; 6; 7; 8; 9; 10][0; 1; 2; 3; 4; 5; 6; 7; 8; 9; 10]Enter a number: New list: []Enter a number: 10New list: [10]Enter a number: 1New list: [1; 10]Enter a number: abcNew list: [1; 10]Enter a number: 9New list: [9; 1; 10]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Core.Option Module &#40;F&#35;&#41;](Core.Option+Module+28%F%2329%.md)

[Microsoft.FSharp.Core Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Core+Namespace+28%F%2329%.md)

