### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 默认值现在为 SHA256

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7.1 开始，默认的消息签名 WCF 中的 Msmq 消息的算法为 SHA256。 在.NET Framework 4.7 和早期版本中，默认消息签名算法是 SHA1。|
|建议|如果在.NET Framework 4.7.1 上遇到进行此更改后的兼容性问题或更高版本，你可以选择退出更改通过添加以下行将对<code>&lt;runtime&gt;</code>app.config 文件的部分：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|运行时|

