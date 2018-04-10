### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>一些.NET Api 原因第一次机会 （处理） EntryPointNotFoundExceptions

|   |   |
|---|---|
|详细信息|在.NET Framework 4.5，少量的.NET 方法开始引发第一次机会<xref:System.EntryPointNotFoundException?displayProperty=name>s。 这些异常在 .NET Framework 内进行处理，但可能会中断不希望出现最可能的异常的测试自动化。 启用 HighVersionLie 后，这些相同的 API 会中断一些 ApiVerifier 方案。|
|建议|升级到 .NET Framework 4.5.1 可避免此 bug 出现。 或者，可以更新测试自动化以不会在首次中断<xref:System.EntryPointNotFoundException?displayProperty=name>s。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

