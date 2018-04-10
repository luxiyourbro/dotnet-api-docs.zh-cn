### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims 考虑所有 claimTypes

|   |   |
|---|---|
|详细信息|在面向.NET Framework 4.6.1 中，如果 X509 声明集初始化从与其 SAN 字段中中, 具有多个 DNS 条目的证书的应用中<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name>方法尝试匹配与所有 DNS 条目的 claimType 自变量。对于面向以前版本的.NET Framework 中，应用，<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name>方法尝试匹配 claimType 参数仅与最后一个 DNS 条目。|
|建议|此更改仅影响面向 .NET Framework 4.6.1 的应用程序。 在 [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation) 兼容性开关中，可能会禁用此更改（如果面向 4.6.1 之前的版本，将启用此更改）。|
|范围|次要|
|版本|4.6.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

