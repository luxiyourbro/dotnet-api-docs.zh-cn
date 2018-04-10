### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>在 Windows 7 上与非 IFS Winsock BSP 或 LSP 存在的 SqlConnection.Open 失败

|   |   |
|---|---|
|详细信息|<xref:System.Data.SqlClient.SqlConnection.Open> 和<xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)>失败.NET Framework 4.5 中，如果在与非 IFS Winsock BSP 或 LSP Windows 7 计算机上运行计算机上是否存在。若要确定是否已安装非 IFS BSP 或 LSP，使用<code>netsh WinSock Show Catalog</code>命令，并检查每个<code>Winsock Catalog Provider Entry</code>返回的项。 如果服务标志值设置了 <code>0x20000</code> 位，提供程序将使用 IFS 句柄，并将正确运行。 如果 <code>0x20000</code> 位已清除（未设置），则它将是非 IFS BSP 或 LSP。|
|建议|此 bug 已在 .NET Framework 4.5.2 中得到修复，因此升级 .NET Framework 可避免出现此问题。 或者，可通过删除任何已安装的非 IFS Winsock LSP 来避免出现此问题。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

