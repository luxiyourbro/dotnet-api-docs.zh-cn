### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>RSACng 现在正确加载非标准的密钥大小的 RSA 的密钥

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 之前的版本，客户的非标准的 RSA 证书的密钥大小不能访问通过这些密钥<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>和<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>扩展方法。  A<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>并显示消息&quot;不支持所请求的密钥大小&quot;引发。 在.NET Framework 4.6.2 中已修复此问题。 同样，<xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)>和<xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)>现在，使用非标准的密钥大小而不引发<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s。|
|建议|如果没有任何异常处理依赖于先前行为的逻辑其中<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>引发时使用非标准的密钥大小，请考虑删除逻辑。|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|

