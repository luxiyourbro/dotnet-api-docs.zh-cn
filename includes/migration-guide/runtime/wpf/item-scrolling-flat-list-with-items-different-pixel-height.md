### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>项滚动不同的像素高度的项的平面列表

|   |   |
|---|---|
|详细信息|当<xref:System.Windows.Controls.ItemsControl?displayProperty=name>显示使用虚拟化的集合 (<code>IsVirtualizing=true</code>) 和项-滚动 (<code>ScrollUnit=Item</code>)，以及何时控件滚动以显示的项的高度 （像素） 不同于与其相邻元素，<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>循环访问所有集合中的项。 此迭代中; 期间 UI 无响应如果集合很大，这可以被视作挂起。在其他情况下，即使在以前的.Net 版本中发生迭代。 例如，它时发生像素滚动 (<code>ScrollUnit=Pixel</code>) 项滚动时遇到项具有不同像素高度和后层次结构数据 (如<xref:System.Windows.Controls.TreeView?displayProperty=name>或<xref:System.Windows.Controls.ItemsControl?displayProperty=name>与启用的分组) 在遇到具有的项时不同于与其相邻元素的子代项数目。为项滚动和不同的像素高度的情况下，.Net 4.6.1 若要修复的层次结构数据的布局中的 bug 中引入了迭代。  如果数据是平面 （无层次结构，），而.Net 4.6.2 不执行它在这种情况下，它则不需要。|
|建议|如果迭代，即发生.Net 4.6.1 中但不是在早期版本的如果<xref:System.Windows.Controls.ItemsControl?displayProperty=name>是滚动的简单列表项-具有不同像素高度的项目中，有两个补救措施：<ol><li>安装.Net 4.6.2。</li><li>安装修补程序 HR 1605 for.Net 4.6.1。</li></ol>|
|范围|次要|
|版本|4.6.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

