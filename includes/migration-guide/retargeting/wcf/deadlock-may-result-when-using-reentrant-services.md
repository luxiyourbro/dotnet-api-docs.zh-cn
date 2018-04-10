### <a name="deadlock-may-result-when-using-reentrant-services"></a>使用可重入服务时，可能会导致死锁

|   |   |
|---|---|
|详细信息|一个可重入服务，它将服务的实例限制为执行一次运行一个线程可能会产生死锁。 容易遇到此问题的服务将具有以下<xref:System.ServiceModel.ServiceBehaviorAttribute>入其代码：<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|建议|若要解决此问题，请执行以下操作：<ul><li>将服务的并发模式设置为<xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType>或&lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;。 例如:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>到.NET Framework 4.6.2，安装最新的更新或升级到更高版本的.NET framework。 这将禁用的流<xref:System.Threading.ExecutionContext>中<xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>。 此行为是可配置;它等效于将以下应用程序设置添加到你的配置文件：</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

