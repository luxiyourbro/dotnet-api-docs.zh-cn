### <a name="remove-ssl3-from-the-wcf-transportdefaults"></a>从 WCF TransportDefaults 删除 Ssl3

|   |   |
|---|---|
|详细信息|结合使用 NetTcp 与传输安全性和凭据类型证书时，SSL 3 协议不再是用于协商安全连接的默认协议。 在大多数情况下存在应该不会影响到现有应用 TLS 1.0 已始终包括在协议列表的 NetTcp。 所有现有客户端应该至少能够使用 TLS 1.0 来协商连接。|
|建议|如果 Ssl3 是必需的则可使用以下配置机制之一将 Ssl3 添加到的协商协议的列表。<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols></li><li>[<](~/docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md)</li><li>[&lt;sslStreamSecurity&gt; section of &lt;customBinding&gt;]~/docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)</li></ul>|
|范围|边缘|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols?displayProperty=nameWithType></li><li><xref:System.ServiceModel.TcpTransportSecurity.SslProtocols?displayProperty=nameWithType></li></ul>|

