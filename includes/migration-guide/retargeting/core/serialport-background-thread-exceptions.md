### <a name="serialport-background-thread-exceptions"></a>无效/不后台线程异常

|   |   |
|---|---|
|详细信息|后台线程使用创建<xref:System.IO.Ports.SerialPort>流不再终止进程引发 OS 异常时。在面向.NET Framework 4.7 和早期版本的应用程序，进程将终止时创建与后台线程上引发操作系统异常<xref:System.IO.Ports.SerialPort>流。在应用程序中，面向.NET Framework 4.7.1 或更高版本，后台线程等待的是操作系统事件与活动的串行端口和相关可能会崩溃在某些情况下，例如突然删除串行端口。|
|建议|对于面向.NET Framework 4.7.1 的应用程序，你可以选择退出异常处理，如果这是不值得通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>对于面向的应用的.NET framework 的早期版本但在.NET Framework 4.7.1 上运行或更高版本，你可以选择在异常处理通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

