### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>WPF 拼写检查失败以意想不到的方式

|   |   |
|---|---|
|详细信息|这包括大量的 WPF 拼写检查器问题：<ul><li>WPF 拼写检查器有时引发 <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>WPF 拼写检查器将失败，并<xref:System.UnauthorizedAccessException>时使用以其他用户身份运行启动应用程序</li><li>WPF 拼写检查器不正确地标识等 Hausnummer 德语复合单词中的拼写错误。</li></ul>|
|建议|问题 1 – 此问题已修复在.NET Framework 4.6.2 问题 #2-WPF 拼写检查器时使用以其他用户身份运行启动应用程序不再受支持。 从.NET Framework 4.6.2 开始，在这种方式中启动的应用程序将不再意外崩溃-改为将以静默方式禁用拼写检查器。 问题 #3-此问题已修复在.NET Framework 4.6.2 中。|
|范围|边缘|
|版本|4.6.1|
|类型|运行时|

