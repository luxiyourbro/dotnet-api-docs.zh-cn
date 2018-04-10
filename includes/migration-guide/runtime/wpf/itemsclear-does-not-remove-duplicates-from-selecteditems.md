### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear 不会从 SelectedItems 删除重复项

|   |   |
|---|---|
|详细信息|（与启用多个所选内容） 的选择器中具有重复项假设其<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>集合的同一个项目出现多次。  从数据源 （例如通过调用 Items.Clear） 中删除这些项无法从其中移除这些<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; 仅删除第一个实例。 此外，随后使用的<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>(例如 SelectedItems.Clear()) 可能会遇到问题如<xref:System.ArgumentException?displayProperty=name>，这是因为<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>包含不再出现在数据源中的项。|
|建议|如果可能升级到.NET 4.6.2。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

