### <a name="xml-schema-validation-is-stricter"></a>XML 架构验证是更严格

|   |   |
|---|---|
|详细信息|在.NET Framework 4.5 中，XML 架构验证是更为严格。 如果使用 xsd:anyURI 来验证 URL（如 mailto 协议），则当 URL 中有空格时，验证将失败。 在 .NET Framework 的早期版本中，验证将成功。 此更改将影响只有应用程序面向.NET Framework 4.5。|
|建议|如果需要更松散的.NET Framework 4.0 验证，验证应用程序可以面向.NET Framework 版本 4.0。 当重定目标到.NET 4.5，但是，应执行代码评审以确保无效 Uri （带空格） 不与 anyURI 数据类型应作为特性值这一问题。|
|范围|次要|
|版本|4.5|
|类型|重定目标|

