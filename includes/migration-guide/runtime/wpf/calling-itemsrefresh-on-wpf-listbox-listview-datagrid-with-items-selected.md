### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>WPF 列表框、 列表视图或选中项的 DataGrid 上的调用 Items.Refresh 可能导致重复的项显示在元素

|   |   |
|---|---|
|详细信息|在.NET Framework 4.5，而在中选择项从代码调用 ListBox.Items.Refresh<xref:System.Windows.Controls.ListBox?displayProperty=name>可能会导致在列表中复制所选的项目。 使用时出现类似问题<xref:System.Windows.Controls.ListView?displayProperty=name>和<xref:System.Windows.Controls.DataGrid?displayProperty=name>。 此问题已在 .NET Framework 4.6 中解决。|
|建议|通过以编程方式取消之前的项的选中情况下，此问题可能会得到解决<xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name>调用，并且在调用完成后再重新选择它们。 此外，此问题已在 .NET Framework 4.6 中解决，因此升级到该版本的 .NET Framework 即可解决该问题。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

