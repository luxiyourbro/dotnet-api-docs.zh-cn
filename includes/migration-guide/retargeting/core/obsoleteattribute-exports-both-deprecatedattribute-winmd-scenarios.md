### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute 在 WinMD 方案中将导出为 ObsoleteAttribute 和 DeprecatedAttribute

|   |   |
|---|---|
|详细信息|当你创建 Windows 元数据数据库 （.winmd 文件），<xref:System.ObsoleteAttribute?displayProperty=name>特性导出为<xref:System.ObsoleteAttribute?displayProperty=name>和[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)。|
|建议|使用的现有源代码的重新编译<xref:System.ObsoleteAttribute?displayProperty=name>属性可能会生成警告时使用该代码从 C + + /cli CX 或 JavaScript.We 不建议将<xref:System.ObsoleteAttribute?displayProperty=name>和[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)向托管程序集; 中的代码则可能会导致生成警告。|
|范围|边缘|
|版本|4.5.1|
|类型|重定目标|

