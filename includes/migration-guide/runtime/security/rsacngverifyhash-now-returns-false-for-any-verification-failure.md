### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash 现在任何验证失败，返回 False

|   |   |
|---|---|
|详细信息|从.NET Framework 4.6.2 开始，此方法返回<strong>False</strong>如果本身的签名格式不正确。 现在，返回 false 的任何计算机验证失败。在.NET Framework 4.6 和 4.6.1 中，该方法将引发<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>如果本身的签名格式不正确。|
|建议|其执行取决于处理的任何代码<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>应改为执行，如果验证失败并且该方法返回<strong>False</strong>。|
|范围|次要|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

