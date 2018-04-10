### <a name="aescryptoserviceprovider-decryptor-provides-a-reusable-transform"></a>AesCryptoServiceProvider 解密器提供了可重用的转换

|   |   |
|---|---|
|详细信息|从面向.NET Framework 4.6.2 的应用开始<xref:System.Security.Cryptography.AesCryptoServiceProvider>解密器提供了可重用的转换。 调用 <xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name> 后，此转换将重新初始化并且可以重用。 对于面向.NET framework 的早期版本的应用程序，尝试通过调用重用解密器<xref:System.Security.Cryptography.CryptoAPITransform.TransformBlock(System.Byte[],System.Int32,System.Int32,System.Byte[],System.Int32)?displayProperty=name>后调用<xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name>引发<xref:System.Security.Cryptography.CryptographicException>或者生成损坏的数据。|
|建议|由于这是预期的行为，此更改的影响应该很小。依赖于先前行为的应用程序可以选择不使用通过添加以下配置设置来对其<code>&lt;runtime&gt;</code>应用程序的配置文件节：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>此外，面向以前版本的.NET framework 但在从.NET Framework 4.6.2 开始的.NET framework 版本下运行的应用程序可以通过选择使用在向其添加到以下配置设置<code>&lt;runtime&gt;</code>部分应用程序的配置文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.AesCryptoServiceProvider.CreateDecryptor?displayProperty=nameWithType></li></ul>|

