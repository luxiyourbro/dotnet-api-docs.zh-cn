### <a name="certificate-eku-oid-validation"></a>证书 EKU OID 验证

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6 开始<xref:System.Net.Security.SslStream>或<xref:System.Net.ServicePointManager>类执行增强型密钥使用 (EKU) 对象标识符 (OID) 验证。 增强型密钥用法 (EKU) 扩展为指示使用密钥的应用程序的对象标识符 (Oid) 的集合。 EKU OID 验证将使用远程证书回调以确保远程证书用途具有正确的 Oid。|
|建议|如果不希望此更改，你可以通过添加以下切换到禁用证书 EKU OID 验证[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)中[ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)的你应用程序配置文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 为了向后兼容仅提供了此设置。 否则不建议使用。</blockquote> |
|范围|次要|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

