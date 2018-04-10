### <a name="path-colon-checks-are-stricter"></a>路径冒号检查是更严格

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 中，已进行大量更改以支持以前不受支持的路径 （同时长度和格式）。 有关正确的驱动器分隔符 （冒号） 语法检查所做更正确，其必须阻止它们用于可容忍的几个选择路径 Api 中的某些 URI 路径的副作用。|
|建议|如果将 URI 传递给受影响的 Api，修改要首先是合法路径的字符串。<ul><li>从 Url 中手动删除方案 (例如删除<code>file://</code>从 Url)</li><li>传递的 URI<xref:System.Uri>类并使用 <xref:System.Uri.LocalPath></li></ul>或者，你可以选择退出的新路径标准化设置<code>Switch.System.IO.UseLegacyPathHandling</code>AppContext 交换机为 true。|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

