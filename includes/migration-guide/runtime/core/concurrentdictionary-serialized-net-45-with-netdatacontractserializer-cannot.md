### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>在使用 NetDataContractSerializer.NET 4.5 中序列化 ConcurrentDictionary 无法反序列化.net 4.5.1 或 4.5.2

|   |   |
|---|---|
|详细信息|由于为的类型的内部更改而<xref:System.Collections.Concurrent.ConcurrentDictionary%602>使用.NET Framework 4.5 序列化的对象使用<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>无法在.NET Framework 4.5.1 或.NET Framework 4.5.2.Note 中反序列化，它在其他方向 （移动使用.NET Framework 进行序列化 4.5.x 和反序列化使用.NET Framework 4.5) 的工作。 同样，适用于.NET Framework 4.6.Serializing 的所有 4.x 跨版本序列化和反序列化使用单个版本的.NET Framework 不受影响。|
|建议|如有必要进行序列化和反序列化<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>一个备用的序列化程序之间的.NET Framework 4.5 和.NET Framework 4.5.1/4.5.2，如<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>或<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>序列化程序应使用而不是<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>。或者，在.NET Framework 4.6 中解决此问题，因为它可能通过升级到该版本的.NET Framework 解决。|
|范围|次要|
|版本|4.5.1|
|类型|运行时|

