### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>在.NET Framework 4.5 下序列化的 MailMessage 对象反序列化可能会失败

|   |   |
|---|---|
|详细信息|从.NET Framework 4.5，开始<xref:System.Web.Mail.MailMessage>对象可以包含非 ASCII 字符。 在 .NET Framework 4 中，仅支持 ASCII 字符。 <xref:System.Web.Mail.MailMessage> 在.NET Framework 4 下，无法反序列的对象，包含非 ASCII 字符，并且经过序列化在.NET Framework 4.5 或更高版本。|
|建议|确保你的代码提供异常处理，反序列化时<xref:System.Web.Mail.MailMessage>对象。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

