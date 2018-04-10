### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>更改 TextBlock 控件的父级的 IsEnabled 属性会影响任何子控件

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6.2，更改开始<xref:System.Windows.UIElement.IsEnabled?displayProperty=name>属性的父级的<xref:System.Windows.Controls.TextBlock?displayProperty=name>控制会影响任何子控件 （如超链接和按钮） 的<xref:System.Windows.Controls.TextBlock?displayProperty=name>控件。在.NET Framework 4.6.1 和早期版本中，控件内<xref:System.Windows.Controls.TextBlock?displayProperty=name>始终不能反映的状态<xref:System.Windows.UIElement.IsEnabled?displayProperty=name>属性<xref:System.Windows.Controls.TextBlock?displayProperty=name>父。|
|建议|无。 此更改符合 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 控件中各控件的预期行为。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

