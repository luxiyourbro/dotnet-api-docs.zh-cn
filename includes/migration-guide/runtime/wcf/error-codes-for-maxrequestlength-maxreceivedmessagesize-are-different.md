### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>MaxRequestLength 或 maxReceivedMessageSize 的错误代码是不同

|   |   |
|---|---|
|详细信息|Web 服务承载于 Internet 信息服务 (IIS) 或 ASP.NET 开发服务器超过 maxRequestLength （在 ASP.NET 中) 在 WCF 中的消息或 maxReceivedMessageSize （在 WCF 中) 具有不同的错误代码 HTTP 状态代码已从 400 （错误请求) 为 413 （请求实体太大），超过 maxRequestLength 或 maxReceivedMessageSize 设置的消息，引发<xref:System.ServiceModel.ProtocolException?displayProperty=name>异常。 这包括传输模式进行流式处理的情况。|
|建议|此更改有利于调试在其中的消息长度超过 ASP.NET 或 WCF 所允许的限制的情况下。必须修改执行处理基于 HTTP 400 状态代码的任何代码。|
|范围|边缘|
|版本|4.5|
|类型|运行时|

