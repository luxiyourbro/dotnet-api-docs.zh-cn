### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>对于与在第一条线段冒号字符的相对 Uri System.Uri.IsWellFormedUriString 方法返回 false

|   |   |
|---|---|
|详细信息|从.NET Framework 4.5，开始<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)>会将使用的相对 Uri<code>:</code>在其第一条线段如不正确。 这是从更改<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>进行以符合 RFC3986 到.NET Framework 4.0 中的行为。|
|建议|此更改 （如许多其他 URI 更改） 只会影响面向.NET Framework 4.5 （或更高版本） 的应用程序。 若要继续使用旧版本行为，面向针对.NET Framework 4.0 的应用程序。 或者，在调用之前扫描 URI 的<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>寻找<code>:</code>你可能想要删除出于验证目的，如果需要种旧行为的字符。|
|范围|次要|
|版本|4.5|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

