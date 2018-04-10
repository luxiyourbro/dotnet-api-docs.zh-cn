### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>尝试 TCP/IP 连接到的 SQL Server 数据库，将解析为`localhost`失败

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6 和 4.6.1 中，尝试 TCP/IP 连接到的 SQL Server 数据库，将解析为<code>localhost</code>失败，出现错误，&quot;建立与 SQL Server 的连接时发生与网络相关或特定于实例的错误。 未找到或无法访问服务器。 请验证实例名称是否正确，SQL Server 是否已配置为允许远程连接。 (提供程序： SQL 网络接口，错误： 26-错误查找服务器/实例指定)&quot;|
|建议|解决此问题，且在.NET Framework 4.6.2 还原以前的行为。 若要连接到将解析为 SQL Server databsae <code>localhost</code>，升级到.NET Framework 4.6.2。|
|范围|次要|
|版本|4.6|
|类型|运行时|

