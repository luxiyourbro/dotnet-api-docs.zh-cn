### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt;始终返回缓存实例

|   |   |
|---|---|
|详细信息|从.NET 4.5 开始<xref:System.Linq.Enumerable.Empty%60%601>始终返回缓存的内部实例<xref:System.Collections.Generic.IEnumerable%601>。以前，<xref:System.Linq.Enumerable.Empty%60%601>将缓存一个空<xref:System.Collections.Generic.IEnumerable%601>次调用 API 时，这意味着，在某些情况下在其中<xref:System.Linq.Enumerable.Empty%60%601>调用快速和并发，不同类型的实例无法返回对不同的调用API。|
|建议|因为以前的行为不确定，所以代码不太可能依赖它。 但是，如果出现需要比较空枚举并希望它们有时不相等这一罕见情形，应创建显式空数组 (<code>new T[0]</code>)，而非使用 <xref:System.Linq.Enumerable.Empty%60%601>。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

