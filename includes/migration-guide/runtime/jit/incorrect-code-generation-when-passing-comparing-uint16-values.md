### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>不正确的代码生成时传递和比较 UInt16 值

|   |   |
|---|---|
|详细信息|由于.NET Framework 4.7 中引入的更改，在某些情况下不正确地在.NET Framework 4.7 上运行的应用程序中的 JIT 编译器生成的代码比较两个<code>T:System.UInt16</code>值。 有关详细信息，请参阅[问题 #11508： 无提示不良 codegen 时传递和比较 ushort args](https://github.com/dotnet/coreclr/issues/11508) GitHub.com 上。|
|建议|如果你遇到问题，在.NET Framework 4.7 中的 16 位无符号值的比较中，升级到.NET Framework 4.7.1。|
|范围|边缘|
|版本|4.7|
|类型|运行时|

