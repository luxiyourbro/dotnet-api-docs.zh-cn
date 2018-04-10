### <a name="changes-in-path-normalization"></a>路径规范化中的更改

|   |   |
|---|---|
|详细信息|从面向.NET Framework 4.6.2 开始与应用程序中，在其中运行时规范化路径的方式已更改。规范化路径涉及修改标识的路径或文件，以便它符合目标操作系统上的有效路径的字符串。 路径规范化通常涉及以下操作：<ul><li>规范化处理组件和目录分隔符。</li><li>将当前目录应用到相对路径。</li><li>评估相对目录 （.） 或路径中的父目录 （.）。</li><li>删减指定字符。</li></ul>从面向.NET Framework 4.6.2 开始与应用程序中，默认情况下启用路径规范化中的以下更改：<ul><li>运行时在规范化处理路径时以操作系统的 [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) 函数为准。</li><li>路径规范化再也不用删减目录部分的末尾内容（如目录名称末尾的空格）。</li><li>在完全信任的设备路径语法支持包括 <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</li><li>The runtime does not validate device syntax paths.</li><li>The use of device syntax to access alternate data streams is supported.</li></ul>These changes improve performance while allowing methods to access previously inaccessible paths. Apps that target the .NET Framework 4.6.1 and earlier versions but are running under the .NET Framework 4.6.2 or later are unaffected by this change.|
|建议|面向.NET Framework 4.6.2 或更高版本可以选择退出此应用更改，并通过添加以下使用旧的规范化<code>&lt;runtime&gt;</code>应用程序配置文件节：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>在.NET Framework 4.6.2 上运行或更高版本可以通过添加以下行将对启用对路径规范化的更改应用的目标.NET Framework 4.6.1 或更早版本，但<code>&lt;runtime&gt;</code>的应用程序.configuration 文件的部分：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.6.2|
|类型|重定目标|

