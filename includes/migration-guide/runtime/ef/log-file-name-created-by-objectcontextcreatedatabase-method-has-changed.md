### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>由 ObjectContext.CreateDatabase 方法创建的日志文件名称已更改，以便匹配 SQL Server 规范

|   |   |
|---|---|
|详细信息|当<xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name>方法调用是直接或通过使用 Code First 与 SqlClient 提供程序和连接字符串中的 AttachDBFilename 值，它会创建名为而不是 filename.ldf filename_log.ldf （其中 filename 是名称的日志文件指定的文件的 AttachDBFilename 值）。 此更改通过提供根据 SQL Server 规范命名的日志文件来改进调试。|
|建议|如果日志文件名对应用而言很重要，应更新该应用，以使用标准的 _log.ldf 文件名格式。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

