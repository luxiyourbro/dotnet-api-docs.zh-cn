### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>多行距 ASP.Net 文本框中时使用 AntiXSSEncoder 更改

|   |   |
|---|---|
|详细信息|在 .NET Framework 4.0 中，如果使用 <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>，则多余行将插入回发的多行文本框中的各行之间。 在 .NET Framework 4.5 中，不包括这些多余的换行符，仅在 Web 应用面向 .NET 4.5 时才可包含|
|建议|请注意，面向 .NET 4.5 的 4.0 Web 应用可能改进了多行文本框，从而不再插入多余的换行符。 如果这样不可取，应用程序可以使这一旧行为，通过面向.NET Framework 4.0 在.NET Framework 4.5 上运行时。|
|范围|次要|
|版本|4.5|
|类型|重定目标|

