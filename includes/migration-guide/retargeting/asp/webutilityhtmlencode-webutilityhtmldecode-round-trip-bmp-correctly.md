### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode 和 WebUtility.HtmlDecode 往返 BMP 正确

|   |   |
|---|---|
|详细信息|对于应用程序面向.NET Framework 4.5，字符可能会超出基本多语言平面 (BMP) 往返过程正确传递给<xref:System.Net.WebUtility.HtmlDecode(System.String)>方法。|
|建议|此更改应不会影响当前应用程序，但若要还原原始行为，设置<code>targetFramework</code>属性<code>&lt;httpRuntime&gt;</code>为字符串以外的其他元素&quot;4.5&quot;。 还可以设置 <code>unicodeEncodingConformance</code> 配置元素的 <code>unicodeDecodingConformance</code> 和 <code>&lt;webUtility&gt;</code> 特性以单独控制 .NET Framework 的目标版本的行为。|
|范围|边缘|
|版本|4.5|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

