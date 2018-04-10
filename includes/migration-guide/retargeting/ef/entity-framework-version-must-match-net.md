### <a name="entity-framework-version-must-match-the-net-framework-version"></a>实体框架版本必须与匹配的.NET Framework 版本

|   |   |
|---|---|
|详细信息|实体框架版本应与.NET framework 版本匹配。 实体框架 5 适用于.NET 4.5。 有一些已知的问题和 EF 围绕.NET 4.5 项目中的 4.x <xref:System.ComponentModel.DataAnnotations>。 在.NET 4.5 中，这些已移动到另一个程序集，因此没有确定要使用的批注的问题。|
|建议|升级到.NET Framework 4.5 的实体框架 5|
|范围|主要|
|版本|4.5|
|类型|重定目标|

