### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>不同的异常处理 ObjectContext.CreateDatabase 和 DbProviderServices.CreateDatabase 方法

|   |   |
|---|---|
|详细信息|从 .NET 4.5 开始，如果数据库创建失败，<code>CreateDatabase</code> 方法将尝试删除空数据库。 如果该操作成功，将传播原始 <xref:System.Data.SqlClient.SqlException?displayProperty=name>（而非始终在 .NET 4.0 中引发的 <xref:System.InvalidOperationException?displayProperty=name>）|
|建议|捕获时<xref:System.InvalidOperationException?displayProperty=name>执行时<xref:System.Data.Objects.ObjectContext.CreateDatabase>或<xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>，SQLExceptions 应现在还捕捉。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

