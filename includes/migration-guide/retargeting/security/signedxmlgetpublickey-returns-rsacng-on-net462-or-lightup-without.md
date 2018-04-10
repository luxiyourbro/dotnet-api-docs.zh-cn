### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey 中返回 RSACng 对 net462 （或激活），而不重定目标更改

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6.2，返回的对象的具体类型开始<xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType>方法 （不带特点） 从更改的 CryptoServiceProvider 实现 Cng 的实现。 这是因为实现更改从使用<code>certificate.PublicKey.Key</code>使用内部<code>certificate.GetAnyPublicKey</code>将转发到<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>。|
|建议|从.NET Framework 4.7.1 上运行的应用开始，可以使用.NET Framework 4.6.1 中的默认情况下使用的 CryptoServiceProvider 实现，并通过添加下面的配置的早期版本切换到[运行时](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)你应用程序配置文件部分：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

