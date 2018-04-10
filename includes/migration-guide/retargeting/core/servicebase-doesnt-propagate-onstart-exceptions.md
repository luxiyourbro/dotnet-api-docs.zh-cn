### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase 不传播 OnStart 异常

|   |   |
|---|---|
|详细信息|在.NET Framework 4.7 和早期版本中，在服务启动时引发的异常不会传播到调用方<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>。从面向.NET Framework 4.7.1 的应用程序开始，运行时将传播到异常<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>无法启动的服务。|
|建议|服务启动后，如果没有异常，该异常将传播。 这应帮助诊断服务无法启动的情况。如果不需要此行为，则可以通过添加以下选择退出<AppContextSwitchOverrides>元素<runtime>的应用程序配置文件的部分：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>如果你的应用程序面向早期版本比 4.7.1，但你想要具有此行为，添加以下<AppContextSwitchOverrides>元素<runtime>的应用程序配置文件的部分：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

