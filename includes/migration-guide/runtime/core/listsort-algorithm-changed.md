### <a name="listsort-algorithm-changed"></a>List.Sort 算法更改

|   |   |
|---|---|
|详细信息|从.NET Framework 4.5 开始<xref:System.Collections.Generic.List%601?displayProperty=name>的排序算法变得 （而不是快速排序反省排序）。 <xref:System.Collections.Generic.List%601?displayProperty=name>排序已被稳定的但此更改可能会导致不同的方案以不稳定的方式进行排序。 这只是表示等效项可能在后续调用中的 api 的不同顺序排序。|
|建议|因为旧的排序算法也的 （尽管方式稍有不同） 不稳定，不应依赖于始终按特定顺序排序的等效项的任何代码。 如果有具体，取决于和正在 lucky 与旧行为的代码的实例，应更新该代码，以便使用的比较器确定地将所需顺序中的项进行排序。|
|范围|透明|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

