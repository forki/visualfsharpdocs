# DbmlFile Type Provider (F#)

Provides the types for a database schema encoded in a .dbml file, the database schema format used by LINQ to SQL. .dbml files contain a schema for a database.

**Namespace/Module Path:** Microsoft.FSharp.Data.TypeProviders

**Assembly:** FSharp.Data.TypeProviders (in FSharp.Data.TypeProviders.dll)


## [!INCLUDE[System_CAPS_syntax](//System/Token/System_CAPS_syntax_md.md)]

```
type DbmlFile<File : string,              ?ResolutionFolder : string,              ?ContextTypeName : string,              ?Serializable : bool>
```

## Static Type Parameters


|Type Parameter|Description|
|--------------|-----------|
|File : string|The path to the DBML file for the database mapping.|
|?ResolutionFolder : string|A folder to be used to resolve relative file paths at compile time. The default value is the folder that contains the project or script.|
|?ContextTypeName : string|The name of the container type that you use to access all the generated types.|
|?Serializable : bool|**true** if you want the generated types to be serializable. The default is **false**.|

## [!INCLUDE[System_CAPS_remarks](//System/Token/System_CAPS_remarks_md.md)]
The .dbml file is an XML file that contains the full description or schema for a relational database. DBML stands for Database Modeling Language and is the database schema format that LINQ to SQL uses. You can generate a .dbml file by using the command-line tool, **SQLMetal.exe**. For more information on **SQLMetal.exe**, see [SqlMetal.exe &#40;Code Generation Tool&#41;](SqlMetal.exe+28%Code+Generation+Tool29%.md). For more information on LINQ to SQL, see [LINQ to SQL](LINQ+to+SQL.md).

For a walkthrough on how to use the **DbmlFile** type provider, see [Walkthrough: Generating F&#35; Types from a DBML File &#40;F&#35;&#41;](Walkthrough%3A+Generating+F%23+Types+from+a+DBML+File+28%F%2329%.md).


## Platforms
[!INCLUDE[win8](../Token/win8_md.md)], Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable


## See Also
[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+28%F%2329%.md)

