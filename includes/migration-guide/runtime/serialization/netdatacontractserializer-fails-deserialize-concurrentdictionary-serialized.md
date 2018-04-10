### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>无法反序列化序列化与不同的.NET 版本 ConcurrentDictionary NetDataContractSerializer

|   |   |
|---|---|
|详细信息|按照设计，<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>仅当同时在序列化和反序列化端共享相同的 CLR 类型时，才可以使用。 因此，不保证可以由不同版本反序列化序列使用的.NET framework 的某一版本的对象。<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> 是已知到无法进行反序列化正确如果.NET Framework 4.5 或更早版本序列化和反序列化使用.NET Framework 4.5.1 或更高版本的类型。|
|建议|有大量针对此问题的可能解决方法：<ul><li>序列化的计算机以使用.NET Framework 4.5.1，以及升级。</li><li>使用<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>而不是<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>如这不需要在序列化和反序列化端上完全相同的 CLR 类型。</li><li>使用<xref:System.Collections.Generic.Dictionary%602?displayProperty=name>而不是<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>由于没有展现此特定 4.5-&gt;4.5.1 中断。</li></ul>|
|范围|次要|
|版本|4.5.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

