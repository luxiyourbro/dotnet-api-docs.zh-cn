### <a name="throttle-concurrent-requests-per-session"></a>每个会话的限制并发请求数

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 和更早版本，ASP.NET 将按顺序，执行请求使用相同的 Sessionid 和 ASP.NET 将始终发出通过 cookie Sessionid 默认情况下。 如果页需要很长时间才能响应，它将只需通过浏览器上按 F5 来大幅降低服务器性能。 在此修复程序，我们将添加要跟踪已排队的请求和超过指定的限制时终止请求的计数器。 默认值为 50。 如果达到此限制，在事件日志和 HTTP 500 响应可能记录在 IIS 日志中，将记录警告。|
|建议|若要还原旧行为，可以在 web.config 文件中添加下面的设置，从而选择禁用新行为。<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|重定目标|

