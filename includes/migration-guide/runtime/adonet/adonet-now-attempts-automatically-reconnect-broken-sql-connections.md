### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET 现在尝试自动重新连接已中断的 SQL 连接

|   |   |
|---|---|
|详细信息|从.NET Framework 4.5.1 开始，.NET Framework 将尝试自动重新连接已中断的 SQL 连接。 虽然这通常将使应用程序更可靠，边缘情况下应用程序需要知道，以便它可以采取一些措施重新连接的连接已丢失。|
|建议|如果由于兼容性问题不需要此功能，它可以禁用通过设置<xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name>连接字符串的属性 (或<xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) 为 0。|
|范围|边缘|
|版本|4.5.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

