### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>WPF 文本框中默认为撤消 100 个的限制

|   |   |
|---|---|
|详细信息|在 .NET 4.5 中，WPF 文本框的默认撤消限制是 100（.NET 4.0 则没有限制）|
|建议|如果一个撤消限制为 100 太低，可以显式设置限制与 <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

