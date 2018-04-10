### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>DataObject.GetData 现在将数据检索为 utf-8

|   |   |
|---|---|
|详细信息|用于面向.NET Framework 4 或.NET Framework 4.5.1 或更早版本上运行的应用程序<code>DataObject.GetData</code>HTML 格式将数据检索为 ASCII 字符串。 因此，非 ASCII 字符 （字符的 ASCII 代码大于 0x7F） 由两个随机字符表示。对于面向.NET Framework 4.5 或更高版本且在.NET Framework 4.5.2 上运行应用， <code>DataObject.GetData</code> HTML 格式的数据检索为 utf-8，它可正确代表大于 0x7F 的字符。|
|建议|如果你实现了一个 HTML 格式的字符串的编码问题的解决方法 (例如，进行显式编码的 HTML 字符串从剪贴板检索通过将其传递给<xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) 和正在重定目标版本 4 到 4.5，你的应用程序解决方法，应删除。如果出于某种原因需要这一旧行为，则应用程序可以面向.NET Framework 4.0，若要获得该行为。|
|范围|边缘|
|版本|4.5.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

