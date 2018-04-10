### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce 支持 sha-256 上面向 4.0 的应用

|   |   |
|---|---|
|详细信息|以前，包含采用 sha-256 签名的证书的 ClickOnce 应用程序需要.NET 4.5 或更高版本必须存在，，即使应用程序针对 4.0。 现在，面向 4.0 的 ClickOnce 应用可以运行在 4.0，即使使用 sha-256 签名。|
|建议|此更改移除了该依赖性，并允许将 sha-256 证书用于面向.NET Framework 4 和更早版本的 ClickOnce 应用签名。|
|范围|次要|
|版本|4.6|
|类型|重定目标|

