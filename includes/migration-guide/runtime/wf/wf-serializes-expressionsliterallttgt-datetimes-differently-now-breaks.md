### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF 序列化 Expressions.Literal&lt;T&gt; Datetime 以不同方式现在 （中断自定义 XAML 分析器）

|   |   |
|---|---|
|详细信息|关联<xref:System.Windows.Markup.ValueSerializer>对象会将转换<xref:System.DateTime?displayProperty=name>或<xref:System.DateTimeOffset?displayProperty=name>第二个对象，其和<xref:System.DateTime.Millisecond?displayProperty=name>组件都为非零和 (对于<xref:System.DateTime?displayProperty=name>值) 其<xref:System.DateTime.Kind>属性不是属性元素未指定而不是字符串的语法。 此更改允许 <xref:System.DateTime?displayProperty=name> 和 <xref:System.DateTimeOffset?displayProperty=name> 值往返。 假定输入 XAML 是采用特性语法的自定义 XAML 分析器将无法正常运行。|
|建议|此更改允许 <xref:System.DateTime?displayProperty=name> 和 <xref:System.DateTimeOffset?displayProperty=name> 值往返。 假定输入 XAML 是采用特性语法的自定义 XAML 分析器将无法正常运行。|
|范围|边缘|
|版本|4.5|
|类型|运行时|

