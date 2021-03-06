# Event.scan<'U,'T,'Del> Function (F#)

Returns a new event that consists of the results of applying the given accumulating function to successive values triggered on the input event.

**Namespace/Module Path:** Microsoft.FSharp.Control.Event

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
Event.scan : ('U -> 'T -> 'U) -> 'U -> IEvent<'Del,'T> -> IEvent<'U> (requires delegate)

// Usage:
Event.scan collector state sourceEvent
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*collector*
Type: **'U -&gt; 'T -&gt; 'U**


The function to update the state with each event value.


*state*
Type: **'U**


The initial state.


*sourceEvent*
Type: [IEvent](http://msdn.microsoft.com/en-us/library/8dbca0df-f8a1-40bd-8d50-aa26f6a8b862)**&lt;'Del,'T&gt;**


The input event.



**An event that fires on the updated state values.**
## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
An item of internal state records the current value of the state parameter. The internal state is not locked during the execution of the accumulation function, so care should be taken that the input [IEvent](http://msdn.microsoft.com/en-us/library/8dbca0df-f8a1-40bd-8d50-aa26f6a8b862) is not triggered by multiple threads simultaneously.

This function is named **Scan** in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.

**The following code example shows how to use the Event.scan function. This code implements a simple click counter. Every time the user clicks on the form, the state increments by 1 and the form's text is changed to display the new state.**
**[!CODE [FsEvents#8](../CodeSnippet/VS_Snippets_Fsharp/fsevents/FSharp/fs/program.fs#8)]**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Control.Event Module &#40;F&#35;&#41;](Control.Event+Module+28%F%2329%.md)

[Microsoft.FSharp.Control Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Control+Namespace+28%F%2329%.md)

