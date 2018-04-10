### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>使用 TransportWithMessageCredential 安全模式的 WCF 绑定

|   |   |
|---|---|
|详细信息|从开始在.NET Framework 4.6.1 中，使用 TransportWithMessageCredential 安全模式的 WCF 绑定可以设置为使用无符号接收消息&quot;到&quot;非对称安全密钥的标头。默认情况下，未签名&quot;到&quot;标头将继续.NET 4.6.1 中，会拒绝。 单元测试仅将接受如果应用程序 opts 到这个新模式的使用 Switch.System.ServiceModel.AllowUnsignedToHeader 配置开关的操作。由于这是一项可以选择使用的功能，它不应影响现有应用的行为。|
|建议|由于这是一项可以选择使用的功能，因此它不应影响现有应用的行为。 若要控制是否或不使用新的行为，请使用以下配置设置：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|透明|
|版本|4.6.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

