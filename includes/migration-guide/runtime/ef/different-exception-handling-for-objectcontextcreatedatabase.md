### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a><span data-ttu-id="91bbe-101">不同的异常处理 ObjectContext.CreateDatabase 和 DbProviderServices.CreateDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="91bbe-101">Different exception handling for ObjectContext.CreateDatabase and DbProviderServices.CreateDatabase methods</span></span>

|   |   |
|---|---|
|<span data-ttu-id="91bbe-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="91bbe-102">Details</span></span>|<span data-ttu-id="91bbe-103">从 .NET 4.5 开始，如果数据库创建失败，<code>CreateDatabase</code> 方法将尝试删除空数据库。</span><span class="sxs-lookup"><span data-stu-id="91bbe-103">Beginning in .NET 4.5, if database creation fails, <code>CreateDatabase</code> methods will attempt to drop the empty database.</span></span> <span data-ttu-id="91bbe-104">如果该操作成功，将传播原始 <xref:System.Data.SqlClient.SqlException?displayProperty=name>（而非始终在 .NET 4.0 中引发的 <xref:System.InvalidOperationException?displayProperty=name>）</span><span class="sxs-lookup"><span data-stu-id="91bbe-104">If that operation succeeds, the original <xref:System.Data.SqlClient.SqlException?displayProperty=name> will be propagated (instead of the <xref:System.InvalidOperationException?displayProperty=name> that was always thrown in .NET 4.0)</span></span>|
|<span data-ttu-id="91bbe-105">建议</span><span class="sxs-lookup"><span data-stu-id="91bbe-105">Suggestion</span></span>|<span data-ttu-id="91bbe-106">捕获时<xref:System.InvalidOperationException?displayProperty=name>执行时<xref:System.Data.Objects.ObjectContext.CreateDatabase>或<xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>，SQLExceptions 应现在还捕捉。</span><span class="sxs-lookup"><span data-stu-id="91bbe-106">When catching an <xref:System.InvalidOperationException?displayProperty=name> while executing <xref:System.Data.Objects.ObjectContext.CreateDatabase> or <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions should now also be caught.</span></span>|
|<span data-ttu-id="91bbe-107">范围</span><span class="sxs-lookup"><span data-stu-id="91bbe-107">Scope</span></span>|<span data-ttu-id="91bbe-108">次要</span><span class="sxs-lookup"><span data-stu-id="91bbe-108">Minor</span></span>|
|<span data-ttu-id="91bbe-109">版本</span><span class="sxs-lookup"><span data-stu-id="91bbe-109">Version</span></span>|<span data-ttu-id="91bbe-110">4.5</span><span class="sxs-lookup"><span data-stu-id="91bbe-110">4.5</span></span>|
|<span data-ttu-id="91bbe-111">类型</span><span class="sxs-lookup"><span data-stu-id="91bbe-111">Type</span></span>|<span data-ttu-id="91bbe-112">运行时</span><span class="sxs-lookup"><span data-stu-id="91bbe-112">Runtime</span></span>|
|<span data-ttu-id="91bbe-113">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="91bbe-113">Affected APIs</span></span>|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|
