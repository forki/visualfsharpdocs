# NullableOperators.( =? )<'T> Function (F#)

The **=** operator where a nullable value appears on the right.

**Namespace/Module Path**: Microsoft.FSharp.Linq.NullableOperators

**Assembly**: FSharp.Core (in FSharp.Core.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Signature:
( =? ) : 'T -> Nullable<'T> -> bool when 'T : equality and 'T : (new : unit ->  'T) and 'T : struct and 'T :> ValueType

// Usage:
value =? nullableValue
```

#### [!INCLUDE[System_CAPS_parameters](//System/Token/System_CAPS_parameters_md.md)]
*value*
Type: 'T


The first input value.


*nullableValue*
Type: **T:System.Nullable&#96;1**&lt;'T&gt;


The second input value, as a nullable value.




## Return Value
**true** if the two input values are numerically equal; otherwise, **false**.


## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
If the second value is null, then the result is **false**.


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 4.0, Portable




## See Also
[Linq.NullableOperators Module &#40;F&#35;&#41;](Linq.NullableOperators+Module+28%F%2329%.md)

[Microsoft.FSharp.Linq Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Linq+Namespace+28%F%2329%.md)

