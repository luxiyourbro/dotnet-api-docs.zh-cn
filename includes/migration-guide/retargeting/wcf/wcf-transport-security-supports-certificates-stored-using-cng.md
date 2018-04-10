### <a name="wcf-transport-security-supports-certificates-stored-using-cng"></a>WCF 传输安全性支持使用 CNG 中存储的证书

|   |   |
|---|---|
|详细信息|从面向.NET Framework 4.6.2 开始与应用程序中，WCF 传输安全支持使用 Windows 加密库 (CNG) 存储的证书。 此支持仅限于将证书与指数长度不超过 32 位的公钥结合使用。 当应用程序的目标.NET Framework 4.6.2 时，此功能是在默认情况下。在.NET framework 的早期版本，则尝试使用 X509 证书与 CSG 密钥存储提供程序会引发异常。|
|建议|目标.NET Framework 4.6.1 和更早版本，但在.NET Framework 4.6.2 运行的应用可以通过添加以下行将对启用对 CNG 证书支持<code>&lt;runtime&gt;</code>app.config 或 web.config 文件的部分：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableCngCertificates=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>也可以使用以下代码以编程方式完成此操作：<pre><code class="language-cs">private const string DisableCngCertificates = @&quot;Switch.System.ServiceModel.DisableCngCertificate&quot;;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, false);&#13;&#10;</code></pre><pre><code class="language-vb">Const DisableCngCertificates As String = &quot;Switch.System.ServiceModel.DisableCngCertificates&quot;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, False)&#13;&#10;</code></pre>请注意，鉴于有此更改，将不再执行任何依赖无法尝试使用 CNG 证书启动安全通信的异常处理代码。|
|范围|次要|
|版本|4.6.2|
|类型|重定目标|

