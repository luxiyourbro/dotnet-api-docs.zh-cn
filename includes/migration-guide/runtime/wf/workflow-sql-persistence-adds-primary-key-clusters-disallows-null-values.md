### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>工作流 SQL 持久性添加 primary key 群集和不允许在某些列中的 null 值

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7 开始，通过 SqlWorkflowInstanceStoreSchema.sql 脚本创建的 SQL 工作流实例存储 (SWIS) 的表使用聚集的主键。 因此，不支持标识<code>null</code>值。 受此更改不影响 SWIS 该操作。 进行了更新，以支持 SQL Server 事务复制。|
|建议|若要体验此更改，SQL 文件 SqlWorkflowInstanceStoreSchemaUpgrade.sql 必须应用于现有的安装。 新数据库安装将自动具有更改。|
|范围|边缘|
|版本|4.7|
|类型|运行时|

