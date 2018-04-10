### <a name="default-signedxml-and-signedxms-algorithms-changed-to-sha256"></a>默认值？ 1？ 绎和 SignedXMS 算法更改为 SHA256

|   |   |
|---|---|
|详细信息|在.NET Framework 4.7 和早期版本，？ 1？ 绎和 SignedCMS 默认为 SHA1 对于某些操作。从.NET Framework 4.7.1 开始，默认情况下，这些操作启用 SHA256。 由于 SHA1 不再被视为是安全的此更改是必需的。|
|建议|有两个新的上下文交换机值控制是否默认情况下使用 SHA1 （不安全） 或 SHA256:<ul><li>Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms</li><li>Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms</li></ul>面向.NET Framework 4.7.1 和更高版本，如果 SHA256 的用途是，可以还原默认值为 SHA1 通过添加下面的配置的应用程序切换到[运行时](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)一部分应用配置文件：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=true;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=true&quot; /&gt;&#13;&#10;</code></pre>对于面向.NET Framework 4.7 和早期版本的应用程序，你可以选择加入此更改通过添加以下配置切换到[运行时](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)你应用程序配置文件部分：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=false;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=false&quot; /&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.Pkcs.CmsSigner?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.Reference?displayProperty=nameWithType></li></ul>|

