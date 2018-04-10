### <a name="unicode-standard-version-80-categories-now-supported"></a>现在支持的 Unicode 标准版本 8.0 类别

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 中，框架中的 Unicode 数据已从 Unicode 标准版本 6.3 升级到版本 8.0。  请求在.NET Framework 4.6.2 的 Unicode 字符类别，某些结果可能与以前的.NET Framework 版本中的结果不匹配。  此更改主要影响切罗基文字节和新傣文元音符号和音调标记。|
|建议|检查代码并移除/更换逻辑依赖于硬编码的 Unicode 字符类别。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

