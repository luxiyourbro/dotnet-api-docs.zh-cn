### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition Datetime 返回略有不同的字符串

|   |   |
|---|---|
|详细信息|字符串表示形式<xref:System.Net.Mime.ContentDisposition?displayProperty=name>的已更新，从 4.6，始终表示的小时部分<xref:System.DateTime?displayProperty=name>具有两位数。 这是为了符合 [RFC822](http://www.ietf.org/rfc/rfc0822.txt) 和 [RFC2822](http://www.ietf.org/rfc/rfc2822.txt)。 这将导致在 4.6 中，当其中一个处理时间元素早于上午 10 点时，<xref:System.Net.Mime.ContentDisposition.ToString> 将返回稍微不同的字符串。 请注意通过将它们转换为字符串，因此任何 ContentDispositions 有时序列化<xref:System.Net.Mime.ContentDisposition.ToString>应评审操作、 序列化或 GetHashCode 调用。|
|建议|不要期望不同 .NET Framework 版本的 ContentDispositions 的字符串表示形式相互进行正确比较。 如果可以，请在执行比较前将字符串转换回 ContentDispositions。|
|范围|次要|
|版本|4.6|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

