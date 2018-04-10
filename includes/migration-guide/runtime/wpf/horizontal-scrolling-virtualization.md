### <a name="horizontal-scrolling-and-virtualization"></a>水平滚动和虚拟化

|   |   |
|---|---|
|详细信息|此更改适用于<xref:System.Windows.Controls.ItemsControl?displayProperty=name>执行方向与主要滚动方向正交自己虚拟化 (首席示例是<xref:System.Windows.Controls.DataGrid?displayProperty=name>EnableColumnVirtualization =&quot;True&quot;)。  已更改的某些水平滚动操作的结果来生成结果更直观且更类似于可比较的垂直操作的结果。操作包括&quot;此处滚动&quot;和&quot;右边缘&quot;，则应使用来自通过右键单击水平滚动条来获取的菜单的名称。  这两种计算候选偏移量和调用<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。滚动到新的偏移量的概念后&quot;此处&quot;或&quot;边缘&quot;可能已更改，因为新取消虚拟化的内容已更改的值<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>。在.Net 4.6.2 之前, 滚动操作只需使用候选偏移量，即使它可能不&quot;此处&quot;或在&quot;边缘&quot;更。  这会导致效果，例如&quot;会传来传去&quot;滚动块，最佳示例所示。 假设<xref:System.Windows.Controls.DataGrid?displayProperty=name>具有 ExtentWidth = 1000年和宽度 = 200。  滚动到&quot;右边缘&quot;使用候选偏移量 1000年 200 = 800。  时滚动到该偏移量，新列是 de-虚拟化;让我们假设它们是范围很大，以便<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>更改为 2000年。  Scroll 结尾 HorizontalOffset = 800 和滚动块&quot;退回&quot;回附近的滚动条的中间精确的在 800/2000年 = 40%。更改是这种情况发生，然后重试时，重新计算新的候选偏移量。 (这是如何垂直滚动已工作。)更改所生成的最终用户，更易于预测和直观的体验，但它还可能会影响任何应用程序依赖于的确切值<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>水平滚动，是否被最终用户或通过显式调用调用后<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。|
|建议|使用的预测的值的应用程序<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>应将更改为提取的实际值 (和的值<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) 后无法更改任何水平滚动<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>由于重复数据的虚拟化。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.Primitives.IScrollInfo?displayProperty=nameWithType></li></ul>|

