### <a name="default-value-of-servicepointmanagersecurityprotocol-is-securityprotocoltypesystemdefault"></a>默认值为 ServicePointManager.SecurityProtocol 是 SecurityProtocolType.System.Default

|   |   |
|---|---|
|详细信息|从面向.NET Framework 4.7 的默认值的应用开始<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>属性是<xref:System.Net.SecurityProtocolType.SystemDefault?displayProperty=nameWithType>。 此更改允许.NET Framework SslStream （例如 FTP、 HTTPS 和 SMTP） 的网络 Api 基于继承默认安全协议从操作系统而不是使用.NET Framework 定义的硬编码值。 默认值因操作系统和由系统管理员执行任何自定义配置而异。 有关每个版本的 Windows 操作系统中的默认 SChannel 协议的信息，请参阅[中 TLS/SSL (Schannel SSP) 的协议](https://msdn.microsoft.com/library/windows/desktop/mt808159.aspx)。对于面向.NET Framework 中，默认值的早期版本的应用程序<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>属性取决于所面向的.NET Framework 的版本。 请参阅[的重定目标更改从.NET Framework 4.5.2 到 4.6 进行迁移的网络部分](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#networking)有关详细信息。|
|建议|此更改影响面向.NET Framework 4.7 或更高版本的应用程序。如果你希望使用定义的协议，而不是依赖于系统的默认设置，你可以显式设置的值<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>属性。如果此更改是不可取的则可以通过添加配置设置为选择退出[\<运行时 >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)的应用程序配置文件的部分。 下面的示例演示<code>&lt;runtime&gt;</code>部分和<code>Switch.System.Net.DontEnableSystemDefaultTlsVersions</code>选择退出交换机：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSystemDefaultTlsVersions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType></li></ul>|

