### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>从 CellEditEnding 处理程序调用 DataGrid.CommitEdit 删除焦点

|   |   |
|---|---|
|详细信息|调用<xref:System.Windows.Controls.DataGrid.CommitEdit>从之一<xref:System.Windows.Controls.DataGrid?displayProperty=name>的<xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name>事件处理程序会导致<xref:System.Windows.Controls.DataGrid?displayProperty=name>失去焦点。|
|建议|此 bug 已在 .NET Framework 4.5.2 中得到修复，因此升级 .NET Framework 可避免出现此问题。 或者，可通过显式重新选择避免<xref:System.Windows.Controls.DataGrid?displayProperty=name>之后调用<xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

