### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF DataTemplate 元素现 UIA 对可见

|   |   |
|---|---|
|详细信息|以前，<xref:System.Windows.DataTemplate?displayProperty=name>元素是对 UI 自动化不可见。 从 4.5 开始，UI 自动化将能检测到这些元素。 这是在许多情况下有用，但可以中断依赖于 UIA 树不包含的测试<xref:System.Windows.DataTemplate?displayProperty=name>元素。|
|建议|UI 自动化测试此应用程序可能需要更新来应对现在包括的 UIA 树结构以前不可见<xref:System.Windows.DataTemplate?displayProperty=name>元素。 例如，对于预计某些元素彼此相邻的测试，现在需要考虑到其间之前不可见的 UIA 元素。 否则，依赖 UIA 元素的特定计数或索引的测试可能需要使用新值进行更新。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

