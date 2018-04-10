### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridViews AllowCustomPaging 设置为 true 可能 PageIndexChanging 时激发事件离开视图的最后一页

|   |   |
|---|---|
|详细信息|.NET Framework 4.5 中的 bug 导致<xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name>有时不激发为<xref:System.Web.UI.WebControls.GridView?displayProperty=name>已启用的 s <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>。|
|建议|此问题已修复在.NET Framework 4.6 中，并可以通过升级到该版本的.NET Framework 进行寻址。 作为解决，应用程序可以执行任何显式 BindGrid <code>Page_Load</code> ，将命中这些条件 (<xref:System.Web.UI.WebControls.GridView?displayProperty=name>是在最后一页和最后一个<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>不同于<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>)。 或者，应用程序可以修改以允许分页 （而不是自定义分页），因为这种情况下并不演示此问题。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

