### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>引发 NullReferenceException HttpRuntime.AppDomainAppPath

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 中，则运行时会引发<code>T:System.NullReferenceException</code>检索时<code>P:System.Web.HttpRuntime.AppDomainAppPath</code>包含 null 字符的值。在.NET Framework 4.6.1 和早期版本中，则运行时会引发<code>T:System.ArgumentNullException</code>。|
|建议|你可以执行对此更改作出响应，请按照任一操作：<ul><li>处理<code>T:System.NullReferenceException</code>如果你的应用程序在.NET Framework 4.6.2 上运行。</li><li>升级到.NET Framework 4.7，也不能还原以前的行为会引发<code>T:System.ArgumentNullException</code>。</li></ul>|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

