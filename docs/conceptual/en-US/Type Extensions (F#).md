# Type Extensions (F#)

Type extensions let you add new members to a previously defined object type.


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
// Intrinsic extension.
type typename with
member self-identifier.member-name =
body
...
[ end ]

// Optional extension.
type typename with
member self-identifier.member-name =
body
...
[ end ]
```

## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
There are two forms of type extensions that have slightly different syntax and behavior. An *intrinsic extension* is an extension that appears in the same namespace or module, in the same source file, and in the same assembly (DLL or executable file) as the type being extended. An *optional extension* is an extension that appears outside the original module, namespace, or assembly of the type being extended. Intrinsic extensions appear on the type when the type is examined by reflection, but optional extensions do not. Optional extensions must be in modules, and they are only in scope when the module that contains the extension is open.

In the previous syntax, *typename* represents the type that is being extended. Any type that can be accessed can be extended, but the type name must be an actual type name, not a type abbreviation. You can define multiple members in one type extension. The *self-identifier* represents the instance of the object being invoked, just as in ordinary members.

The **end** keyword is optional in lightweight syntax.

Members defined in type extensions can be used just like other members on a class type. Like other members, they can be static or instance members. These methods are also known as *extension methods*; properties are known as *extension properties*, and so on. Optional extension members are compiled to static members for which the object instance is passed implicitly as the first parameter. However, they act as if they were instance members or static members according to how they are declared. Implicit extension members are included as members of the type and can be used without restriction.

Extension methods cannot be virtual or abstract methods. They can overload other methods of the same name, but the compiler gives preference to non-extension methods in the case of an ambiguous call.

If multiple intrinsic type extensions exist for one type, all members must be unique. For optional type extensions, members in different type extensions to the same type can have the same names. Ambiguity errors occur only if client code opens two different scopes that define the same member names.

In the following example, a type in a module has an intrinsic type extension. To client code outside the module, the type extension appears as a regular member of the type in all respects.

[!CODE [FsLangRef2#3701](../CodeSnippet/VS_Snippets_Fsharp/fslangref2/FSharp/fs/typeextensions.fs#3701)]
    You can use intrinsic type extensions to separate the definition of a type into sections. This can be useful in managing large type definitions, for example, to keep compiler-generated code and authored code separate or to group together code created by different people or associated with different functionality.

In the following example, an optional type extension extends the **System.Int32** type with an extension method **FromString** that calls the static member **Parse**. The **testFromString** method demonstrates that the new member is called just like any instance member.

[!CODE [FsLangRef2#3702](../CodeSnippet/VS_Snippets_Fsharp/fslangref2/FSharp/fs/typeextensions.fs#3702)]
    The new instance member will appear like any other method of the **Int32** type in IntelliSense, but only when the module that contains the extension is open or otherwise in scope.


## Generic Extension Methods
Before F# 3.1, the F# compiler didn't support the use of C#-style extension methods with a generic type variable, array type, tuple type, or an F# function type as the “this” parameter. F# 3.1 supports the use of these extension members.

For example, in F# 3.1 code, you can use extension methods with signatures that resemble the following syntax in C#:


```c#
static member Method<T>(this T input, T other)
```
This approach is particularly useful when the generic type parameter is constrained. Further, you can now declare extension members like this in F# code and define an additional, semantically rich set of extension methods. In F#, you usually define extension members as the following example shows:


```f#
type seq<’T> with
/// Repeat each element of the sequence n times
member xs.RepeatElements(n: int) =
seq { for x in xs do for i in 1 .. n do yield x }
```
However, for a generic type, the type variable may not be constrained. You can now declare a C#-style extension member in F# to work around this limitation. When you combine this kind of declaration with the inline feature of F#, you can present generic algorithms as extension members.

Consider the following declaration:


```f#
[<Extension>]
type ExtraCSharpStyleExtensionMethodsInFSharp () =
[<Extension>]
static member inline Sum(xs: seq<’T>) = Seq.sum xs
```
By using this declaration, you can write code that resembles the following sample.


```f#
let listOfIntegers = [ 1 .. 100 ]
let listOfBigIntegers = [ 1I to 100I ]
let sum1 = listOfIntegers.Sum()
let sum2 = listOfBigIntegers.Sum()
```
In this code, the same generic arithmetic code is applied to lists of two types without overloading, by defining a single extension member.


## See Also
[F&#35; Language Reference](F%23+Language+Reference.md)

[Members &#40;F&#35;&#41;](Members+28%F%2329%.md)

