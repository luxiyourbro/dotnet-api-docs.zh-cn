### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection 可以不再连接到 SQL Server 1997 或数据库使用 VIA 适配器

|   |   |
|---|---|
|详细信息|使用 SQL Server 数据库的连接[虚拟接口适配器 (VIA) 协议](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx)不再受支持。 用于连接到 SQL Server 数据库的协议是在连接字符串中可见。 通过将包含 VIA 连接：&lt;servername&gt;。 如果此应用程序连接到 SQL 通过以外 VIA 协议 (tcp： 或 np： 例如)，则将不遇到任何重大更改。此外，不再支持连接到 SQL Server 7 (1997)。|
|建议|不推荐使用 VIA 协议，因此，应使用备用协议连接到 SQL 数据库。 使用的最常见协议是 TCP/IP。 找不到有关启用 TCP/IP 协议的说明[此处](https://msdn.microsoft.com/library/bb909712.aspx)。 如果将访问该数据库仅从 intranet 中，共享的管道协议可能会提供更好的性能，如果网络速度很慢。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

