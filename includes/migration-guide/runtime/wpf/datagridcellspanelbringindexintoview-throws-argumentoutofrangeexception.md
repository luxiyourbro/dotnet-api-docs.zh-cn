### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView 引发 ArgumentOutOfRangeException

|   |   |
|---|---|
|详细信息|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> 以异步方式将工作，当启用了列虚拟化，但尚未确定列宽。  如果列被删除之前的异步工作情况发生，<xref:System.ArgumentOutOfRangeException?displayProperty=name>可以发生。|
|建议|任何以下一项：<ol><li>升级到.NET 4.7。</li><li>安装 for.NET 4.6.2 维护最新修补程序。</li><li>避免异步响应之前删除列<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)>已完成。</li></ol>|
|范围|边缘|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

