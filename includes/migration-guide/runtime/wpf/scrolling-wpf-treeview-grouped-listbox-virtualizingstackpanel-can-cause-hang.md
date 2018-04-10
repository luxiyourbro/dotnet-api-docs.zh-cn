### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>滚动 WPF 树视图或分组的 ListBox VirtualizingStackPanel 中可能会导致挂起

|   |   |
|---|---|
|详细信息|在.NET Framework 4.5 版中，滚动 WPF<xref:System.Windows.Controls.TreeView?displayProperty=name>在虚拟化堆栈面板可导致挂起。 如果视区中有边距 (中的项之间<xref:System.Windows.Controls.TreeView?displayProperty=name>，例如，或在 ItemsPresenter 元素上)。 此外，在某些情况下，即使没有边距，视图中不同大小的项目也可能会导致不稳定性。|
|建议|升级到 .NET Framework 4.5.1 可避免此 bug 出现。 或者，可以从查看集合删除边距 (如<xref:System.Windows.Controls.TreeView?displayProperty=name>s) 中虚拟化堆栈如果所有包含项的面板是相同的大小。|
|范围|主要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

