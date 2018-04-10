### <a name="xslt-forward-compat-now-works"></a>XSLT 向前兼容现在可以正常工作

|   |   |
|---|---|
|详细信息|在.NET Framework 4 中，XSLT 1.0 向前兼容性具有以下问题：<ul><li>如果其版本设置为 2.0，并且分析器遇到无法识别的 XSLT 1.0 构造，则无法加载样式表。</li><li>如果将样式表版本设置为 1.1，则 <code>xsl:sort</code> 构造无法对数据进行排序。</li></ul>在.NET Framework 4.5 中，这些问题已修复，并且 XSLT 1.0 向前兼容性模式可正常工作。|
|建议|大多数应用程序应该不会影响，但数据将进行排序以不同方式在某些情况下，现在遵循 xsl:sort。 如果<code>xsl:sort</code>是在 1.1 样式表中使用，确认应用过去一直不依赖于数据的排序顺序。 如果应用程序依赖于排序行为 4.0，删除<code>xsl:sort</code>从样式表。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

