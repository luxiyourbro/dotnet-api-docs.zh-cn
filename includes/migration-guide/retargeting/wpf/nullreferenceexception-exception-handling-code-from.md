### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>ImageSourceConverter.ConvertFrom 异常处理代码中的 NullReferenceException

|   |   |
|---|---|
|详细信息|<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> 异常处理代码中的错误导致了引发不正确的 <xref:System.NullReferenceException?displayProperty=name>，而不是引发计划的异常（例如 <xref:System.IO.DirectoryNotFoundException?displayProperty=name>、<xref:System.IO.FileNotFoundException?displayProperty=name>），此更改改正该错误，使得该方法现在引发正确的异常。默认情况下，所有面向 .NET Framework 4.6.2 和更低版本的应用程序将继续引发 <xref:System.NullReferenceException?displayProperty=name> 以实现兼容性，面向 .NET Framework 4.7 和更高版本的开发人员应看到正确的异常。//使用“x”替换空格（如果适用）|
|建议|想要还原为在面向 .NET Framework 4.7 时获取 <xref:System.NullReferenceException?displayProperty=name> 的开发人员可以将以下内容添加/合并到应用程序的 App.config 文件：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

