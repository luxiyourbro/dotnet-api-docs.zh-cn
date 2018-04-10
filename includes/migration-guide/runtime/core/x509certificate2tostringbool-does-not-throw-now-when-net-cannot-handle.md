### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) 不会引发现在当.NET 无法处理该证书

|   |   |
|---|---|
|详细信息|如果以前，此方法将引发<code>true</code>传递了 verbose 参数来传递，并且了.NET Framework 不支持的证书安装。 现在，该方法将成功，且返回有效的字符串的省略了证书的无法访问部分。|
|建议|具体取决于任何代码<xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)>应更新为在某些情况下，在其中 API 将具有以前引发预期返回的字符串可能排除一些证书数据 （如公钥、 私钥和扩展）。|
|范围|边缘|
|版本|4.6|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

