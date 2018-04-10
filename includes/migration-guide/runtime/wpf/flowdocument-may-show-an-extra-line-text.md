### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument 可能显示额外的行的文本

|   |   |
|---|---|
|详细信息|在某些情况下，<xref:System.Windows.Documents.FlowDocument>在.NET Framework 4.5 相比如何显示在.NET Framework 4.0 上运行时上运行时，元素将显示额外的行的文本。 有没有已知的情况下的项更改导致不佳或显示屏，显示任何文本，但它会导致要显示的文本，以前中被省略<xref:System.Windows.Documents.FlowDocument>的查看。|
|建议|在某些情况下，由一个减少显示元素的 PageHeight 属性可以还原的以前显示的行数。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

