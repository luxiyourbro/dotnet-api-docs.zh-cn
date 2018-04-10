### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a>HttpUtility.JavaScriptStringEncode 转义 and 符

|   |   |
|---|---|
|详细信息|从.NET Framework 4.5，开始<xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name>转义 & 符 (&amp;) 字符。|
|建议|如果应用依赖于此方法以前的行为，可将 aspnet:JavaScriptDoNotEncodeAmpersand 设置添加到配置文件中的 [ASP.NET appSettings 元素](https://msdn.microsoft.com/library/hh975440.aspx)。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

