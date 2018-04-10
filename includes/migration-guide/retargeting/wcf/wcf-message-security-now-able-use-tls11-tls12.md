### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>WCF 消息安全现在是能够使用 TLS1.1 和 TLS1.2

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7 开始，客户可以 TLS1.1 或 TLS1.2 在配置的 SSL3.0 和 TLS1.0 除了通过应用程序配置设置的 WCF 消息安全性。|
|建议|在.NET Framework 4.7，支持 TLS1.1 和 TLS1.2 WCF 消息安全中的默认处于禁用状态。 你可以通过添加以下行将对启用它<code>&lt;runtime&gt;</code>app.config 或 web.config 文件的部分：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|重定目标|

