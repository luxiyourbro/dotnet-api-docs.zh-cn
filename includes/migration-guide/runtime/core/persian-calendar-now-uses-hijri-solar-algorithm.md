### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>波斯历现在均使用回历太阳能算法

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6，开始<xref:System.Globalization.PersianCalendar?displayProperty=name>类均使用回历太阳能算法。 转换之间的日期<xref:System.Globalization.PersianCalendar?displayProperty=name>和其他日历可能会产生略有不同的结果以开头的.NET Framework 4.6 日期早于 1800年或晚于 2023 （公历）。此外，<xref:System.Globalization.PersianCalendar.MinSupportedDateTime>现<code>March 22, 0622 instead of March 21, 0622</code>。|
|建议|请注意，在 .NET 4.6 中使用 PersianCalendar 时，某些较早或较晚的日期可能略微不同。 另外，当在不同 .NET Framework 版本上运行的进程之间序列化日期时，请勿将它们存储为 PersianCalendar 日期字符串（因为这些值可能不相同）。|
|范围|次要|
|版本|4.6|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

