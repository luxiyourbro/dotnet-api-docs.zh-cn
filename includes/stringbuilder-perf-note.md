使用基于字符的索引与<xref:System.Text.StringBuilder.Chars%2A>属性可以是以下情况下执行速度极慢：

- <xref:System.Text.StringBuilder>实例是大 （例如，它由组成的几个数万个字符）。
- <xref:System.Text.StringBuilder>是"块区"。 也就是说，如重复对方法的调用<xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType>已自动扩展对象的<xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType>属性和分配新到它的内存块。

因为每个字符访问指导区块以查找正确的缓冲区进行到索引的整个链接的列表会严重影响性能。

> [!NOTE]
>  即使对于大型大批量<xref:System.Text.StringBuilder>对象、 使用<xref:System.Text.StringBuilder.Chars%2A>以便基于索引的访问一个或少量的字符的属性会影响可以忽略不计性能; 通常情况下，它是**0 （n)**操作。 当循环中的字符，则会发生显著的性能影响<xref:System.Text.StringBuilder>对象，它是**O(n^2)**操作。 

如果你遇到性能问题时使用基于字符的索引与<xref:System.Text.StringBuilder>对象，你可以使用任何下列解决方法：

- 将转换<xref:System.Text.StringBuilder>到实例<xref:System.String>通过调用<xref:System.Text.StringBuilder.ToString%2A>方法，然后访问字符串中的字符。

- 将现有的内容复制<xref:System.Text.StringBuilder>到新的对象预大小<xref:System.Text.StringBuilder>对象。 可以提高性能，因为新<xref:System.Text.StringBuilder>对象不是块式。 例如:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- 设置的初始容量<xref:System.Text.StringBuilder>到通过调用约等于其最大的预期大小的值的对象<xref:System.Text.StringBuilder.%23ctor(System.Int32)>构造函数。 请注意此分配的内存，即使整个块<xref:System.Text.StringBuilder>很少达到其最大容量。
