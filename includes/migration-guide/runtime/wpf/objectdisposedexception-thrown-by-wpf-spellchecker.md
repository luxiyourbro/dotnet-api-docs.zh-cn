### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException 由 WPF 拼写检查器引发

|   |   |
|---|---|
|详细信息|WPF 应用程序有时崩溃期间使用的应用程序关闭<xref:System.ObjectDisposedException?displayProperty=name>由拼写检查器引发。 这被固定的在.NET 4.7 WPF 通过适当地，处理异常，从而确保应用程序将不再受到负面影响。 应注意的是偶尔最可能的异常将继续在调试器下运行应用程序中观察到的。|
|建议|升级到.NET 4.7|
|范围|边缘|
|版本|4.6.1|
|类型|运行时|

