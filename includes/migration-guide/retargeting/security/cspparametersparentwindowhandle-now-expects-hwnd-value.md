### <a name="cspparametersparentwindowhandle-now-expects-hwnd-value"></a>CspParameters.ParentWindowHandle 现在需要 HWND 值

|   |   |
|---|---|
|详细信息|<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>值，在.NET Framework 2.0 中引入允许应用程序注册父窗口句柄值，以便访问密钥所需的任何 UI （如 PIN 提示或同意对话框） 为指定窗口的模式子级将打开。从面向.NET Framework 4.7 应用开始，可以设置 Windows 窗体应用程序<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>使用类似以下的代码的属性：<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>在以前版本的.NET Framework，则这应为<xref:System.IntPtr?displayProperty=name>表示内存中的位置其中[HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND)驻留的值。 将属性设置为窗体。在 Windows 7 上处理和早期版本不起作用，但在 Windows 8 和更高版本上，这会导致&quot; <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>： 参数不正确。&quot;|
|建议|面向.NET 4.7 或更高版本希望注册父窗口关系的应用程序建议使用简化的形式：<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>用户必须标识要传递的正确值已持有值的内存位置的地址<code>form.Handle</code>可以选择退出此行为更改 AppContext 开关设置<code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code>到<code>true</code>。<ol><li>以编程方式设置 compat 上开关 AppContext，如所述[此处](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>在 app.config 文件的 <code>&lt;runtime&gt;</code> 部分中添加下面的代码行：</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>相反，用户想要选择加入新行为对.NET Framework 4.7 运行时在较旧的.NET Framework 版本的应用程序负载可以设置 AppContext 时切换到<code>false</code>。|
|范围|次要|
|版本|4.7|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle?displayProperty=nameWithType></li></ul>|

