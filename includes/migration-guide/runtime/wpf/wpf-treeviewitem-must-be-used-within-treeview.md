### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>必须在树视图中使用 WPF TreeViewItem

|   |   |
|---|---|
|详细信息|更改会限制的使用情况的 4.5 中引入了<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>元素之外<xref:System.Windows.Controls.TreeView?displayProperty=name>。 在下列条件下，可能会出现这种情况：<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>视觉父级不是一个面板。 (A<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>为生成<xref:System.Windows.Controls.TreeView?displayProperty=name>将具有为其父级的面板)</li><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>为的后代<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>充当&quot;项主机&quot;列表控件 （ListBox、 DataGrid、 ListView、 等。）。 无需启用虚拟化。</li><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>是项滚动 (<code>ScrollUnit=&quot;Item&quot;</code>)。</li><li>有些用户调用 <code>VirtualizingStackPanel.MakeVisible(v)</code> 以将元素 <code>v</code> 滚动至视图。 这可通过许多方法显式或隐式实现；或许最常见的方法是，只需单击 <code>v</code> 即可为其提供键盘焦点。</li><li>从视觉父级链<code>v</code>到<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>传递<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>。</li></ul>换而言之，此选项显示时<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>之外使用<xref:System.Windows.Controls.TreeView?displayProperty=name>，并且用户单击的后代<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>以使其视图。 如果<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>没有可获得焦点的子代，你将永远不会看到此问题。 这其中命中的情况下的一个示例是当<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>是 DataTemplate 的根。 发生此问题时，WPF 框架中将引发 InvalidCastException。|
|建议|将向此问题提供修补程序。|
|范围|次要|
|版本|4.5|
|类型|运行时|

