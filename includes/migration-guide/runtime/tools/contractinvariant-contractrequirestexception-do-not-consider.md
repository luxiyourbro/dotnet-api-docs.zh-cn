### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant 或 Contract.Requires<TException>不考虑 String.IsNullOrEmpty 为纯

|   |   |
|---|---|
|详细信息|对于面向.NET Framework 4.6.1 中，如果固定协定的应用<xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType>或的前置条件协定<xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)>调用<xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType>方法，重写程序发出编译器警告 CC1036:&quot;检测到调用方法System.String.IsNullOrWhteSpace(System.String) 而无需 [纯] 方法中。&quot;这是编译器警告而不编译器错误。|
|建议|此行为在 [GitHub 问题 #339](https://github.com/Microsoft/CodeContracts/issues/339) 中已得到解决。 若要消除此警告，你可以下载并编译中的代码协定工具的源代码的更新的版本[GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md)。 可在页面底部找到下载信息。|
|范围|次要|
|版本|4.6.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

