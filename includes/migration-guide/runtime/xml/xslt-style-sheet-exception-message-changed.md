### <a name="xslt-style-sheet-exception-message-changed"></a>更改的 XSLT 样式表异常消息

|   |   |
|---|---|
|详细信息|在.NET Framework 4.5 中，XSLT 文件过于复杂时的错误消息的文本是&quot;样式表太过复杂。&quot;在以前版本中，错误消息为&quot;XSLT 编译错误。&quot;取决于错误消息的文本的应用程序代码将不再有效。 但是，异常类型保持不变，因此，此更改应该不会造成实际影响。|
|建议|更新任何应用程序代码，具体取决于从这种错误情况异常消息，需要新的消息，或 （甚至更好地） 更新代码以仅取决于异常类型 (<xref:System.Xml.Xsl.XsltException?displayProperty=name>)，这仍是如此。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

