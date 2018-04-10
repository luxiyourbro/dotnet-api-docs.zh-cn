### <a name="rsacng-and-dsacng-are-once-again-usable-in-partial-trust-scenarios"></a>RSACng 和 DSACng 是在部分信任情况下再次可用

|   |   |
|---|---|
|详细信息|CngLightup (在多个更高级别的加密中使用 api，如<xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>) 和<xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType>在某些情况下依赖于完全信任。 其中包括 P/Invokes 而无需断言<xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>权限和代码路径其中<xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType>具有的权限要求<xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>。 从.NET Framework 4.6.2 开始，CngLightup 用于切换到<xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType>只要有可能。 因此，部分信任应用的成功使用<xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>开始失败并引发<xref:System.Security.SecurityException>异常。此更改将添加所需的断言，以便使用 CngLightup 的所有函数都具有所需的权限。|
|建议|如果在.NET Framework 4.6.2 此更改具有产生负面影响你的部分信任应用程序，升级到.NET Framework 4.7.1。|
|范围|边缘|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.DSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.LegalKeySizes?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.CreateSignature(System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.VerifySignature(System.Byte[],System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Decrypt(System.Byte[],System.Security.Cryptography.RSAEncryptionPadding)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.SignHash(System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

