### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>通过 ClickOnce 发布的使用 sha-256 代码签名证书的应用程序可能会在 Windows 2003 上失败

|   |   |
|---|---|
|详细信息|使用 SHA256 对可执行文件签名。 以前，无论代码签名证书是 SHA-1 还是 SHA-256，都使用 SHA1 进行签名。 这适用于：<ul><li>使用 Visual Studio 2012 或更高版本生成的所有应用程序。</li><li>使用 Visual Studio 2010 或更早版本在安装了 .NET Framework 4.5 的系统上生成的应用程序。</li></ul>此外，如果安装了 .NET Framework 4.5 或更高版本，则 ClickOnce 清单也会采用 SHA-256 签名，因为 SHA-256 证书与编译所采用的 .NET Framework 版本无关。|
|建议|签名 ClickOnce 可执行文件进行更改仅影响 Windows Server 2003 系统;它们需要安装 KB 938397。签名使用 sha-256 的清单，即使应用是面向.NET Framework 4.0 或更早版本更改，将引入依赖.NET Framework 4.5 或更高版本之间的运行时。|
|范围|边缘|
|版本|4.5|
|类型|重定目标|

