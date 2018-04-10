### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>ETW 事件名称不能仅通过"启动"停止"后缀

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6 和 4.6.1 中，则运行时会引发<xref:System.ArgumentException>当两个事件跟踪的 Windows (ETW) 事件名称差异仅在于&quot;启动&quot;或&quot;停止&quot;后缀 (作为一个事件名为时<code>LogUser</code>和另一个名为<code>LogUserStart</code>)。 在这种情况下，运行时不会构建不能发出任何日志记录的事件源。|
|建议|若要避免此异常，请确保没有两个事件名称的差异仅在于&quot;启动&quot;或&quot;停止&quot;后缀。从.NET Framework 4.6.2; 开始删除此要求运行时可以区分事件名称的差异仅在于&quot;启动&quot;和&quot;停止&quot;后缀。|
|范围|边缘|
|版本|4.6|
|类型|重定目标|

