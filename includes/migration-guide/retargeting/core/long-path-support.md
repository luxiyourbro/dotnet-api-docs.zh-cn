### <a name="long-path-support"></a>长路径支持

|   |   |
|---|---|
|详细信息|从应用开始，支持.NET Framework 4.6.2，长路径 (最多 32 个 K 字符），该目标和 260 个字符 (或<code>MAX_PATH</code>) 已删除路径的长度限制。对于应用程序编译为面向.NET Framework 4.6.2，代码路径之前引发<xref:System.IO.PathTooLongException?displayProperty=name>因为路径超过 260 个字符将立即引发<xref:System.IO.PathTooLongException?displayProperty=name>仅在以下情况：<ul><li>路径的长度大于<xref:System.Int16.MaxValue>(32,767) 个字符。</li><li>操作系统返回 <code>COR_E_PATHTOOLONG</code> 或其等同项。</li></ul>对于面向.NET Framework 4.6.1 及更早版本的应用程序，则运行时会自动引发<xref:System.IO.PathTooLongException?displayProperty=name>每当路径超过 260 个字符。|
|建议|对于面向.NET Framework 4.6.2 的应用程序，你可以选择退出长路径支持如果这是不值得通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>对于面向的应用的.NET framework 的早期版本但在.NET Framework 4.6.2 上运行或更高版本，你可以选择在长路径支持通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.6.2|
|类型|重定目标|

