### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage 将不再引发可重入 IMessageFilter.PreFilterMessage 实现

|   |   |
|---|---|
|详细信息|.NET Framework 4.6.1 之前，调用<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>与<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>其调用<xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>或<xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>(时还调用<xref:System.Windows.Forms.Application.DoEvents>) 将导致<xref:System.IndexOutOfRangeException?displayProperty=name>。从面向.NET Framework 4.6.1 应用程序开始，将不再引发此异常，并可重入使用筛选器按上文所述可能。|
|建议|请注意，<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>将不再引发的可重入<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>行为上面所述。 这仅影响面向的.NET Framework 4.6.1.Apps 面向.NET Framework 4.6.1 可以选择退出此更改 （或目标的较旧框架中可以选择的应用） 应用程序使用[DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation)兼容性开关。|
|范围|边缘|
|版本|4.6.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

