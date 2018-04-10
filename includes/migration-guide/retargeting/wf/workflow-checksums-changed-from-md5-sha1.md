### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>从 MD5 更改为 SHA1 的工作流校验和

|   |   |
|---|---|
|详细信息|若要支持使用 Visual Studio 进行调试，工作流运行时生成使用哈希算法的工作流实例的校验和。 在.NET Framework 4.6.2 和早期版本中，使用 MD5 算法，这将导致问题 FIPS 启用系统上工作流校验和哈希。 从.NET Framework 4.7 开始，该算法是 SHA1。 如果你的代码已持久化这些校验和，则会将不兼容。|
|建议|如果代码是无法加载工作流实例由于校验和失败，请尝试设置<code>AppContext</code>切换&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;为 true。在代码中：<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>或配置中：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7|
|类型|重定目标|

