### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>WPF PackageDigitalSignatureManager 的默认哈希算法现在为 SHA256

|   |   |
|---|---|
|详细信息|<code>System.IO.Packaging.PackageDigitalSignatureManager</code>提供与 WPF 包之间的关系的数字签名功能。  在.NET Framework 4.7 和早期版本中，默认的算法 (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) 用于签名的包部分已 SHA1。  由于具有 SHA1 的新安全问题，此默认设置已更改为 SHA256 从.NET Framework 4.7.1 开始。  此更改影响所有包签名，包括 XPS 文档。|
|建议|开发人员想要利用此更改时面向的 framework 版本低于.NET 4.7.1 或的开发人员需要以前的功能，同时面向.NET 4.7.1 或更高版本可以正确设置以下 AppContext 标志。  值为 true 将导致 SHA1 用作默认的算法;false 导致 SHA256。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

