### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>使用空参数调用 CreateDefaultAuthorizationContext 已更改

|   |   |
|---|---|
|详细信息|实现<xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name>返回通过调用<xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name>与 null authorizationPolicies 参数已更改其在.NET Framework 4.6 中的实现。|
|建议|在极少数情况下，使用自定义身份验证的 WCF 应用可能会看到行为差异。 在这类情况下，可使用以下两种方式之一还原以前的行为：<ol><li>重新编译你的应用以面向早于 4.6 的 .NET Framework 版本。 对于 IIS 承载的服务，使用&lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt;元素以面向.NET Framework 的早期版本。</li><li>将下面的行添加到 app.config 文件的 <code>&lt;appSettings&gt;</code> 部分：<code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|范围|次要|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

