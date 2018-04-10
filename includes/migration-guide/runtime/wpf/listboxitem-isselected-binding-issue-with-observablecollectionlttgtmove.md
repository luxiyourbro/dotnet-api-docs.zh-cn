### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>ObservableCollection ListBoxItem IsSelected 绑定问题&lt;T&gt;。移动

|   |   |
|---|---|
|详细信息|调用<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>或<xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)>上绑定到的集合<xref:System.Windows.Controls.ListBox?displayProperty=name>其中选中项会导致不正常行为与将来的所选内容或的 unselection<xref:System.Windows.Controls.ListBox?displayProperty=name>项。|
|建议|调用<xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name>和<xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name>而不是<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>将解决此问题。 此外，此问题已在 .NET Framework 4.6 中解决，因此升级到该版本的 .NET Framework 即可解决该问题。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

