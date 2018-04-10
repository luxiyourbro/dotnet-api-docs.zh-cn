### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a>TLS 1.x 默认情况下的将 SCH_SEND_AUX_RECORD 标志传递给基础 SCHANNEL API

|   |   |
|---|---|
|详细信息|使用 TLS 时 1.x，依赖于基础 Windows SCHANNEL API 的.NET Framework。 从.NET Framework 4.6 开始[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)标志会传递默认情况下，SCHANNEL 给。 这将导致 SCHANNEL 拆分到两个单独的记录，为单字节和第二个作为第一个要加密数据<em>n</em>-1 字节。在极少数情况下，这会中断客户端和假设的数据位于单个记录中的现有服务器之间的通信。|
|建议|如果此更改会中断与现有的服务器的通信，则可以禁用发送[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)标志，并还原不将数据拆分为单独的记录通过添加以下切换到以前的行为[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)中[ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)的你的应用配置文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 为了向后兼容仅提供了此设置。 否则不建议使用。</blockquote> |
|范围|边缘|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

