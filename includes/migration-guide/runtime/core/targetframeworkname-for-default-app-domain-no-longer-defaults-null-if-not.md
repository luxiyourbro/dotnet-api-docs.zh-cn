### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>默认应用程序域的 TargetFrameworkName 不再默认为 null，如果未设置

|   |   |
|---|---|
|详细信息|<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>以前在为默认应用程序域，除非显式设置。 从 4.6<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>默认应用程序域的属性将具有默认值 （如果有的话） 从 TargetFrameworkAttribute 派生。 非默认应用程序域将继续继承其<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>从默认应用程序域 （这将不为 null 4.6 中默认） 显式重写。|
|建议|应更新代码，以独立于默认为 null 的 <xref:System.AppDomainSetup.TargetFrameworkName>。 如果需要此属性继续评估为 null，它可显式设为该值。|
|范围|边缘|
|版本|4.6|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

