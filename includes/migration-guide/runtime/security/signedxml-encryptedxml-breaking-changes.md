### <a name="signedxml-and-encryptedxml-breaking-changes"></a>？ 1？ 绎和 EncryptedXml 重大更改

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 中，安全修补程序在<xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name>和<xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name>导致不同的运行时行为。 例如，应用于对象的<ul><li>如果文档包含多个元素具有相同<code>id</code>属性和签名则将这些元素之一定位为签名的根，文档将现在被视为无效。</li><li>文档引用中使用非规范 XPath 转换算法都被视为无效。</li><li>文档引用中使用非规范的 XSLT 转换算法现在将考虑无效。</li><li>分离的外部资源任何的签名程序利用将无法执行此操作。</li></ul>|
|建议|开发人员可能想要查看的使用情况<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>和<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>、 以及类型派生自<xref:System.Security.Cryptography.Xml.Transform>由于文档接收方可能不能对其进行处理。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

