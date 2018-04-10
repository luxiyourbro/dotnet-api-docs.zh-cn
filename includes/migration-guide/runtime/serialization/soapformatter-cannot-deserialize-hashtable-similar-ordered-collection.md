### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter 无法反序列化哈希表和类似有序集合对象

|   |   |
|---|---|
|详细信息|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name>不保证对象序列化在一个.NET Framework 版本将成功进行反序列化的其他版本下的执行。 具体而言，一些排序集合 (如<xref:System.Collections.Hashtable?displayProperty=name>) 添加 4.0 和 4.5 之间的成员，以便这些类型的对象无法反序列化使用.NET 4.0 如果它们已使用.NET 4.5 序列化。 请注意，如果序列化的数据在同一 .NET Framework 版本中进行序列化和反序列化，将不会发生任何问题。|
|建议|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> 应使用替换序列化<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>序列化或<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>能够适应.NET Framework 的更改。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

