### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>异常处理 ImageSourceConverter.ConvertFrom 从代码中的 NullReferenceException

|   |   |
|---|---|
|详细信息|异常处理代码中的错误<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)>导致不正确<xref:System.NullReferenceException?displayProperty=name>而不是预期异常引发 (例如<xref:System.IO.DirectoryNotFoundException?displayProperty=name>， <xref:System.IO.FileNotFoundException?displayProperty=name>)，以便该方法现在将正确的异常引发，此更改将更正该错误。通过默认面向.NET Framework 4.6.2 的所有应用程序，下面将继续引发<xref:System.NullReferenceException?displayProperty=name>及更高版本兼容性，面向.NET Framework 4.7 的开发人员有可能的话，应看到右 exceptions.// 替换空间具有 x|
|建议|开发人员想要恢复到获取<xref:System.NullReferenceException?displayProperty=name>当面向.NET Framework 4.7 可以添加转换/合并到其应用程序的 App.config 文件以下：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

