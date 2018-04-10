### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>当文本框中处于非活动状态时，WPF 文本框中选择文本出现另一种颜色

|   |   |
|---|---|
|详细信息|在 .NET 4.5 中，当 WPF 文本框控件处于非活动状态（该控件没有焦点）时，文本框中选定文本所显示的颜色与该控件处于活动状态时所显示的颜色不同。|
|建议|通过设置可能会还原以前的 (.NET 4.0) 行为<xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported>属性<code>false</code>。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

