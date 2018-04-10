### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a>在任务之间的 CurrentCulture 和 CurrentUICulture 流

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6，开始<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>存储在线程的<xref:System.Threading.ExecutionContext?displayProperty=name>，在异步操作的流动。这意味着，更改为<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>将会反映在更高版本以异步方式运行的任务。 这是从以前的.NET Framework 版本的行为不同 (这将重置<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>所有异步任务中)。|
|建议|此更改影响的应用可能会解决这个问题通过显式设置所需<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>作为异步任务中的第一个操作。 或者，这一旧行为 (不使<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 可能通过设置以下的兼容性开关参加：<pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre>.NET Framework 4.6.2 中的 WPF 的已修复此问题。 它还中已修复了.NET 框架 4.6，通过 4.6.1 [KB 3139549](https://support.microsoft.com/kb/3139549)。 面向 4.6 或更高版本的.NET 应用程序将自动获得正确的行为在 WPF 应用程序- <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 将保留在调度程序操作。|
|范围|次要|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|

