### <a name="connection-pool-blocking-period-for-azure-sql-databases-is-removed"></a>删除阻塞期的 Azure SQL 数据库的连接池

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6.2 开始，对于连接打开请求到已知的 Azure SQL 数据库 (*。 database.windows.net，*。 database.chinacloudapi.cn，*。 database.usgovcloudapi.net，*。 database.cloudapi.de)，连接池阻塞期删除，并连接打开错误不会缓存。 在出现暂时连接错误后随即重试连接打开请求。 此更改允许的连接打开尝试立即重试对于 Azure SQL 数据库，从而提高云-启用应用程序的性能。 对于所有其他连接尝试，连接池阻塞期仍然会强制执行。在.NET Framework 4.6.1 和早期版本中，当应用程序连接到数据库时遇到暂时性连接故障时连接尝试不能重试速度快，因为连接池中缓存错误并重新引发它为 1 到 5 秒分钟。 有关详细信息，请参阅[SQL Server 连接池 (ADO.NET)](~/docs/framework/data/adonet/sql-server-connection-pooling.md)。 这种行为会给 Azure SQL 数据库连接带来问题，因为经常会因暂时性错误而导致连接失败，这些错误通常在几秒内便会恢复。 连接池拦截功能意味着，应用程序无法连接到数据库大量时间，即使数据库可用并且应用程序需要几秒钟内呈现。|
|建议|如果不需要此行为，可以通过设置配置连接池阻塞期<xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name>.NET Framework 4.6.2 中引入的属性。 该属性的值属于 <xref:System.Data.SqlClient.PoolBlockingPeriod?displayProperty=name> 枚举，可采用以下三个值中的任意一个：<ul><li><xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.Auto></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.NeverBlock></li></ul>可以通过将 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name> 属性设置为 <xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock> 来还原以前的行为。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.Common.DbConnection.OpenAsync?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

