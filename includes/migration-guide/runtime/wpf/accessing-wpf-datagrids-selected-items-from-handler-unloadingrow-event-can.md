### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>DataGrid 的 UnloadingRow 事件处理程序从访问 WPF DataGrid 的选定的项可能会导致 NullReferenceException

|   |   |
|---|---|
|详细信息|由于.NET Framework 4.5，事件处理程序中的 bug<xref:System.Windows.Controls.DataGrid>涉及某一行的删除的事件可能会导致<xref:System.NullReferenceException?displayProperty=name>如果它们访问引发<xref:System.Windows.Controls.DataGrid>的<xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name>或<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>属性。|
|建议|此问题已修复在.NET Framework 4.6 中，并可以通过升级到该版本的.NET Framework 进行寻址。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

