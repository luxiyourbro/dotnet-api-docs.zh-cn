### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>ETW EventListeners 并捕获事件从提供程序与显式关键字 （例如 TPL 提供程序）

|   |   |
|---|---|
|详细信息|具有空白关键字掩码的 ETW EventListeners 无法从具有显式关键字的提供程序中正确捕获事件。 在 .NET Framework 4.5 中，TPL 提供程序开始提供显式关键字，引发了此问题。 在 .NET Framework 4.6 中，EventListeners 已更新，此问题不再存在。|
|建议|若要解决此问题，请替换对的调用<xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)>通过显式指定的 EnableEvents 重载调用&quot;任何关键字&quot;掩码，用于使用： <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>。或者，此问题已修复在.NET Framework 4.6 中，并可以通过升级到该版本的.NET Framework 进行寻址。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

