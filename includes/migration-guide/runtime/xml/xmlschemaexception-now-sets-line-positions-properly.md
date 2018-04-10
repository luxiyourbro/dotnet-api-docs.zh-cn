### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException 现在正确设置行的位置

|   |   |
|---|---|
|详细信息|如果<xref:System.Xml.Linq.LoadOptions.SetLineInfo>值传递给 Load 方法并发生验证错误，<xref:System.Xml.Schema.XmlSchemaException.LineNumber>和<xref:System.Xml.Schema.XmlSchemaException.LinePosition>属性现在包含行信息。|
|建议|假定的异常处理代码<xref:System.Xml.Schema.XmlSchemaException.LineNumber>和<xref:System.Xml.Schema.XmlSchemaException.LinePosition>将不会因为加载 XML 时使用 SetLineInfo 时，这些属性将立即正确设置应更新集。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

